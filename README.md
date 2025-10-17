<div align="center">

# Claude AI 智能代理集合

[![中文](https://img.shields.io/badge/语言-中文-red?style=flat-square)](README.md)
[![English](https://img.shields.io/badge/Language-English-blue?style=flat-square)](README_EN.md)

**专为Claude Code设计的全面AI代理集合**

[![GitHub Stars](https://img.shields.io/github/stars/Toskysun/sub-agents?style=social)](https://github.com/Toskysun/sub-agents)
[![GitHub Forks](https://img.shields.io/github/forks/Toskysun/sub-agents?style=social)](https://github.com/Toskysun/sub-agents)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

</div>

---

## 🚀 概述

这个仓库包含了一套强大的专业AI代理集合，旨在增强您的Claude Code开发体验。每个代理都具备深度领域专业知识和**严格的边界约束**，能够高效地处理特定的技术栈和开发任务。

## 🎯 核心特性

- **Claude Code插件系统**: 完全集成Claude Code官方插件架构
- **简易安装**: 通过 `/plugin` 命令安装或手动复制到 `~/.claude/`
- **增强任务评估**: 6级 (0-5) 复杂度评估与超智能分析 (ultrathink模式)
- **28+个专业代理**: 全面覆盖现代开发技术栈，配备严格的角色边界
- **项目专属代理**: `/initx` 命令可创建专为您项目需求定制的自定义代理
- **代理边界系统**: ALLOWED/FORBIDDEN模式防止职责蔓延，确保精准执行
- **依赖感知执行**: 智能依赖检测与基于阶段的执行策略
- **多技术栈支持**: Vue.js、React、Go、Rust、Python、Android、Java、安全分析等
- **生产就绪**: 经过实战测试的配置，为真实世界开发优化
- **性能优化**: 简单任务3倍速度提升，复杂协调2倍可靠性提升

## 🛠 快速开始

### 安装

您可以通过两种方式安装此集合：

- **插件安装**：更方便，但命令较长（如 `/universal:ai`）
- **手动安装**（推荐）：需要手动复制文件，但命令简洁（如 `/ai`）

#### 方法1: 插件安装

1. **添加marketplace到Claude Code**:
   ```bash
   claude
   ```

   ```shell
   /plugin marketplace add Toskysun/sub-agents
   ```

2. **安装插件**:
   ```shell
   /plugin install universal@sub-agents
   ```

3. **重启Claude Code**以激活代理

4. **验证安装**:
   ```shell
   /universal:ai list
   /universal:initx --preview
   /help
   ```

   💡 **提示**: 插件安装后命令需要加命名空间前缀 `/universal:`。如果您希望使用更简洁的 `/ai` 和 `/initx` 命令，建议使用**方法2: 手动安装**。

5. **（可选）安装CLAUDE.md配置**:

   ⚠️ **注意**: 插件系统无法自动安装 `CLAUDE.md`，您需要手动复制：

   ```bash
   # 全局配置（推荐）
   curl -o ~/.claude/CLAUDE.md https://raw.githubusercontent.com/Toskysun/sub-agents/master/CLAUDE.md

   # 或者项目专属配置
   curl -o ./CLAUDE.md https://raw.githubusercontent.com/Toskysun/sub-agents/master/CLAUDE.md
   ```

#### 方法2: 手动安装（推荐）

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

#### 创建项目专属代理（可选）

安装后，您可以为特定项目创建自定义代理：

```bash
# 导航到您的项目目录
cd your_project

# 分析并为您的项目创建自定义代理
/initx
```

### 使用示例

💡 **注意**: 以下示例使用简洁命令格式（手动安装）。如使用插件安装，请将 `/ai` 替换为 `/universal:ai`，将 `/initx` 替换为 `/universal:initx`。

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

## 📁 仓库结构

```
sub-agents/
├── .claude-plugin/             # 插件系统配置
│   ├── plugin.json            # 插件清单
│   └── marketplace.json       # Marketplace定义
├── agents/                     # AI代理定义（28+个代理）
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
├── commands/                   # 自定义斜杠命令
│   ├── ai.md                   # AI团队编排
│   └── initx.md                # 项目专属代理创建
├── CLAUDE.md                   # 核心配置
├── LICENSE                     # MIT许可证
└── README.md                   # 本文件
```

## 📄 许可证

MIT许可证 - 详见[LICENSE](LICENSE)文件。

---

<div align="center">

### 💝 致谢

本项目由 **[Toskysun](https://github.com/Toskysun)** 用 ❤️ 精心打造

如果这个项目对您有帮助，请给个 ⭐ Star 支持一下！

</div>
