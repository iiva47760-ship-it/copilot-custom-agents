# Quick Start Guide - GitHub Copilot Custom Agents

## 5-Minute Setup

### Step 1: Download Agents
```bash
# Clone the repository
git clone https://github.com/iiva47760-ship-it/copilot-custom-agents.git
cd copilot-custom-agents
```

### Step 2: Choose Your Deployment Method

#### **Option A: VS Code (Easiest)**
```bash
# Copy settings to your workspace
cp vscode-settings.json .vscode/settings.json

# Restart VS Code
# Open Copilot Chat → Start using @api, @react, @security, etc.
```

#### **Option B: CLI (Most Powerful)**
```bash
# Install agents
copilot agents install --config ./config/copilot-agents-config.json

# Use any time
copilot @backend-api-expert "Design REST API for todo app"
```

#### **Option C: GitHub Actions (Enterprise)**
```bash
# Copy workflow to your repo
cp deploy-agents-workflow.yml .github/workflows/

# Push to main branch
git push origin main

# Agents auto-deploy on commit
```

### Step 3: Start Using Agents

**Your 5 Agents Are Ready:**

1. **@api** - Backend API Expert
   ```bash
   copilot @backend-api-expert "Design a user authentication API"
   ```

2. **@react** - Frontend React Specialist
   ```bash
   copilot @frontend-react-specialist "Optimize this component"
   ```

3. **@security** - Security Specialist
   ```bash
   copilot @security-specialist "Review for vulnerabilities"
   ```

4. **@devops** - DevOps Infrastructure
   ```bash
   copilot @devops-infrastructure "Create Docker setup"
   ```

5. **@qa** - QA Automation Expert
   ```bash
   copilot @qa-automation-expert "Write E2E tests"
   ```

## Common Use Cases

### 🚀 Starting a New Project
```bash
# Get architectural guidance
copilot @backend-api-expert "Design API for e-commerce platform"
copilot @frontend-react-specialist "Structure React component hierarchy"
copilot @devops-infrastructure "Set up deployment pipeline"
```

### 🔍 Code Review
```bash
# Review for different aspects
copilot @backend-api-expert "Review this API endpoint"
copilot @security-specialist "Security audit of these files"
copilot @qa-automation-expert "Check test coverage"
```

### 🐛 Debugging
```bash
copilot @backend-api-expert "Why is this endpoint slow?"
copilot @frontend-react-specialist "Why does this component re-render?"
copilot @security-specialist "Is this a security issue?"
```

## VS Code Integration

### Quick Chat Commands

| Command | Agent | Use Case |
|---------|-------|----------|
| `@api` | Backend Expert | API design & review |
| `@react` | React Specialist | React components & patterns |
| `@security` | Security Specialist | Vulnerability & compliance |
| `@devops` | DevOps Infrastructure | Deployment & infrastructure |
| `@qa` | QA Expert | Testing & quality assurance |

### Using with Files

```
1. Open a code file
2. Select code snippet (Cmd/Ctrl + L)
3. Open Copilot Chat (Cmd/Ctrl + K)
4. Type: @api "Review this endpoint"
5. Get context-aware guidance
```

## CLI Commands Cheatsheet

```bash
# List available agents
copilot agents list

# Get agent info
copilot agents info backend-api-expert

# Use an agent
copilot @backend-api-expert "Your question here"

# Get help
copilot agents help
copilot @agent-name --help

# View agent capabilities
copilot agents capabilities backend-api-expert
```

## Troubleshooting

### Agents Not Available

```bash
# Verify installation
copilot agents status

# Reinstall if needed
copilot agents uninstall
copilot agents install --config ./config/copilot-agents-config.json

# Restart VS Code
```

### Wrong Responses

```bash
# Check agent instructions
cat config/agent-backend-api-expert/instructions.md

# Provide more context in your question
# ❌ "Review my code"
# ✅ "Review my Express.js API endpoint for performance and security"
```

## Full Documentation

- 📖 **docs/DEPLOYMENT.md** - Detailed setup for all methods
- 📚 **docs/USAGE-EXAMPLES.md** - Advanced examples and patterns
- 🎯 **docs/agents-index.md** - All agents and capabilities

## Next Steps

1. ✅ Choose deployment method above
2. ✅ Follow 5-minute setup
3. ✅ Try example queries
4. ✅ Customize for your needs
5. ✅ Share with your team

---

**You're all set!** Start asking questions and let our agents help you build better software.