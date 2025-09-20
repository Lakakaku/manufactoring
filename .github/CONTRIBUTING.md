# Contributing to FactoryKnowledge

Thank you for your interest in contributing to FactoryKnowledge! This document provides guidelines and instructions for contributing to the project.

## Code of Conduct

By participating in this project, you agree to abide by our Code of Conduct, which promotes a respectful and inclusive environment for all contributors.

## Getting Started

1. Fork the repository
2. Clone your fork: `git clone https://github.com/your-username/factoryknowledge.git`
3. Create a new branch: `git checkout -b feature/your-feature-name`
4. Make your changes
5. Commit your changes: `git commit -m "feat: add new feature"`
6. Push to your fork: `git push origin feature/your-feature-name`
7. Create a Pull Request

## Development Setup

```bash
# Install dependencies
npm install

# Run development environment
npm run dev

# Run tests
npm test

# Run linting
npm run lint

# Type checking
npm run typecheck
```

## Commit Messages

We follow [Conventional Commits](https://www.conventionalcommits.org/) for commit messages:

- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation changes
- `style:` Code style changes (formatting, etc.)
- `refactor:` Code refactoring
- `test:` Adding or updating tests
- `chore:` Maintenance tasks
- `perf:` Performance improvements

Examples:
```
feat: add machine QR code generation
fix: resolve video upload timeout issue
docs: update API documentation
```

## Pull Request Process

1. Ensure all tests pass locally
2. Update documentation if needed
3. Add tests for new functionality
4. Ensure no sensitive information is included
5. Request review from maintainers
6. Address review feedback promptly

## Testing Guidelines

- Write unit tests for all new functions
- Ensure integration tests cover critical paths
- Test on both iOS and Android for mobile changes
- Test across different browsers for web changes
- Maintain minimum 80% code coverage

## Code Style

- Follow existing code patterns in the repository
- Use TypeScript for type safety
- Follow ESLint rules
- Use Prettier for formatting
- Keep functions small and focused
- Write self-documenting code

## Project Structure

```
/apps
  /mobile     - React Native app
  /web        - Next.js admin dashboard
  /worker     - Video processing service
/packages
  /shared     - Shared utilities and types
  /ui         - Shared UI components
```

## Areas for Contribution

### Good First Issues
Look for issues labeled `good first issue` for beginner-friendly tasks.

### Priority Areas
- Mobile offline sync improvements
- Video processing optimization
- UI/UX enhancements
- Documentation
- Test coverage
- Accessibility improvements
- Internationalization

## Questions?

- Open a GitHub Discussion for general questions
- Join our community chat
- Check existing issues before creating new ones

## License

By contributing, you agree that your contributions will be licensed under the project's license.