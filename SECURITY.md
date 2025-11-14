# Security Policy

## Our Commitment

The security of Exact Word Counter is a top priority. We take all security vulnerabilities seriously and appreciate your efforts to responsibly disclose your findings.

## Privacy & Security Features

### By Design
- **100% Client-Side**: All text processing happens in your browser
- **No Data Transmission**: Your text never leaves your device
- **No Tracking**: Zero analytics, cookies, or third-party services
- **No Server**: Static files only, no backend infrastructure
- **Open Source**: Fully auditable code

### Technical Security
- **Content Security Policy**: Can be implemented via web server headers
- **No eval()**: No dynamic code execution
- **No inline scripts**: (Except embedded in index.html for zero-dependency design)
- **HTTPS Ready**: Works with HTTPS for secure connections
- **LocalStorage Only**: Minimal data storage, only user preferences

## Supported Versions

We provide security updates for the following versions:

| Version | Supported          |
| ------- | ------------------ |
| 2.0.x   | :white_check_mark: |
| 1.0.x   | :white_check_mark: |
| < 1.0   | :x:                |

## Reporting a Vulnerability

We appreciate responsible disclosure of security vulnerabilities.

### Where to Report

**DO NOT** open a public GitHub issue for security vulnerabilities.

Instead, please report security issues via:

1. **GitHub Security Advisory** (Preferred)
   - Go to the [Security tab](https://github.com/Raoof128/Word_Counter/security)
   - Click "Report a vulnerability"
   - Fill out the form with details

2. **Email** (Alternative)
   - Email: [Create GitHub issue after fixing]
   - Use subject: "SECURITY: [Brief description]"

### What to Include

Please include the following information:

- **Type of vulnerability** (e.g., XSS, CSRF, data leak)
- **Affected component** (e.g., index.html, service-worker.js)
- **Steps to reproduce** (detailed, step-by-step)
- **Potential impact** (what can an attacker do?)
- **Proof of concept** (code, screenshots, or video)
- **Suggested fix** (if you have one)
- **Your environment** (browser, OS version)

### Example Report Template

```markdown
## Vulnerability Type
[e.g., Cross-Site Scripting (XSS)]

## Affected Component
[e.g., Text input sanitization in index.html:500]

## Description
[Clear description of the vulnerability]

## Steps to Reproduce
1. Step one
2. Step two
3. Step three

## Impact
[What can an attacker achieve? Who is affected?]

## Proof of Concept
[Code snippet, screenshot, or description]

## Suggested Fix
[If you have a recommendation]

## Environment
- Browser: Chrome 120
- OS: Windows 11
- Version: 2.0.0
```

## Response Timeline

- **Initial Response**: Within 48 hours
- **Status Update**: Within 7 days
- **Fix Timeline**: Depends on severity
  - **Critical**: 1-7 days
  - **High**: 7-14 days
  - **Medium**: 14-30 days
  - **Low**: 30-60 days

## Disclosure Policy

- We will acknowledge receipt of your vulnerability report
- We will work with you to understand and validate the issue
- We will keep you informed of our progress
- We will credit you in the release notes (if you wish)
- We request that you:
  - Give us reasonable time to fix the issue before public disclosure
  - Make a good faith effort to avoid privacy violations
  - Not exploit the vulnerability beyond proof of concept

## Security Best Practices for Users

When using Exact Word Counter:

### Recommended
- ✅ Use HTTPS when hosting (especially if deployed)
- ✅ Keep your browser updated
- ✅ Use a modern browser with security features
- ✅ Review the code before self-hosting
- ✅ Verify the source when downloading

### Important Notes
- 🔒 Your text stays in your browser - it's never transmitted
- 🔒 LocalStorage data persists locally only
- 🔒 Service Worker caches are local to your device
- 🔒 No authentication needed - nothing to compromise

## Security Considerations

### For Self-Hosting

If you're hosting Exact Word Counter yourself, consider:

1. **Content Security Policy Headers**
```
Content-Security-Policy: default-src 'self'; script-src 'self' 'unsafe-inline'; style-src 'self' 'unsafe-inline'
```

2. **HTTPS Configuration**
- Use Let's Encrypt for free SSL certificates
- Force HTTPS redirects
- Use HSTS header

3. **Server Headers**
```
X-Content-Type-Options: nosniff
X-Frame-Options: DENY
X-XSS-Protection: 1; mode=block
Referrer-Policy: no-referrer
```

### For Development

When contributing:
- Never commit sensitive data
- Review all external resources (we use none!)
- Validate all user inputs
- Test for XSS vulnerabilities
- Follow secure coding practices

## Known Security Considerations

### Current Architecture
- **Inline Scripts**: Scripts are in HTML for zero-dependency design
  - Trade-off: Simpler deployment vs. stricter CSP
  - Mitigation: Code is auditable and static

- **LocalStorage**: Used for preferences
  - Not encrypted (browser limitation)
  - Only stores non-sensitive configuration
  - Can be cleared by user anytime

### Not Vulnerabilities
- Text visible in browser DevTools: *By design* (client-side app)
- LocalStorage readable: *Expected* (stores only preferences)
- Service Worker cache: *Intended* (offline functionality)

## Hall of Fame

We recognize security researchers who help improve our security:

<!-- Contributors who report valid security issues will be listed here -->

*No security issues reported yet*

## Questions?

For general questions about security (not vulnerability reports):
- Open a GitHub Discussion
- Tag as "security"

---

Thank you for helping keep Exact Word Counter and its users safe!
