# Security Policy

## Reporting a Vulnerability

If you find a vulnerability, please do not open a public issue with exploit details.

Open a GitHub issue with a minimal description, or contact the maintainer through GitHub.
The project currently does not process server-side user data, but it may handle sensitive
local diary, schedule, and habit data on user devices.

## Security Scope

Relevant areas include:

- Local storage handling
- Service Worker cache behavior
- Notification permission handling
- Android WebView and Manifest configuration
- Dependency vulnerabilities
- Unsafe file exposure in Android configuration
