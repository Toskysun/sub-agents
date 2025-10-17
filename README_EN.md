<div align="center">

# Claude AI Agents Collection

[![English](https://img.shields.io/badge/Language-English-blue?style=flat-square)](README_EN.md)
[![中文](https://img.shields.io/badge/语言-中文-red?style=flat-square)](README.md)

**A comprehensive collection of specialized AI agents for Claude Code**

[![GitHub Stars](https://img.shields.io/github/stars/Toskysun/sub-agents?style=social)](https://github.com/Toskysun/sub-agents)
[![GitHub Forks](https://img.shields.io/github/forks/Toskysun/sub-agents?style=social)](https://github.com/Toskysun/sub-agents)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

</div>

---

## 🚀 Overview

This repository contains a powerful collection of specialized AI agents designed to enhance your Claude Code development experience. Each agent is crafted with deep domain expertise and **strict boundary enforcement** to handle specific technology stacks and development tasks efficiently.

## 🎯 Key Features

- **Claude Code Plugin System**: Fully integrated with Claude Code's official plugin architecture
- **Easy Installation**: Install via `/plugin` commands or manual copy to `~/.claude/`
- **Enhanced Task Assessment**: 6-level (0-5) complexity evaluation with ultra-intelligent analysis (ultrathink mode)
- **28+ Specialized Agents**: Comprehensive coverage of modern development technologies with strict role boundaries
- **Project-Specific Agents**: `/initx` command creates custom agents tailored to your unique project requirements
- **Agent Boundary System**: ALLOWED/FORBIDDEN pattern preventing scope creep and ensuring precision
- **Dependency-Aware Execution**: Smart dependency detection with phase-based execution strategies
- **Multi-Technology Support**: Vue.js, React, Go, Rust, Python, Android, Java, Security, and more
- **Production Ready**: Battle-tested configurations optimized for real-world development
- **Performance Optimized**: 3x faster simple tasks, 2x more reliable complex coordination

## 🛠 Quick Start

### Installation

You can install this collection in two ways:

- **Plugin Installation**: More convenient, but longer commands (e.g., `/universal:ai`)
- **Manual Installation** (Recommended): Requires manual file copying, but simpler commands (e.g., `/ai`)

#### Method 1: Plugin Installation

1. **Add the marketplace** to Claude Code:
   ```bash
   claude
   ```

   ```shell
   /plugin marketplace add Toskysun/sub-agents
   ```

2. **Install the plugin**:
   ```shell
   /plugin install universal@sub-agents
   ```

3. **Restart Claude Code** to activate the agents

4. **Verify installation**:
   ```shell
   /universal:ai list
   /universal:initx --preview
   /help
   ```

   💡 **Tip**: After plugin installation, commands require the namespace prefix `/universal:`. If you prefer simpler commands like `/ai` and `/initx`, we recommend **Method 2: Manual Installation**.

5. **(Optional) Install CLAUDE.md configuration**:

   ⚠️ **Note**: The plugin system cannot automatically install `CLAUDE.md`. You need to manually copy it:

   ```bash
   # For global configuration (recommended)
   curl -o ~/.claude/CLAUDE.md https://raw.githubusercontent.com/Toskysun/sub-agents/master/CLAUDE.md

   # OR for project-specific configuration
   curl -o ./CLAUDE.md https://raw.githubusercontent.com/Toskysun/sub-agents/master/CLAUDE.md
   ```

#### Method 2: Manual Installation (Recommended)

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Toskysun/sub-agents.git
   cd sub-agents
   ```

2. **Copy to Claude Code directory**:
   ```bash
   # Linux/Mac
   cp -r * ~/.claude/

   # Windows
   copy * %USERPROFILE%\.claude\
   ```

3. **Restart Claude Code** or reload configuration

#### Create Project-Specific Agents (Optional)

After installation, you can create custom agents for your specific project:

```bash
# Navigate to your project directory
cd your_project

# Analyze and create custom agents for your project
/initx
```

### Usage Examples

💡 **Note**: Examples below use simplified command format (manual installation). If using plugin installation, replace `/ai` with `/universal:ai` and `/initx` with `/universal:initx`.

**Global Agent Tasks** (Available everywhere):
```
/ai "Create a Vue.js dashboard component"
/ai "Build a FastAPI authentication service"
/ai "Design a Material Design mobile interface"
/ai "Optimize Go microservice performance"
```

**Project-Specific Agent Tasks** (After running `/initx`):
```
/ai "optimize checkout flow"      # Uses vue-ecommerce-developer
/ai "implement payment gateway"   # Uses payment-integration-specialist
/ai "add inventory alerts"        # Uses postgres-inventory-architect
/ai "deploy to production"        # Uses aws-deployment-specialist
```

**Multi-Agent Coordination**:
```
/ai "Build a full-stack e-commerce platform"
/ai "Create a React component library with testing"
/ai "Develop a secure Android app with API integration"
```

**Team Management**:
```
/ai list          # Show all available agents (global + project)
/ai info react    # Get React specialist details
/initx --preview  # Preview custom agents for your project
```

## 🤖 Available Agents

### 🧠 Analysis Agents (NO CODE EXECUTION)
*Strict Constraints: Analyze and report only. Cannot execute code or implement solutions.*

- **technical-solution-architect**: Designs technical solutions and creates implementation roadmaps
- **technical-researcher**: Investigates technologies and provides research reports
- **code-review-expert**: Analyzes code quality and identifies issues (cannot fix problems)

### 💻 Development Agents (DOMAIN-SPECIFIC EXECUTION)
*Strict Constraints: Execute code only within specific technology domains.*

#### Frontend Specialists
- **vue-developer**: Vue.js 3, Composition API, Nuxt.js, Pinia (Vue ecosystem only)
- **react-developer**: React 18, Next.js, Redux Toolkit, Server Components (React ecosystem only)
- **frontend-developer**: General frontend development and UI frameworks

#### Backend Specialists
- **backend-developer**: Multi-stack API development (FastAPI/Spring Boot/Node.js) - server-side only
- **go-architect**: Go microservices, distributed systems, cloud-native
- **rust-architect**: Systems programming, performance optimization, memory safety
- **flask-expert**: Python Flask web applications and REST APIs
- **fastapi-expert**: Async Python APIs, automatic documentation
- **java-developer**: Enterprise Java development and Spring Boot
- **spring-architect**: Spring ecosystem, microservices architecture

#### Mobile & Design
- **android-developer**: Native Android apps, Kotlin, Architecture Components
- **mobile-ui-designer**: Mobile UX/UI, responsive design, platform guidelines
- **google-ui-designer**: Material Design 3, Accessibility, Design Systems

#### Infrastructure & DevOps
- **devops-engineer**: Docker containerization and deployment (infrastructure only)
- **infrastructure-developer**: Build tools, CI/CD pipelines, automation scripts

### 🔐 Security & Analysis Specialists
- **android-hooking-expert**: Frida, dynamic analysis, runtime manipulation
- **xposed-developer**: Xposed modules, system-level modifications
- **reverse-engineer**: Static analysis, decompilation, vulnerability research
- **malware-analyst**: Threat detection, behavioral analysis, incident response

### 🌙 Automation & Scripting
- **lua-developer**: Game scripting, automation, OpenResty web development

### 🔧 Quality Agents (ANALYSIS AND GUIDANCE)
*Strict Constraints: Provide guidance and coordination but cannot implement solutions.*

- **qa-engineer**: Testing strategy and quality analysis (cannot write production code)
- **test-expert**: Testing framework design and strategy (cannot implement business logic)
- **task-dispatch-director**: Pure coordination only (⚠️ Never calls itself)

## 🚀 Project-Specific Agent System (`/initx`)

### 🎯 Create Custom AI Teams for Your Project

Beyond the global agents, you can create **project-specific agents** tailored to your exact requirements using the `/initx` command.

#### Key Benefits:
- **10x Faster Development**: Custom agents understand your specific business logic and tech stack
- **Zero Learning Curve**: Agents pre-configured with your project patterns and conventions
- **Smart Collaboration**: Agents know your project's unique integration points and dependencies
- **Domain Expertise**: Deep knowledge of your specific requirements and constraints

#### Usage:
```bash
/initx                    # Analyze project and create custom agents
/initx --preview         # Preview mode (no file creation)
/initx --focus=security  # Create security-focused agents
/initx --template=mobile # Use mobile project template
/initx --model=inherit   # Force all agents to use specific model (inherit/sonnet/opus/haiku)
```

#### Intelligent Agent Creation:
The system analyzes your project structure and creates specialized agents like:
- `vue-ecommerce-developer` - Project-specific Vue expert for e-commerce
- `payment-integration-specialist` - Custom payment API expert
- `postgres-inventory-architect` - Database-specific data architect
- `aws-deployment-specialist` - Platform-specific deployment expert

#### Model Selection Options:
- **Default**: Intelligent model selection based on agent complexity
- **--model=inherit**: All agents inherit parent session model (best for cost control)
- **--model=sonnet**: All agents use Sonnet (balanced performance)
- **--model=opus**: All agents use Opus (maximum reasoning capability)
- **--model=haiku**: All agents use Haiku (fastest response time)

#### Generated Structure:
```
your_project/
├── .claude/
│   └── agents/                    # Project-specific agents
│       ├── vue-ecommerce-developer.md
│       ├── payment-integration-specialist.md
│       └── postgres-inventory-architect.md
├── CLAUDE.md                      # Updated with custom team
└── .gitignore                     # Updated exclusions
```

## 📋 Task Complexity Levels

| Level | Type | Description | Handling | Performance |
|-------|------|-------------|----------|-------------|
| **Level 0** | Micro | Information queries, file reading | Direct execution | Instant response |
| **Level 1** | Simple | Single file changes, basic configs | Single agent direct | 3x faster routing |
| **Level 2** | Medium | Component development, feature modules | Single agent complex | Full process handling |
| **Level 3** | Composite | Multi-module coordination, 2-3 domains | Serial multi-agent | Context handoffs |
| **Level 4** | Parallel | Independent modules, performance optimization | Concurrent execution | 4x speedup potential |
| **Level 5** | Enterprise | System refactoring, architecture design | Director coordination | Complex orchestration |

## 🚀 Advanced Features

### 🎯 Agent Boundary System
- **ALLOWED/FORBIDDEN Pattern**: Explicit constraints preventing scope creep
- **Domain-Specific Execution**: Agents work only within their expertise areas
- **Delegation Requirements**: Mandatory handoffs when tasks exceed boundaries
- **Anti-Over-Engineering**: Prevents unnecessary multi-agent invocations

### 📊 Dependency-Aware Execution
- **Smart Dependency Analysis**: Automatic detection of task prerequisites
- **Phase-Based Execution**: Serial execution for dependent tasks, parallel for independent
- **Context Handoffs**: Proper information flow between execution phases
- **Selective Parallelism**: Maximum speedup while maintaining safety

### ⚡ Performance Optimization
- **Level 0-5 Task Classification**: Precision routing from micro-tasks to enterprise coordination
- **3x faster simple tasks**: Direct execution bypasses unnecessary overhead
- **2x more reliable complex coordination**: Proper dependency management
- **Automatic Fallback**: 3-retry system with intelligent agent reassignment

### 🛡️ Quality & Safety
- **Anti-Deadlock Protection**: task-dispatch-director limited to pure coordination
- **Quality Gates**: Built-in code review and testing workflows
- **TodoWrite Strategy**: Level-appropriate task tracking and management
- **Boundary Enforcement**: Strict agent role compliance with violation detection

## 📁 Repository Structure

```
sub-agents/
├── .claude-plugin/             # Plugin System Configuration
│   ├── plugin.json            # Plugin manifest
│   └── marketplace.json       # Marketplace definition
├── agents/                     # AI Agent Definitions (28+ agents)
│   ├── vue-developer.md        # Vue.js/Nuxt.js specialist
│   ├── react-developer.md      # React/Next.js expert
│   ├── go-architect.md         # Go microservices architect
│   ├── rust-architect.md       # Rust systems programmer
│   ├── flask-expert.md         # Python Flask developer
│   ├── fastapi-expert.md       # Python FastAPI specialist
│   ├── google-ui-designer.md   # Material Design expert
│   ├── android-developer.md    # Android app developer
│   ├── mobile-ui-designer.md   # Mobile UX designer
│   ├── java-developer.md       # Java enterprise developer
│   ├── spring-architect.md     # Spring ecosystem architect
│   ├── lua-developer.md        # Lua scripting expert
│   ├── android-hooking-expert.md # Android security analyst
│   ├── xposed-developer.md     # Xposed module developer
│   ├── reverse-engineer.md     # Security researcher
│   ├── malware-analyst.md      # Threat intelligence analyst
│   ├── backend-developer.md    # API & database expert
│   ├── frontend-developer.md   # UI/UX developer
│   ├── devops-engineer.md      # DevOps & deployment
│   ├── code-review-expert.md   # Code quality guardian
│   ├── test-expert.md          # Testing strategist
│   ├── task-dispatch-director.md # Central coordinator
│   └── ... (more agents)
├── commands/                   # Custom Slash Commands
│   ├── ai.md                   # AI team orchestration
│   └── initx.md                # Project-specific agent creation
├── CLAUDE.md                   # Core configuration
├── LICENSE                     # MIT License
└── README.md                   # This file
```

## 📄 License

MIT License - see [LICENSE](LICENSE) for details.

---

<div align="center">

### 💝 Acknowledgments

Crafted with ❤️ by **[Toskysun](https://github.com/Toskysun)**

If this project helps you, please give it a ⭐ Star to show your support!

</div>
