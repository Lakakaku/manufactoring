# Security Policy

## Supported Versions

We provide security updates for the following versions:

| Version | Supported          |
| ------- | ------------------ |
| 1.x.x   | :white_check_mark: |
| < 1.0   | :x:                |

## Reporting a Vulnerability

We take security vulnerabilities seriously. If you discover a security issue, please follow these steps:

### DO NOT create a public GitHub issue

Instead, please report vulnerabilities via:

**Email**: security@factoryknowledge.com

### What to Include

When reporting a vulnerability, please include:

1. **Description**: Clear description of the vulnerability
2. **Impact**: Potential impact and severity assessment
3. **Steps to Reproduce**: Detailed steps to reproduce the issue
4. **Proof of Concept**: Code or screenshots if applicable
5. **Suggested Fix**: Any recommendations for fixing the issue

### Response Timeline

- **Initial Response**: Within 48 hours
- **Status Update**: Within 5 business days
- **Resolution Target**:
  - Critical: 7 days
  - High: 14 days
  - Medium: 30 days
  - Low: 90 days

## Security Best Practices

### For Contributors

- Never commit sensitive data (API keys, passwords, tokens)
- Use environment variables for configuration
- Follow secure coding practices
- Keep dependencies updated
- Run security scans before submitting PRs

### For Users

- Keep your FactoryKnowledge installation updated
- Use strong passwords and enable 2FA for admin accounts
- Regularly review user permissions
- Monitor access logs
- Use HTTPS for all connections
- Restrict database access

## Security Features

FactoryKnowledge implements multiple security layers:

### Data Protection
- AES-256 encryption for videos at rest
- TLS 1.3 for data in transit
- Row Level Security in database
- Signed URLs for video access

### Authentication & Authorization
- Supabase Auth with JWT tokens
- Role-based access control (RBAC)
- Session management with refresh tokens
- Two-factor authentication for admins

### Infrastructure Security
- Regular security audits
- Dependency vulnerability scanning
- Container security scanning
- API rate limiting
- CORS policy enforcement

## Compliance

FactoryKnowledge is designed to meet:
- GDPR requirements
- ISO 9001 standards
- SOC 2 Type II (in progress)
- OWASP security guidelines

## Security Contacts

- Primary: security@factoryknowledge.com
- Backup: engineering@factoryknowledge.com

## Acknowledgments

We appreciate responsible disclosure and will acknowledge security researchers who help us improve FactoryKnowledge's security.

## PGP Key

For encrypted communications, use our PGP key:
```
[PGP key will be added here]
```