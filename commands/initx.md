# InitX - Project Intelligence & Agent Recruitment System

## Usage
`/initx [OPTIONS]`

## 🎯 Core Function

Analyze project codebase, detect technology stack, and **CREATE NEW PROJECT-SPECIFIC AGENTS** tailored to your unique requirements. Saves custom agents to `.claude/agents/` and updates project `CLAUDE.md`.

## 🚀 Command Modes

### 🎯 Basic Usage
```bash
/initx                    # Smart analysis & agent creation
/initx --preview         # Preview mode (no file creation)
/initx --force          # Force overwrite existing agents
```

### 📊 Advanced Options
- `--mode=minimal`     - Create only essential agents
- `--focus=security`   - Focus on security-specific agents  
- `--exclude=ui`       - Skip UI/design agents
- `--template=mobile`  - Use mobile project template
- `--model=inherit`    - Force all agents to use specified model (inherit/sonnet/opus/haiku)

## 🧠 Intelligence Detection Matrix

### Technology Stack Recognition
```yaml
Frontend: vue (*.vue, nuxt.config.js), react (*.jsx, next.config.js), angular
Backend: fastapi (main.py), spring (pom.xml), go (go.mod), node (express/koa)
Mobile: android (*.kt, AndroidManifest.xml), flutter (pubspec.yaml)
Security: reversing (*.apk, frida scripts), hooking (xposed modules)
```

### Project Complexity Assessment
- **Simple**: 1-2 custom agents (single stack)
- **Medium**: 3-5 custom agents (multi-stack)  
- **Complex**: 5-8 custom agents (microservices)
- **Enterprise**: 8+ custom agents (distributed)

## 🤖 Agent Creation Algorithm

### Phase 1: Core Stack Agents
**Creates NEW specialized agents based on detected stack:**
- `vue-{project-name}-developer` - Project-specific Vue expert
- `api-{domain}-specialist` - Custom API integration expert
- `{database}-data-architect` - Database-specific data expert

### Phase 2: Domain-Specific Agents  
**Creates NEW agents for unique project domains:**
- `{domain}-business-logic-expert` - Business rules specialist
- `{integration}-connector-agent` - Third-party integration expert
- `{platform}-deployment-specialist` - Platform-specific deployment

### Phase 3: Quality & Operations Agents
**Creates NEW agents for project-specific QA:**
- `{stack}-testing-specialist` - Stack-specific testing expert
- `{environment}-ops-engineer` - Environment-specific operations

## 📁 Generated Structure

```
project_root/
├── .claude/
│   └── agents/                    # NEW custom agents
│       ├── vue-ecommerce-developer.md
│       ├── payment-integration-specialist.md
│       ├── postgres-data-architect.md
│       └── aws-deployment-specialist.md
├── CLAUDE.md                      # Updated with new team
└── .gitignore                     # Updated exclusions
```

## 🏗️ Custom Agent Template

⚠️ **LANGUAGE REQUIREMENT**: All agent content MUST be generated in ENGLISH.

```markdown
---
name: {project-domain}-{specialization}-agent
description: Project-specific {specialization} expert for {project_name}
model: inherit  # Options: inherit | sonnet | opus | haiku
---

You are the **{Project Domain} {Specialization} Agent** for the {project_name} project.

## STRICT AGENT BOUNDARIES

**ALLOWED ACTIONS:**
- {Domain-specific actions based on project analysis}
- {Tech stack specific implementations}
- {Integration and performance optimizations}

**FORBIDDEN ACTIONS:**
- {Cross-domain work} (delegate to {appropriate_agent})
- Infrastructure concerns (delegate to devops-engineer)
- Security audits (delegate to code-review-expert)

**CORE MISSION:** {Single sentence describing the agent's purpose}

## RESPONSIBILITIES

### 1. {Primary Domain Area}
- {Specific responsibilities based on project analysis}
- {Pattern implementations from detected codebase}

### 2. {Quality & Testing}
- {Testing requirements specific to domain}
- {Performance criteria for project}

### 3. {Collaboration}
- Input from: {upstream agents}
- Output to: {downstream agents}
- Coordinate with: {peer agents}

## TECHNOLOGY STACK
**Primary**: {Detected technologies with versions}
**Integrations**: {Third-party services}
**Constraints**: Work exclusively within {project_domain} of {project_name}
```

## 🧠 Intelligent Model Selection System

### Model Selection Matrix
```yaml
Complex Reasoning (opus): Architecture design, security analysis, microservices
Balanced Performance (sonnet): Most development agents, API/database, testing
Simple Fast (haiku): Config generation, simple scripts, documentation
Inherit from Parent (inherit): Maintain consistency, avoid switching overhead
```

