# Security Policy

[🇫🇷 Version française](SECURITY.fr.md)

## 🔒 Reporting a Vulnerability

The AbsyssLab team takes security bugs seriously. We appreciate your efforts to
responsibly disclose your findings, and will make every effort to acknowledge your
contributions.

### How to Report

**⚠️ Please do NOT report security vulnerabilities through public GitHub issues.**

Instead, please report security vulnerabilities by:

1. **Opening a Security Advisory** (preferred)
   - Go to the repository's Security tab
   - Click "Report a vulnerability"
   - Fill in the details

2. **Sending an email**
   - Email the maintainers with details
   - Use subject line: `[SECURITY] Brief description`

3. **Private issue**
   - Contact a maintainer to create a private issue

### What to Include

To help us better understand and resolve the issue, please include:

- **Type of vulnerability** (e.g., SQL injection, XSS, authentication bypass)
- **Full path** of the source file(s) related to the vulnerability
- **Location** of the affected source code (tag/branch/commit or direct URL)
- **Step-by-step instructions** to reproduce the issue
- **Proof-of-concept or exploit code** (if possible)
- **Impact** of the vulnerability
- **Your assessment** of the severity
- **Proposed mitigation** (if you have suggestions)

### What to Expect

- **Initial response** - Within 48 hours
- **Assessment** - We will evaluate the severity and impact
- **Fix development** - We will work on a fix and keep you updated
- **Disclosure** - Coordinated disclosure after fix is released
- **Credit** - Security advisories will credit the reporter (unless anonymity is requested)

## 🛡️ Security Update Policy

### Supported Versions

We provide security updates for the following versions:

| Version | Supported          |
| ------- | ------------------ |
| Latest  | ✅ Yes             |
| < Latest| ⚠️ Best effort     |

We strongly recommend always using the latest version of our connectors.

### Security Updates

- Security patches are released as soon as possible after a vulnerability is confirmed
- Updates are announced via:
  - GitHub Security Advisories
  - Repository releases
  - GitHub Discussions (if critical)

## 🔐 Security Best Practices

When using AbsyssLab VTOM connectors, follow these security best practices:

### 1. Credentials Management

**❌ DON'T:**
- Hard-code credentials in scripts
- Store passwords in plain text
- Commit credentials to version control
- Share credentials in logs or issues

**✅ DO:**
- Use environment variables
- Use secret management systems (HashiCorp Vault, Azure Key Vault, AWS Secrets Manager)
- Use VTOM's built-in credential management
- Rotate credentials regularly
- Use service accounts with minimum required permissions

### 2. Network Security

**Recommendations:**
- Use TLS/SSL for all API communications
- Implement network segmentation
- Use firewalls to restrict access
- Enable API rate limiting when available
- Use private networks for sensitive operations

### 3. Access Control

**Recommendations:**
- Apply principle of least privilege
- Use role-based access control (RBAC)
- Regularly audit user permissions
- Remove unused accounts
- Enable multi-factor authentication (MFA) where supported

### 4. Logging and Monitoring

**Recommendations:**
- Enable audit logging
- Monitor for suspicious activities
- Mask sensitive data in logs
- Regularly review logs
- Set up alerts for security events

### 5. Updates and Patching

**Recommendations:**
- Keep connectors up to date
- Subscribe to security advisories
- Test updates in non-production environments first
- Have a rollback plan
- Document your update procedures

## 🚨 Known Security Considerations

### API Keys and Tokens

Many connectors require API keys or tokens. Always:
- Store them securely
- Never expose them in code or logs
- Use environment variables or secret managers
- Rotate them periodically
- Revoke unused tokens

### Docker Containers

If using containerized connectors:
- Use official base images
- Keep base images updated
- Scan images for vulnerabilities
- Don't run containers as root
- Use read-only filesystems when possible

### External Dependencies

- Regularly update Python dependencies
- Use `pip-audit` or `safety` to check for known vulnerabilities
- Pin dependency versions in production
- Review dependency licenses and security records

## 📋 Security Checklist

Before deploying a connector in production:

- [ ] Credentials stored securely (not hard-coded)
- [ ] TLS/SSL enabled for API communications
- [ ] Minimum required permissions configured
- [ ] Audit logging enabled
- [ ] Sensitive data masked in logs
- [ ] Latest version of connector installed
- [ ] Dependencies up to date and scanned
- [ ] Network access restricted appropriately
- [ ] Monitoring and alerting configured
- [ ] Incident response plan documented
- [ ] Backup and recovery procedures tested

## 🔍 Vulnerability Disclosure Timeline

1. **Day 0** - Vulnerability reported
2. **Day 1-2** - Initial response and acknowledgment
3. **Day 3-7** - Vulnerability assessed and severity determined
4. **Day 7-30** - Fix developed and tested
5. **Day 30** - Fix released (may be sooner for critical issues)
6. **Day 30+** - Public disclosure in security advisory

For critical vulnerabilities, we aim for a faster timeline.

## 📞 Contact

For security-related questions that are not vulnerabilities:
- Open a discussion in the repository
- Tag it with `security` label

For general questions about security:
- See our [Support Guide](SUPPORT.md)

## 🏆 Hall of Fame

We recognize security researchers who help us keep our projects secure:

<!-- Security researchers will be listed here after responsible disclosure -->

*Be the first to help us improve our security!*

---

**Thank you for helping keep AbsyssLab VTOM connectors secure! 🙏**

