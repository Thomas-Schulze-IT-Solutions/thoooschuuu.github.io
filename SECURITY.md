# Security Policy

## Supported Versions

This is a static personal website hosted on GitHub Pages. There is no versioned software release — the `main` branch is always the live version.

| Branch | Supported |
|--------|-----------|
| `main` | ✅ Yes |

## Reporting a Vulnerability

If you discover a security vulnerability in this repository (e.g. exposed secrets, a compromised dependency, or a cross-site scripting issue in the site's JavaScript), please report it responsibly:

1. **Do not open a public GitHub issue** for security vulnerabilities.
2. Use [GitHub's private vulnerability reporting](https://github.com/thoooschuuu/thoooschuuu.github.io/security/advisories/new) to submit a report confidentially.
3. Alternatively, send an e-mail to **info@thomas-schulze-it-solutions.de** with the subject line `[SECURITY] <brief description>`.

You can expect an acknowledgement within **5 business days** and a resolution or mitigation plan within **14 days** for confirmed vulnerabilities.

## Dependency Security

This repository uses [Dependabot](https://docs.github.com/en/code-security/dependabot) to automatically monitor and update:

- **GitHub Actions** used in CI/CD workflows (`.github/workflows/`)
- **npm packages** used by the Playwright test suite (`tests/`)

The production website itself has **zero runtime dependencies** — it is a plain HTML/CSS/JavaScript static site with no third-party frameworks or CDN resources.