### Force Model Option (--model parameter)
```bash
/initx --model=inherit    # All agents inherit from parent (best for cost control)
/initx --model=sonnet     # All agents use Sonnet (balanced performance)
/initx --model=opus       # All agents use Opus (maximum reasoning) 
/initx --model=haiku      # All agents use Haiku (fastest response)
```

⚠️ Using `--model` overrides intelligent model selection for consistency/cost control.

### User Confirmation Flow

#### Standard Mode (Intelligent Model Selection)
```bash
🤖 Agent Creation - {agent_name}
📊 Recommended: {suggested_model} ({reason})

Select model: [1] ✅ Recommended [2] Opus [3] Sonnet [4] Haiku [5] Inherit
Confirm? [y/N]
```

#### Force Model Mode (--model parameter)
```bash
🤖 Agent Creation - {agent_name}
📊 Model: {forced_model} (forced by --model)
Confirm? [y/N]
```

### ⚠️ IMPORTANT: Language Requirements
**All generated agents MUST be created in English**, regardless of the user's input language:
- Agent names: Always in English (e.g., `vue-ecommerce-developer`, not `vue-电商-开发者`)
- Agent descriptions: Always in English
- Agent content: Always in English
- Documentation comments: Always in English

This ensures consistency and compatibility across all projects and teams.

## ⚡ Execution Flow

### Phase 1: Project Intelligence (15s)
```bash
🔍 Analyzing project structure...
├── 📊 Detecting tech stack and versions
├── 🏗️ Identifying architecture patterns  
├── 📈 Assessing complexity and scale
└── 🎯 Discovering unique requirements

✅ Analysis Complete
- Type: E-commerce Web App
- Stack: Vue 3 + FastAPI + PostgreSQL
- Complexity: Medium (4/5)  
- Unique: Payment integration, inventory management
```

### Phase 2: Agent Creation & Confirmation (20s)

#### Standard Mode:
```bash
🤖 Intelligent Model Matching...

vue-ecommerce-developer (recommended: sonnet)
├─ Reason: Vue 3 patterns, balanced performance
├─ Select: [1] ✅ sonnet [2] opus [3] haiku [4] inherit
└─ ✅ Created

fastapi-payment-specialist (recommended: opus)
├─ Reason: Payment integration, complex logic
├─ Select: [1] ✅ opus [2] sonnet [3] haiku [4] inherit
└─ ✅ Created

[... more agents ...]

📊 Created 8 agents: 4 sonnet, 2 opus, 1 haiku, 1 inherit
```

#### Force Model Mode (/initx --model=inherit):
```bash
🤖 Force Model: inherit (all agents use parent model)

vue-ecommerce-developer
├─ ⚠️ Using inherit (recommended: sonnet)
└─ ✅ Created

fastapi-payment-specialist  
├─ ⚠️ Using inherit (recommended: opus)
└─ ✅ Created

[... more agents ...]

📊 Created 8 agents: 8 inherit (forced)
```

### Phase 3: Team Configuration (10s)
```bash
📝 Configuring AI team collaboration...
├── 📁 Saving agents to .claude/agents/ directory
├── 🔧 Setting up collaboration matrix and dependencies
├── 📋 Updating CLAUDE.md with team information
└── 🎯 Ready for project-specific task execution

✅ Custom AI team ready!
🚀 Use /ai "optimize checkout flow" to engage specialist team
```

## 🎛️ Smart Templates

### E-commerce Project
```yaml
detected_patterns: [shopping_cart, payment_flow, inventory]
created_agents:
  - payment-integration-specialist
  - inventory-management-expert  
  - customer-analytics-agent
  - ecommerce-testing-specialist
```

### Security Research Project  
```yaml
detected_patterns: [apk_analysis, hooking, reverse_engineering]
created_agents:
  - android-malware-analyst
  - frida-hooking-specialist
  - apk-reverse-engineer
  - vulnerability-scanner-expert
```

### Microservices Project
```yaml
detected_patterns: [service_mesh, api_gateway, distributed_data]
created_agents:
  - service-mesh-architect
  - api-gateway-specialist
  - distributed-data-expert
  - microservices-testing-specialist
```

## 🚀 System Benefits

### 🎯 **Project-Specific Intelligence**
- **Custom Agents**: Tailored to your exact tech stack and domain
- **Smart Collaboration**: Agents know your project's integration points
- **Model Flexibility**: Choose optimal model strategy with `--model` parameter

### ⚡ **Rapid Development**
- **10x Faster**: Custom experts vs generic agents  
- **Zero Learning Curve**: Agents pre-configured for your project
- **Cost Control**: Force consistent model usage with `--model=inherit`

### 💰 **Cost Management**
- **Default**: Intelligent per-agent model selection
- **--model=inherit**: Maximum cost control
- **--model=sonnet**: Balanced cost/performance
- **--model=haiku**: Minimum cost, fast response

---

**InitX creates your perfect AI development team - not just assigns existing ones!**  
🚀 One command, custom specialists, exponential productivity!