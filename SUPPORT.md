# Support

[🇫🇷 Version française](SUPPORT.fr.md)

Welcome to Absyss VTOM Connectors support! 👋

This document will help you find the assistance you need.

## 📚 Documentation

Before opening an issue, please check the available documentation:

### Connector-Specific Documentation

Each connector has its own README with:
- Installation instructions
- Configuration guide
- Usage examples
- Troubleshooting section
- API reference

### General Resources

- [Contributing Guide](CONTRIBUTING.md) - How to contribute
- [Code of Conduct](CODE_OF_CONDUCT.md) - Community guidelines
- [Security Policy](SECURITY.md) - How to report security issues

## 🆘 Getting Help

### 1. Search Existing Issues

Before creating a new issue, please search:
- [Organization-wide issues](https://github.com/search?q=org%3AAbsyssLab+type%3Aissue)
- Specific repository issues
- Closed issues (your question might already be answered)

### 2. GitHub Discussions 💬

For questions, ideas, and community interaction:
- [Organization Discussions](https://github.com/orgs/AbsyssLab/discussions)

**Good for:**
- General questions
- Best practices
- Use case discussions
- Feature brainstorming
- Community help

### 3. Create an Issue 🐛

Use the appropriate template:

- **[Bug Report](https://github.com/AbsyssLab/.github/issues/new?template=bug_report.yml)**
  - Something isn't working
  - Unexpected behavior
  - Error messages

- **[Feature Request](https://github.com/AbsyssLab/.github/issues/new?template=feature_request.yml)**
  - New functionality
  - Enhancement to existing feature
  - Performance improvement

- **[Connector Request](https://github.com/AbsyssLab/.github/issues/new?template=connector_request.yml)**
  - Propose a new connector
  - Integration with new tool/platform

## 🔍 Troubleshooting

### Common Issues

#### Connection Errors

**Symptoms:** Unable to connect to target API/service

**Solutions:**
1. Verify credentials are correct
2. Check network connectivity
3. Verify firewall rules
4. Ensure target service is accessible
5. Check for proxy requirements
6. Review API endpoint URLs

#### Authentication Failures

**Symptoms:** 401/403 errors, "Unauthorized" messages

**Solutions:**
1. Verify API keys/tokens are valid
2. Check token expiration
3. Ensure proper permissions are granted
4. Verify service account configuration
5. Check for MFA requirements

#### Job Execution Failures

**Symptoms:** Jobs fail with error codes

**Solutions:**
1. Check VTOM logs (stdout/stderr)
2. Verify job parameters
3. Ensure all dependencies are installed
4. Check Python version compatibility
5. Verify environment variables
6. Review resource availability (disk space, memory)

#### Performance Issues

**Symptoms:** Slow execution, timeouts

**Solutions:**
1. Check network latency
2. Review API rate limits
3. Optimize query parameters
4. Increase timeout values
5. Consider batch operations
6. Monitor system resources

### Debug Mode

Most connectors support debug mode for detailed logging:

```bash
# Set debug environment variable
export DEBUG=1
export VTOM_LOG_LEVEL=DEBUG

# Run with verbose output
python connector.py --debug
```

### Log Analysis

When reporting issues, include:
- Full error messages
- Stack traces
- Relevant log snippets (with sensitive data removed)
- VTOM job output
- Connector version
- Environment details

## 📋 Information to Provide

When asking for help, please include:

### Environment
- Visual TOM version
- Connector version
- Python version
- Operating System
- Target service/API version

### Configuration
- Relevant configuration (remove sensitive data)
- Environment variables used
- Job definition (if applicable)

### Error Details
- Complete error message
- Stack trace
- Steps to reproduce
- Expected vs actual behavior
- Logs (sanitized)

### Example Format

```markdown
**Environment:**
- VTOM: 6.4.0
- Connector: vtom-azure-data-factory v1.2.0
- Python: 3.10.5
- OS: Ubuntu 20.04
- Azure Data Factory: V2

**Issue:**
Job fails when triggering pipeline with parameters

**Error:**
```
Error: Pipeline trigger failed
Status code: 400
Message: Invalid parameter format
```

**Steps to Reproduce:**
1. Configure job with parameters: {...}
2. Execute job from VTOM
3. Error occurs

**Expected:** Pipeline should trigger successfully
**Actual:** 400 error returned
```

## 🚀 Quick Start Guides

### Installation

```bash
# Clone the connector
git clone https://github.com/AbsyssLab/<connector-name>.git

# Install dependencies
pip install -r requirements.txt

# Configure
cp config.example.yaml config.yaml
# Edit config.yaml with your settings

# Test
python connector.py --test
```

### Basic Configuration

Most connectors require:
1. **API credentials** - Token, key, or username/password
2. **Endpoint URL** - Target service URL
3. **Connection settings** - Timeout, retry, etc.
4. **VTOM integration** - Job definition, parameters

### Integration with VTOM

1. **Copy connector** to VTOM scripts directory
2. **Create job** in VTOM application
3. **Configure parameters** as job variables
4. **Set environment** variables for credentials
5. **Test execution** manually first
6. **Schedule job** once working

## 📞 Contact Options

### Community Support (Free)

- GitHub Discussions - Questions and community help
- GitHub Issues - Bug reports and feature requests
- Public documentation - README, guides

**Response time:** Best effort, community-driven

### Professional Support

For organizations requiring:
- SLA-backed support
- Priority bug fixes
- Custom development
- Training and consulting
- Direct technical support

Please contact the maintainers through GitHub.

## ⏰ Response Times

**Community Support:**
- Questions: Usually within 2-5 days
- Bug reports: Acknowledged within 1 week
- Feature requests: Reviewed monthly

**Critical Issues:**
- Security vulnerabilities: Within 48 hours
- Critical bugs: Prioritized based on impact

## 🌐 Language Support

- **English** - Primary language for all documentation and issues
- **French** - Community translations available for some documents

When asking for help in languages other than English, please note that
response times may be longer.

## 📖 Learning Resources

### Visual TOM Resources
- [Absyss Official Website](https://www.absyss.com)
- Visual TOM Documentation
- VTOM API Reference

### Connector Development
- [Python Best Practices](https://docs.python-guide.org/)
- API Integration Guides
- GitHub Actions CI/CD

### Contributing
- [How to Contribute](CONTRIBUTING.md)
- [Code of Conduct](CODE_OF_CONDUCT.md)
- Pull Request Guidelines

## ✅ Support Checklist

Before requesting help:

- [ ] I've read the connector's README
- [ ] I've searched existing issues
- [ ] I've checked the troubleshooting guide
- [ ] I've verified my configuration
- [ ] I've tested with debug logging enabled
- [ ] I have all required information ready
- [ ] I've removed sensitive data from logs

## 🤝 Community

Join our community:
- ⭐ Star repositories you find useful
- 👀 Watch repositories for updates
- 🍴 Fork and experiment
- 💬 Participate in discussions
- 🐛 Report bugs
- ✨ Suggest features
- 🔧 Contribute code

## 📜 Disclaimer

Absyss VTOM connectors are provided "as is" under the Apache License 2.0.
While we strive to provide quality software and support, there are no warranties
or guarantees. See the [LICENSE](LICENSE) for details.

---

**Thank you for using Absyss VTOM Connectors! 🙏**

<div align="center">
  <sub>Questions? Don't hesitate to ask in Discussions!</sub>
</div>

