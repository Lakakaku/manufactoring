# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

FactoryKnowledge is a mobile-first video knowledge management platform for manufacturing facilities. Workers document machine operations through video, creating a searchable, offline-accessible knowledge base on the factory floor.

## Architecture

### Technology Stack
- **Mobile App**: React Native (iOS/Android)
- **Admin Dashboard**: Next.js 14 with App Router
- **Database**: Supabase (PostgreSQL with RLS)
- **Video Processing**: FFmpeg on Railway workers
- **Video Storage**: Supabase Storage with CDN
- **Authentication**: Supabase Auth
- **Payments**: Stripe
- **Styling**: Tailwind CSS

### Project Structure (Planned Monorepo)
```
/apps/mobile         - React Native mobile application
/apps/web           - Next.js admin dashboard
/apps/worker        - Video processing service (Railway)
/packages/shared    - Shared types, utilities, and business logic
/packages/ui        - Shared UI components
```

## Development Commands

Since this is a greenfield project, standard commands will be established as the project develops:

### Expected Commands (to be implemented)
```bash
# Root monorepo
npm install          # Install all dependencies
npm run dev          # Start all services in development
npm run build        # Build all packages
npm run test         # Run all tests
npm run lint         # Lint all packages
npm run typecheck    # Type check all packages

# Mobile app (apps/mobile)
npm run ios          # Run iOS app
npm run android      # Run Android app
npm run test:mobile  # Test mobile app

# Web dashboard (apps/web)
npm run dev:web      # Start Next.js dev server
npm run build:web    # Build for production
npm run test:web     # Test web app

# Video worker (apps/worker)
npm run dev:worker   # Start worker locally
npm run test:worker  # Test video processing
```

## Key Implementation Notes

### Database Design
- **Factory isolation**: All data is isolated at the factory level using RLS policies
- **Machine ownership**: Any authenticated factory user can add machines (tracked via `added_by_user_id`)
- **Offline sync**: Mobile app uses SQLite for offline storage with sync queue (`offline_sync_queue` table)
- **Search**: PostgreSQL full-text search with trigram similarity for typo tolerance

### Video Processing Pipeline
1. Videos uploaded to temporary storage
2. Railway worker picks up processing job from queue
3. FFmpeg compresses and generates multiple quality versions
4. Thumbnails generated automatically
5. Processed videos moved to CDN-backed storage
6. Original video archived or deleted based on settings

### Mobile Offline Architecture
- SQLite mirrors critical Supabase tables
- Sync queue captures all offline actions
- Delta sync minimizes bandwidth usage
- Conflict resolution favors latest timestamp
- Auto-downloads content based on department assignment

### Authentication Flow
1. Factory admin creates account and receives Factory Join Code
2. Workers enter join code in mobile app
3. User assigned role (admin/worker) and department
4. Department determines initial content sync
5. Knowledge Champions have additional approval rights

### Critical Performance Targets
- App launch to search: <2 seconds
- Video start playing: <1 second (if cached)
- Upload processing: <30 seconds for 5-minute video
- Search results: <200ms
- Machine addition form: <500ms to load

## Current Development Phase

The project is in initial setup phase. Reference TASKS.md for the complete development roadmap with 400+ specific tasks organized by component and phase.

## Testing Strategy

- Unit tests: Jest for all packages (target 80% coverage)
- Integration tests: Test database operations, API integrations, video processing
- E2E tests: Cypress for web, Detox for React Native
- Performance tests: Focus on video upload, search response, and offline sync

## Security Considerations

- All videos encrypted at rest (AES-256)
- Row Level Security enforces factory-level data isolation
- Signed URLs for video access (no public access)
- API rate limiting on all endpoints
- Audit logs for compliance tracking

## Deployment Targets

- **Web Dashboard**: Vercel
- **Video Worker**: Railway
- **Database**: Supabase (managed)
- **Mobile Apps**: App Store (iOS), Play Store (Android)
- **CDN**: CloudFront or similar for video delivery