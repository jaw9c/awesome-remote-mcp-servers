# Contributing to Awesome Remote MCP Servers

Thank you for your interest in contributing to Awesome Remote MCP Servers! This is a curated, opinionated list focused on high-quality, official MCP servers. This document provides guidelines and instructions for contributing to this repository.

## Quality Standards

Before submitting a server for inclusion, please ensure it meets these criteria:

- **Official Support**: The server must be officially supported by its maintainers
- **Production Ready**: Must be stable and suitable for production use
- **Active Maintenance**: Regular updates and bug fixes
- **Security**: Proper authentication and security measures, with OAuth 2.0 support preferred
- **Reliability**: Proven track record of uptime and performance
- **Community**: Active user community and support channels

## How to Contribute

### 1. Fork the Repository

First, fork this repository to your GitHub account.

### 2. Add Your Remote MCP Server

Add your remote MCP server to the table in the README.md file. Each entry should follow this format:

```markdown
| Server Name | Category | URL | Authentication | Maintainer |
|------------|----------|-----|----------------|------------|
| Your Server | Category | `https://your-server-url` | OAuth | [Your Organization](https://your-org-url) |
```

Required information:
- **Server Name**: The name of your MCP server
- **Category**: One of the following:
  - Language Models
  - Software Development
  - RAG-as-a-Service
  - Payments
  - Data Analysis
  - Other
- **URL**: The complete URL to access your MCP server
- **Authentication**: Must be OAuth 2.0, following the MCP spec
- **Maintainer**: The official maintainer or organization with a link to their website

### 3. Additional Requirements

Please ensure your contribution includes:

- Link to official GitHub repository or website
- Evidence of active maintenance (e.g., recent commits, releases)
- Documentation of security measures
- Information about the support channels
- Any relevant benchmarks or performance metrics
- Production deployment examples (if available)

### 4. Submit a Pull Request

1. Create a new branch for your changes
2. Make your changes
3. Submit a pull request with a clear description of:
   - Why the server meets our quality criteria
   - How it's being used in production
   - Any notable features or benefits

## Code of Conduct

By participating in this project, you agree to abide by the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md).

## Questions?

If you have any questions about contributing, please open an issue in the repository. 