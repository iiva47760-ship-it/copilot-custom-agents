# Deployment Guide

## Overview
This guide provides step-by-step instructions for deploying GitHub Copilot Custom Agents to your organization.

## Deployment Methods

### 1. Local CLI Installation

**Installation:**
```bash
git clone https://github.com/iiva47760-ship-it/copilot-custom-agents.git
cd copilot-custom-agents
copilot agents install --config ./config/copilot-agents-config.json
```

**Usage:**
```bash
copilot @backend-api-expert "Design a REST API"
copilot @frontend-react-specialist "Optimize this component"
copilot @security-specialist "Security audit"
copilot @devops-infrastructure "Create Kubernetes deployment"
copilot @qa-automation-expert "Write E2E tests"
```

### 2. VS Code Integration

**Setup:**
1. Copy `vscode-settings.json` to `.vscode/settings.json`
2. Install GitHub Copilot extension
3. Reload VS Code

**Usage:**
```
Open Copilot Chat and use shortcuts:
- @api "your task"
- @react "your task"
- @security "your task"
- @devops "your task"
- @qa "your task"
```

### 3. GitHub Actions Integration

**Setup:**
1. Copy `deploy-agents-workflow.yml` to `.github/workflows/`
2. Push to main branch
3. Workflow validates and deploys on every push

### 4. JetBrains IDE Integration

**Installation:**
1. Install GitHub Copilot plugin
2. Copy agent configurations
3. Reload IDE

### 5. Enterprise Deployment

**For Organization-Wide Deployment:**
```bash
copilot agents publish --org <org-name> --config ./config/copilot-agents-config.json
```

## Configuration

### Environment Variables

```bash
export COPILOT_ORG=<organization-name>
export COPILOT_API_TOKEN=<api-token>
export COPILOT_AGENT_CONFIG=./config/copilot-agents-config.json
export COPILOT_DEFAULT_MODEL=claude-3-5-sonnet
export COPILOT_LOG_LEVEL=info
```

## Customization

### Modify Agent Behavior

1. Edit agent instructions
2. Update configuration in JSON
3. Test locally
4. Commit and push

### Add Custom Agents

1. Create new directory
2. Create instructions.md
3. Update config JSON
4. Deploy

## Monitoring

```bash
# Check deployment status
copilot agents status

# View usage metrics
copilot agents metrics

# Export metrics
copilot agents metrics --export metrics.csv
```

## Support

- 📖 Documentation: See docs/
- 🐛 Issues: GitHub Issues
- 💡 Discussions: GitHub Discussions