# .github Repository

[🇫🇷 Version française](README.fr.md)

This repository contains **default community health files** and templates for all repositories in the **AbsyssLab** organization.

## 📂 What's Inside

This repository provides organization-wide defaults that will be used by all AbsyssLab repositories that don't have their own versions of these files.

### 🏛️ Organization Profile

- **[profile/README.md](profile/README.md)** - Public organization profile displayed on [github.com/AbsyssLab](https://github.com/AbsyssLab)

### 📋 Issue Templates

Located in `ISSUE_TEMPLATE/`:

- **[bug_report.yml](ISSUE_TEMPLATE/bug_report.yml)** - Template for bug reports
- **[feature_request.yml](ISSUE_TEMPLATE/feature_request.yml)** - Template for feature requests
- **[connector_request.yml](ISSUE_TEMPLATE/connector_request.yml)** - Template for new connector proposals
- **[config.yml](ISSUE_TEMPLATE/config.yml)** - Configuration for issue templates

### 🔄 Pull Request Template

- **[pull_request_template.md](PULL_REQUEST_TEMPLATE/pull_request_template.md)** - Standard PR template

### ⚙️ Workflow Templates

Located in `workflow-templates/`:

- **[python-ci.yml](workflow-templates/python-ci.yml)** - CI/CD workflow for Python projects
  - Linting (flake8, pylint)
  - Testing (pytest)
  - Security scanning (bandit, safety)
  - Docker build
- **[release.yml](workflow-templates/release.yml)** - Automated release workflow
  - Changelog generation
  - Release artifacts
  - Docker image publishing

### 📚 Community Health Files

- **[CONTRIBUTING.md](CONTRIBUTING.md)** - How to contribute ([🇫🇷 French](CONTRIBUTING.fr.md))
- **[CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)** - Community guidelines ([🇫🇷 French](CODE_OF_CONDUCT.fr.md))
- **[SECURITY.md](SECURITY.md)** - Security policy and vulnerability reporting ([🇫🇷 French](SECURITY.fr.md))
- **[SUPPORT.md](SUPPORT.md)** - How to get help ([🇫🇷 French](SUPPORT.fr.md))
- **[LICENSE](LICENSE)** - Apache License 2.0

## 🌍 Language Support

This repository provides documentation in:
- **English** (primary) - All files
- **French** - Community health files with `.fr.md` extension

Each language version includes links to switch between languages.

## 🎯 Purpose

### For Repository Maintainers

These defaults ensure consistency across all AbsyssLab repositories:
- Standardized contribution guidelines
- Unified issue and PR templates
- Consistent coding standards
- Common security practices
- Reusable GitHub Actions workflows

### For Contributors

Find everything you need to contribute:
- Clear contribution guidelines
- Bug reporting templates
- Feature request process
- Security vulnerability reporting
- Support resources

## 📖 How It Works

GitHub automatically uses files from this `.github` repository as defaults for any repository in the organization that doesn't have its own versions.

### Precedence

```
Repository-level files > .github repository files > GitHub defaults
```

If a repository has its own `CONTRIBUTING.md`, that will be used instead of the one in this repository.

### Scope

These defaults apply to:
- ✅ Public repositories
- ✅ Private repositories
- ✅ All organization members
- ✅ External contributors

## 🚀 Using Workflow Templates

Workflow templates can be used when creating new workflows in any repository:

1. Go to repository's **Actions** tab
2. Click **New workflow**
3. See **Workflows created by AbsyssLab** section
4. Choose a template and configure it

Templates include:
- Python CI/CD pipeline
- Automated release management

## 📝 Customizing for Your Repository

If a repository needs different guidelines:

1. **Copy the file** from `.github` to your repository
2. **Modify** it as needed
3. **Commit** - your version will override the default

Example:
```bash
# Copy CONTRIBUTING.md to your repo
cp ../.github/CONTRIBUTING.md .
# Edit and customize
vim CONTRIBUTING.md
# Commit
git add CONTRIBUTING.md
git commit -m "Add custom contributing guidelines"
```

## 🔧 Maintaining This Repository

### Updating Templates

When updating templates:

1. **Test changes** in a sample repository first
2. **Document changes** in pull request
3. **Notify** via GitHub Discussions if major changes
4. **Version** significant changes (use tags)

### Best Practices

- Keep templates generic and reusable
- Avoid repository-specific information
- Use placeholders for dynamic content
- Maintain both English and French versions
- Test templates before merging
- Get feedback from maintainers

### Review Schedule

- **Monthly** - Review and update if needed
- **Quarterly** - Community feedback collection
- **Annually** - Major revision if necessary

## 📊 What Gets Applied Where

| File | Used For | Falls Back To |
|------|----------|---------------|
| CONTRIBUTING.md | Contribution guidelines | GitHub default |
| CODE_OF_CONDUCT.md | Community standards | None |
| SECURITY.md | Security policy | None |
| SUPPORT.md | Support resources | None |
| LICENSE | Default license | None |
| Issue templates | Issue creation | GitHub defaults |
| PR template | Pull request creation | GitHub default |
| Workflow templates | Actions workflows | None |

## 🤝 Contributing to This Repository

Want to improve organization-wide defaults?

1. **Open an issue** to discuss major changes
2. **Submit a PR** with your improvements
3. **Test** in a sample repository
4. **Document** what you changed and why

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

## 📞 Questions?

- 💬 [Discussions](https://github.com/orgs/AbsyssLab/discussions) - Ask questions
- 🐛 [Issues](https://github.com/AbsyssLab/.github/issues) - Report problems
- 📖 [Support Guide](SUPPORT.md) - Get help

## 📚 Resources

### GitHub Documentation

- [Creating a default community health file](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
- [About issue and pull request templates](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/about-issue-and-pull-request-templates)
- [Creating workflow templates](https://docs.github.com/en/actions/using-workflows/creating-starter-workflows-for-your-organization)

### AbsyssLab Resources

- [Organization Profile](https://github.com/AbsyssLab)
- [All Repositories](https://github.com/orgs/AbsyssLab/repositories)
- [VTOM Connectors](https://github.com/AbsyssLab?q=vtom&type=all)

## 📄 License

This repository and all default files are licensed under the [Apache License 2.0](LICENSE).

## 🌟 Impact

This repository helps maintain quality and consistency across:
- **19+ connectors** for Visual TOM
- **Multiple contributors** from various organizations
- **Diverse use cases** in production environments

---

<div align="center">
  <strong>Building better open source practices at AbsyssLab</strong>
  <br/>
  <sub>Last updated: October 2025</sub>
</div>

