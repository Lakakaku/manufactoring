# Technology Stack

## Frontend
### Mobile App (React Native)
- **Framework**: React Native with Expo
- **Navigation**: React Navigation
- **State Management**: Zustand + React Query
- **Offline Storage**: SQLite with TypeORM
- **Video Player**: react-native-video
- **UI Components**: Custom components with NativeWind (Tailwind for RN)

### Admin Dashboard (Next.js)
- **Framework**: Next.js 14 with App Router
- **Styling**: Tailwind CSS + shadcn/ui
- **State Management**: Zustand + React Query
- **Forms**: React Hook Form + Zod
- **Charts**: Recharts
- **Tables**: TanStack Table

## Backend
### Database (Supabase)
- **Core Database**: PostgreSQL
- **Real-time**: Supabase Realtime for sync
- **Authentication**: Supabase Auth
- **Storage**: Supabase Storage for videos
- **Row Level Security**: Factory-level data isolation

### Video Processing (Railway)
- **Runtime**: Node.js workers on Railway
- **Processing**: FFmpeg for compression and transcoding
- **Queue**: PostgreSQL-based job queue
- **Storage**: Multi-tier (temp → processing → CDN)

### API Layer
- **Framework**: tRPC for type-safe APIs
- **Validation**: Zod schemas
- **Rate Limiting**: Upstash Redis

## Infrastructure
### Deployment
- **Web**: Vercel
- **Workers**: Railway
- **Database**: Supabase (managed)
- **CDN**: CloudFront for video delivery
- **Monitoring**: Sentry + Vercel Analytics

### Development Tools
- **Monorepo**: Turborepo
- **Package Manager**: pnpm
- **Type Checking**: TypeScript strict mode
- **Linting**: ESLint + Prettier
- **Testing**: Jest + React Testing Library
- **E2E Testing**: Cypress (web), Detox (mobile)

## Key Technical Decisions
1. **Offline-First**: SQLite for mobile ensures factory floor usability
2. **Video Optimization**: Multiple quality versions for bandwidth efficiency
3. **Factory Isolation**: RLS policies ensure complete data separation
4. **Progressive Sync**: Delta sync minimizes bandwidth usage
5. **Type Safety**: End-to-end TypeScript with tRPC