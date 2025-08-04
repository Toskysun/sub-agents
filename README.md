# Claude AI Agents Collection | Claude AI 智能代理集合

<div align="center">

[![English](https://img.shields.io/badge/Language-English-blue?style=flat-square)](#english) 
[![中文](https://img.shields.io/badge/语言-中文-red?style=flat-square)](#中文)

**A comprehensive collection of specialized AI agents for Claude Code**

*专为Claude Code设计的全面AI代理集合*

</div>

---

<div id="english">

## 🚀 Overview

This repository contains a powerful collection of specialized AI agents designed to enhance your Claude Code development experience. Each agent is crafted with deep domain expertise and **strict boundary enforcement** to handle specific technology stacks and development tasks efficiently.

## 🎯 Key Features

- **Enhanced Task Assessment**: 6-level (0-5) complexity evaluation with ultra-intelligent analysis (ultrathink mode)
- **28+ Specialized Agents**: Comprehensive coverage of modern development technologies with strict role boundaries
- **Project-Specific Agents**: `/initx` command creates custom agents tailored to your unique project requirements
- **Agent Boundary System**: ALLOWED/FORBIDDEN pattern preventing scope creep and ensuring precision
- **Dependency-Aware Execution**: Smart dependency detection with phase-based execution strategies
- **Multi-Technology Support**: Vue.js, React, Go, Rust, Python, Android, Java, Security, and more
- **Production Ready**: Battle-tested configurations optimized for real-world development
- **Performance Optimized**: 3x faster simple tasks, 2x more reliable complex coordination

## 📁 Repository Structure

```
claude-ai-agents/
├── agents/                     # AI Agent Definitions
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
├── commands/
│   ├── ai.md                   # AI team orchestration
│   └── initx.md                # Project-specific agent creation
├── CLAUDE.md                   # Core configuration
└── README.md                   # This file
```

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

## 🛠 Quick Start

### Installation

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

4. **(Optional) Create Project-Specific Agents**:
   ```bash
   # Navigate to your project directory
   cd your_project
   
   # Analyze and create custom agents for your project
   /initx
   ```

### Usage Examples

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

## 📖 Documentation

- [Agent Development Guide](docs/agent-development.md)
- [Configuration Reference](docs/configuration.md)
- [Best Practices](docs/best-practices.md)
- [Troubleshooting](docs/troubleshooting.md)

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

## 📄 License

MIT License - see [LICENSE](LICENSE) for details.

---

</div>

<div id="中文">

## 🚀 概述

这个仓库包含了一套强大的专业AI代理集合，旨在增强您的Claude Code开发体验。每个代理都具备深度领域专业知识和**严格的边界约束**，能够高效地处理特定的技术栈和开发任务。

## 🎯 核心特性

- **增强任务评估**: 6级 (0-5) 复杂度评估与超智能分析 (ultrathink模式)
- **28+个专业代理**: 全面覆盖现代开发技术栈，配备严格的角色边界
- **项目专属代理**: `/initx` 命令可创建专为您项目需求定制的自定义代理
- **代理边界系统**: ALLOWED/FORBIDDEN模式防止职责蔓延，确保精准执行
- **依赖感知执行**: 智能依赖检测与基于阶段的执行策略
- **多技术栈支持**: Vue.js、React、Go、Rust、Python、Android、Java、安全分析等
- **生产就绪**: 经过实战测试的配置，为真实世界开发优化
- **性能优化**: 简单任务3倍速度提升，复杂协调2倍可靠性提升

## 📁 仓库结构

```
claude-ai-agents/
├── agents/                     # AI代理定义
│   ├── vue-developer.md        # Vue.js/Nuxt.js专家
│   ├── react-developer.md      # React/Next.js专家
│   ├── go-architect.md         # Go微服务架构师
│   ├── rust-architect.md       # Rust系统程序员
│   ├── flask-expert.md         # Python Flask开发者
│   ├── fastapi-expert.md       # Python FastAPI专家
│   ├── google-ui-designer.md   # Material Design专家
│   ├── android-developer.md    # Android应用开发者
│   ├── mobile-ui-designer.md   # 移动端UX设计师
│   ├── java-developer.md       # Java企业级开发者
│   ├── spring-architect.md     # Spring生态系统架构师
│   ├── lua-developer.md        # Lua脚本专家
│   ├── android-hooking-expert.md # Android安全分析师
│   ├── xposed-developer.md     # Xposed模块开发者
│   ├── reverse-engineer.md     # 安全研究员
│   ├── malware-analyst.md      # 威胁情报分析师
│   ├── backend-developer.md    # API与数据库专家
│   ├── frontend-developer.md   # UI/UX开发者
│   ├── devops-engineer.md      # DevOps与部署
│   ├── code-review-expert.md   # 代码质量守护者
│   ├── test-expert.md          # 测试策略师
│   ├── task-dispatch-director.md # 中央协调器
│   └── ... (更多代理)
├── commands/
│   ├── ai.md                   # AI团队编排
│   └── initx.md                # 项目专属代理创建
├── CLAUDE.md                   # 核心配置
└── README.md                   # 本文件
```

## 🚀 项目专属代理系统 (`/initx`)

### 🎯 为您的项目创建定制AI团队

除了全局代理外，您可以使用 `/initx` 命令创建**项目专属代理**，完全针对您的具体需求进行定制。

#### 核心优势:
- **10倍开发速度**: 定制代理理解您的特定业务逻辑和技术栈
- **零学习成本**: 代理预配置了您的项目模式和约定
- **智能协作**: 代理了解您项目独特的集成点和依赖关系
- **领域专业**: 深入了解您的特定需求和约束

#### 使用方法:
```bash
/initx                    # 分析项目并创建自定义代理
/initx --preview         # 预览模式（不创建文件）
/initx --focus=security  # 创建安全专注的代理
/initx --template=mobile # 使用移动项目模板
/initx --model=inherit   # 强制所有代理使用指定模型 (inherit/sonnet/opus/haiku)
```

#### 智能代理创建:
系统分析您的项目结构并创建专业代理，例如：
- `vue-ecommerce-developer` - 电商项目专属Vue专家
- `payment-integration-specialist` - 定制支付API专家
- `postgres-inventory-architect` - 数据库专属数据架构师
- `aws-deployment-specialist` - 平台专属部署专家

#### 模型选择选项:
- **默认**: 基于代理复杂度的智能模型选择
- **--model=inherit**: 所有代理继承父会话模型（最佳成本控制）
- **--model=sonnet**: 所有代理使用Sonnet（平衡性能）
- **--model=opus**: 所有代理使用Opus（最大推理能力）
- **--model=haiku**: 所有代理使用Haiku（最快响应时间）

#### 生成的结构:
```
your_project/
├── .claude/
│   └── agents/                    # 项目专属代理
│       ├── vue-ecommerce-developer.md
│       ├── payment-integration-specialist.md
│       └── postgres-inventory-architect.md
├── CLAUDE.md                      # 更新的自定义团队配置
└── .gitignore                     # 更新的排除项
```

## 🤖 可用代理

### 🧠 分析型代理 (禁止代码执行)
*严格约束：只能分析和报告，不能执行代码或实现解决方案。*

- **technical-solution-architect**: 设计技术解决方案并创建实施路线图
- **technical-researcher**: 调研技术并提供研究报告
- **code-review-expert**: 分析代码质量并识别问题（无法修复问题）

### 💻 开发型代理 (域专属执行)
*严格约束：只能在特定技术领域内执行代码。*

#### 前端专家
- **vue-developer**: Vue.js 3、组合式API、Nuxt.js、Pinia（仅Vue生态系统）
- **react-developer**: React 18、Next.js、Redux Toolkit、Server Components（仅React生态系统）
- **frontend-developer**: 通用前端开发和UI框架

#### 后端专家
- **backend-developer**: 多栈API开发（FastAPI/Spring Boot/Node.js）- 仅服务端
- **go-architect**: Go微服务、分布式系统、云原生
- **rust-architect**: 系统编程、性能优化、内存安全
- **flask-expert**: Python Flask Web应用和REST API
- **fastapi-expert**: 异步Python API、自动文档生成
- **java-developer**: 企业级Java开发和Spring Boot
- **spring-architect**: Spring生态系统、微服务架构

#### 移动端与设计
- **android-developer**: 原生Android应用、Kotlin、架构组件
- **mobile-ui-designer**: 移动端UX/UI、响应式设计、平台指南
- **google-ui-designer**: Material Design 3、无障碍性、设计系统

#### 基础设施与DevOps
- **devops-engineer**: Docker容器化和部署（仅基础设施）
- **infrastructure-developer**: 构建工具、CI/CD管道、自动化脚本

### 🔐 安全与分析专家
- **android-hooking-expert**: Frida、动态分析、运行时操控
- **xposed-developer**: Xposed模块、系统级修改
- **reverse-engineer**: 静态分析、反编译、漏洞研究
- **malware-analyst**: 威胁检测、行为分析、事件响应

### 🌙 自动化与脚本
- **lua-developer**: 游戏脚本、自动化、OpenResty Web开发

### 🔧 质量型代理 (分析和指导)
*严格约束：提供指导和协调但不能实现解决方案。*

- **qa-engineer**: 测试策略和质量分析（无法编写生产代码）
- **test-expert**: 测试框架设计和策略（无法实现业务逻辑）
- **task-dispatch-director**: 纯粹协调（⚠️ 绝不调用自身）

## 🛠 快速开始

### 安装

1. **克隆仓库**:
   ```bash
   git clone https://github.com/Toskysun/sub-agents.git
   cd sub-agents
   ```

2. **复制到Claude Code目录**:
   ```bash
   # Linux/Mac
   cp -r * ~/.claude/
   
   # Windows
   copy * %USERPROFILE%\.claude\
   ```

3. **重启Claude Code**或重新加载配置

4. **（可选）创建项目专属代理**:
   ```bash
   # 导航到您的项目目录
   cd your_project
   
   # 分析并为您的项目创建自定义代理
   /initx
   ```

### 使用示例

**全局代理任务**（随时可用）:
```
/ai "创建一个Vue.js仪表板组件"
/ai "构建一个FastAPI认证服务"
/ai "设计一个Material Design移动界面"
/ai "优化Go微服务性能"
```

**项目专属代理任务**（运行 `/initx` 后）:
```
/ai "优化结账流程"           # 使用 vue-ecommerce-developer
/ai "实现支付网关"           # 使用 payment-integration-specialist
/ai "添加库存警报"           # 使用 postgres-inventory-architect
/ai "部署到生产环境"         # 使用 aws-deployment-specialist
```

**多代理协调**:
```
/ai "构建一个全栈电商平台"
/ai "创建一个带测试的React组件库"
/ai "开发一个带API集成的安全Android应用"
```

**团队管理**:
```
/ai list          # 显示所有可用代理（全局+项目）
/ai info react    # 获取React专家详情
/initx --preview  # 预览您项目的自定义代理
```

## 📋 任务复杂度级别 

| 级别 | 类型 | 描述 | 处理方式 | 性能优势 |
|------|------|------|----------|----------|
| **Level 0** | 微任务 | 信息查询、文件读取 | 直接执行 | 即时响应 |
| **Level 1** | 简单 | 单文件更改、基础配置 | 单代理直接 | 3倍速度路由 |
| **Level 2** | 中等 | 组件开发、功能模块 | 单代理复杂 | 全流程处理 |
| **Level 3** | 复合 | 多模块协调、2-3个领域 | 串行多代理 | 上下文传递 |
| **Level 4** | 并行 | 独立模块、性能优化 | 并发执行 | 4倍速度潜力 |
| **Level 5** | 企业级 | 系统重构、架构设计 | Director协调 | 复杂编排 |

## 🚀 高级特性

### 🎯 代理边界系统
- **ALLOWED/FORBIDDEN模式**: 明确约束防止职责蔓延
- **域专属执行**: 代理只在其专业领域内工作  
- **委托要求**: 任务超出边界时强制交接
- **反过度工程**: 防止不必要的多代理调用

### 📊 依赖感知执行
- **智能依赖分析**: 自动检测任务先决条件
- **基于阶段的执行**: 依赖任务串行执行，独立任务并行执行
- **上下文交接**: 执行阶段间的适当信息流
- **选择性并行**: 在保证安全的前提下最大化速度提升

### ⚡ 性能优化
- **Level 0-5 任务分类**: 从微任务到企业级协调的精准路由
- **简单任务3倍速度提升**: 直接执行绕过不必要的开销
- **复杂协调2倍可靠性**: 适当的依赖管理
- **自动回退**: 3次重试系统配合智能代理重新分配

### 🛡️ 质量与安全
- **反死锁保护**: task-dispatch-director限制为纯粹协调
- **质量门禁**: 内置代码审查和测试工作流
- **TodoWrite策略**: 级别适当的任务跟踪和管理
- **边界执行**: 严格的代理角色合规性与违规检测

## 📖 文档

- [代理开发指南](docs/agent-development.md)
- [配置参考](docs/configuration.md)
- [最佳实践](docs/best-practices.md)
- [故障排除](docs/troubleshooting.md)

## 🤝 贡献

我们欢迎贡献！请查看我们的[贡献指南](CONTRIBUTING.md)了解详情。

## 📄 许可证

MIT许可证 - 详见[LICENSE](LICENSE)文件。

</div>

---

<div align="center">

**Made with ❤️ for the Claude Code community**

[![GitHub Stars](https://img.shields.io/github/stars/Toskysun/sub-agents?style=social)](https://github.com/Toskysun/sub-agents)
[![GitHub Forks](https://img.shields.io/github/forks/Toskysun/sub-agents?style=social)](https://github.com/Toskysun/sub-agents)

</div>