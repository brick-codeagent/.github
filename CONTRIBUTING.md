# Contributing to Brick

Thanks for your interest in contributing! Brick is a modular AI coding agent where every feature is a pluggable extension.

## How to Contribute

### Reporting Bugs

Open a [bug report](https://github.com/brick-codeagent/brick-base/issues/new?labels=bug&template=bug_report.md) with:
- Clear steps to reproduce
- Expected vs actual behavior
- Environment details (Node version, OS, LLM provider)

### Suggesting Features

Open a [feature request](https://github.com/brick-codeagent/brick-base/issues/new?labels=enhancement&template=feature_request.md) describing:
- The problem you're solving
- Your proposed solution
- Whether it could be an extension

### Submitting Pull Requests

1. Fork the repo and create a branch from `main`
2. Make your changes
3. Run `npm run build && npm run lint` to verify
4. Submit a PR with a clear title and description

## Development Setup

```bash
git clone https://github.com/brick-codeagent/brick-base.git
cd brick-base
npm install
npm run build
npm link     # makes `brick` available globally
```

## Code Style

- TypeScript with strict mode
- Follow the patterns in existing code
- Keep functions small (<50 lines) and focused
- No `console.log` in production code
- Use immutable patterns (spread, not mutation)

## Creating Extensions

See the [Extension Developer Guide](https://github.com/brick-codeagent/brick-base/blob/main/docs/EXTENSION_DEV.md) for details on building Brick extensions.

## Code of Conduct

This project follows the [Contributor Covenant](https://github.com/brick-codeagent/.github/blob/main/CODE_OF_CONDUCT.md). Be respectful and inclusive.