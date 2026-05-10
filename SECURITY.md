# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability in Brick, please **do not** open a public issue.

Instead, send a private report to the repository maintainer via GitHub's
[private vulnerability reporting](https://github.com/brick-codeagent/brick-base/security/advisories/new)
feature.

Please include:

- A description of the vulnerability
- Steps to reproduce
- Potential impact

You should receive a response within 48 hours. If the issue is confirmed, a
fix will be released as soon as possible depending on complexity.

## Preferred Encryption

Not available yet — please use the GitHub private reporting tool linked above.

## Known Security Practices

- Brick uses environment variables for API keys (`BRICK_API_KEY`)
- Extensions run as separate processes with stdio isolation
- Shell commands execute with configurable timeout (default 30s)
- No telemetry or data collection
- Git operations respect existing `.gitignore` rules