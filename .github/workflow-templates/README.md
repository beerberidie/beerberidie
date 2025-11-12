# 🔧 GitHub Actions Workflow Templates

This directory contains reusable CI/CD workflow templates for Python and Node.js projects.

---

## 📋 Available Templates

### 1. **python-ci.yml** - Python CI/CD Pipeline

**Use this template for:**
- Python projects with `requirements.txt`
- Python packages with `pyproject.toml`
- FastAPI, Flask, Django applications
- Python CLI tools

**Features:**
- ✅ Multi-version testing (Python 3.9, 3.10, 3.11)
- ✅ Code linting with flake8
- ✅ Code formatting check with black
- ✅ Type checking with mypy
- ✅ Testing with pytest and coverage reporting
- ✅ Security scanning with bandit
- ✅ Dependency vulnerability checking with safety
- ✅ Codecov integration for coverage reports

**How to use:**
1. Copy `python-ci.yml` to your project's `.github/workflows/` directory
2. Customize the Python versions if needed
3. Ensure your project has either `requirements.txt` or `pyproject.toml`
4. Add a `tests/` directory with pytest tests
5. Commit and push to trigger the workflow

**Example project structure:**
```
your-project/
├── .github/
│   └── workflows/
│       └── ci.yml          # Copy python-ci.yml here
├── src/                    # Your source code
├── tests/                  # Your tests
├── requirements.txt        # Dependencies
├── README.md
└── LICENSE
```

---

### 2. **node-ci.yml** - Node.js/TypeScript CI/CD Pipeline

**Use this template for:**
- React applications
- TypeScript projects
- Node.js backend services
- Vite/Next.js/Create React App projects

**Features:**
- ✅ Multi-version testing (Node.js 16, 18, 20)
- ✅ Code linting (ESLint)
- ✅ TypeScript type checking
- ✅ Testing with coverage
- ✅ Build verification
- ✅ Security audit with npm audit
- ✅ Outdated package detection
- ✅ Build artifact upload

**How to use:**
1. Copy `node-ci.yml` to your project's `.github/workflows/` directory
2. Customize the Node.js versions if needed
3. Ensure your `package.json` has the following scripts:
   - `lint` - For linting (optional)
   - `type-check` - For TypeScript checking (optional)
   - `test` - For running tests (optional)
   - `test:coverage` - For coverage reports (optional)
   - `build` - For building the application (required)
4. Commit and push to trigger the workflow

**Example package.json scripts:**
```json
{
  "scripts": {
    "dev": "vite",
    "build": "tsc && vite build",
    "lint": "eslint . --ext ts,tsx --report-unused-disable-directives --max-warnings 0",
    "type-check": "tsc --noEmit",
    "test": "vitest",
    "test:coverage": "vitest --coverage"
  }
}
```

**Example project structure:**
```
your-project/
├── .github/
│   └── workflows/
│       └── ci.yml          # Copy node-ci.yml here
├── src/                    # Your source code
├── tests/                  # Your tests (optional)
├── package.json
├── tsconfig.json           # For TypeScript projects
├── README.md
└── LICENSE
```

---

## 🚀 Quick Start

### For Python Projects:

```bash
# 1. Create workflows directory
mkdir -p .github/workflows

# 2. Copy the Python template
cp path/to/python-ci.yml .github/workflows/ci.yml

# 3. Commit and push
git add .github/workflows/ci.yml
git commit -m "ci: add GitHub Actions workflow"
git push
```

### For Node.js Projects:

```bash
# 1. Create workflows directory
mkdir -p .github/workflows

# 2. Copy the Node.js template
cp path/to/node-ci.yml .github/workflows/ci.yml

# 3. Commit and push
git add .github/workflows/ci.yml
git commit -m "ci: add GitHub Actions workflow"
git push
```

---

## 📊 Adding Status Badges to README

After setting up the workflow, add a status badge to your README:

### Python Projects:
```markdown
![CI](https://github.com/YOUR_USERNAME/YOUR_REPO/workflows/Python%20CI%2FCD%20Pipeline/badge.svg)
```

### Node.js Projects:
```markdown
![CI](https://github.com/YOUR_USERNAME/YOUR_REPO/workflows/Node.js%20CI%2FCD%20Pipeline/badge.svg)
```

Replace `YOUR_USERNAME` and `YOUR_REPO` with your actual GitHub username and repository name.

---

## 🔧 Customization Options

### Changing Trigger Branches

By default, workflows run on `main` and `develop` branches. To change this:

```yaml
on:
  push:
    branches: [ main, master, staging ]  # Add your branches here
  pull_request:
    branches: [ main, master ]
```

### Changing Python/Node Versions

**Python:**
```yaml
strategy:
  matrix:
    python-version: ['3.9', '3.10', '3.11', '3.12']  # Add/remove versions
```

**Node.js:**
```yaml
strategy:
  matrix:
    node-version: [16.x, 18.x, 20.x, 21.x]  # Add/remove versions
```

### Disabling Specific Jobs

To disable a job, comment it out or remove it:

```yaml
# jobs:
#   security-audit:  # This job is now disabled
#     name: Security Audit
#     runs-on: ubuntu-latest
#     steps:
#       ...
```

---

## 🛡️ Security Best Practices

1. **Never commit secrets** - Use GitHub Secrets for API keys and tokens
2. **Keep dependencies updated** - Regularly run `npm audit` or `safety check`
3. **Review security alerts** - Enable Dependabot alerts in repository settings
4. **Use specific action versions** - Pin actions to specific versions (e.g., `@v4`)

---

## 📚 Additional Resources

- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Workflow Syntax Reference](https://docs.github.com/en/actions/reference/workflow-syntax-for-github-actions)
- [GitHub Actions Marketplace](https://github.com/marketplace?type=actions)
- [Codecov Documentation](https://docs.codecov.com/)

---

## 🤝 Contributing

If you have improvements or additional templates to suggest, please:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request with your changes

---

## 📝 Template Maintenance

These templates are maintained by Garason and updated regularly to reflect best practices and new GitHub Actions features.

**Last Updated:** November 2025

---

## ❓ Troubleshooting

### Workflow not running?
- Check that the workflow file is in `.github/workflows/`
- Verify the file has `.yml` or `.yaml` extension
- Ensure the trigger branches match your branch name

### Tests failing?
- Check that your test directory exists
- Verify test dependencies are installed
- Review the workflow logs for specific errors

### Build failing?
- Ensure all dependencies are listed in `requirements.txt` or `package.json`
- Check for syntax errors in your code
- Verify the build command is correct

---

<div align="center">

**Happy CI/CD! 🚀**

</div>

