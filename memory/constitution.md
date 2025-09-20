# FactoryKnowledge Constitution

## Core Values

### Mission
Democratize manufacturing knowledge by empowering every factory worker to document, share, and access operational expertise through intuitive video-based learning.

### Vision
Become the global standard for manufacturing knowledge management, where every machine procedure is documented, every worker is empowered, and operational excellence is achieved through shared expertise.

## Fundamental Principles

### 1. Worker-First Design
- Mobile experience takes precedence over desktop
- Offline capability is non-negotiable
- Interface must work on low-cost devices
- Minimize text input, maximize visual interaction

### 2. Collaborative Knowledge Ownership
- Any worker can contribute to the knowledge base
- Documentation is a shared responsibility
- Recognition and credit for contributions
- Collective intelligence over individual expertise

### 3. Simplicity Over Features
- 10-minute video limit encourages focused content
- One procedure, one video, one purpose
- Clear over comprehensive
- Essential features only in MVP

### 4. Trust Through Transparency
- Clear data ownership (factory owns their data)
- Visible contribution tracking
- Audit trails for compliance
- Open about limitations and roadmap

### 5. Continuous Learning Culture
- Make documentation rewarding, not burdensome
- Celebrate knowledge sharing
- Learn from usage patterns
- Iterate based on factory floor feedback

## Technical Principles

### 1. Offline-First Architecture
- Local-first data storage
- Queue-based sync strategy
- Conflict resolution favors most recent
- Graceful degradation without connectivity

### 2. Progressive Enhancement
- Core features work on all devices
- Enhanced features for capable devices
- Performance over aesthetics
- Battery efficiency consideration

### 3. Data Sovereignty
- Factory-level isolation is absolute
- No cross-factory data leakage
- Export capabilities for data portability
- Clear deletion and retention policies

### 4. Scalable Simplicity
- Start simple, scale smartly
- Monorepo for initial velocity
- Microservices when needed, not before
- Database design supports future growth

### 5. Security by Design
- Encryption at rest and in transit
- Principle of least privilege
- Regular security audits
- Compliance-ready from day one

## Product Principles

### 1. Video as Primary Medium
- Video captures tacit knowledge text cannot
- Visual learning for diverse literacy levels
- Standardize recording (landscape, quality)
- Optimize for factory floor viewing

### 2. Search Must Be Forgiving
- Typo-tolerant search
- Multiple languages and dialects
- Visual search (future: find by machine photo)
- Context-aware suggestions

### 3. Quality Through Community
- Peer review over top-down control
- Knowledge Champions as quality gates
- Version history preserves all contributions
- Feedback loops improve content

### 4. Measurable Impact
- Track documentation coverage
- Measure knowledge gaps
- Monitor usage patterns
- Demonstrate ROI through metrics

## Operational Principles

### 1. Customer Success
- Onboarding determines retention
- First video within first day
- Regular check-ins during first month
- Success metrics shared transparently

### 2. Sustainable Growth
- Revenue before features
- Profitable unit economics
- Organic growth through word-of-mouth
- Strategic partnerships over paid acquisition

### 3. Continuous Deployment
- Ship daily, learn constantly
- Feature flags for gradual rollout
- Rollback capability within minutes
- Monitor everything, alert on anomalies

### 4. Open Communication
- Public roadmap
- Transparent incident reports
- Regular customer advisory sessions
- Community-driven feature prioritization

## Non-Negotiables

### What We Will Always Do
1. Protect factory data with encryption
2. Maintain offline functionality
3. Support multiple languages
4. Provide data export capabilities
5. Respect worker privacy
6. Maintain backward compatibility
7. Respond to security issues within 48 hours

### What We Will Never Do
1. Sell or share factory data
2. Require constant internet connection
3. Lock customers into our platform
4. Discriminate content by subscription tier
5. Use worker data for advertising
6. Implement surveillance features
7. Compromise security for convenience

## Decision Framework

When making product or technical decisions, ask:

1. **Does this help a worker on the factory floor?**
2. **Will this work offline?**
3. **Can a worker with minimal training use this?**
4. **Does this respect data sovereignty?**
5. **Is this the simplest solution that works?**
6. **Will this scale to 10,000 factories?**
7. **Does this align with our mission?**

If any answer is "no," reconsider the approach.

## Evolution Clause

This constitution is a living document. Changes require:
- Documented rationale
- Customer feedback consideration
- Team consensus
- 30-day notice for breaking changes
- Migration path for affected features

Last Updated: 2025-09-20
Version: 1.0.0