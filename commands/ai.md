## Usage
`/ai <TASK_DESCRIPTION | list | info <role> | workflow | auto>`

## 🎯 Task Complexity Assessment (ENHANCED)

### Level 0: Micro Tasks - Direct execution
- **Scenario**: Information queries, file reading, status checks
- **Characteristics**: No code modification, pure information retrieval  
- **Boundary**: <5 minutes, no professional knowledge needed
- **Triggers**: "view", "check", "display", "read"
- **Action**: Main controller completes directly, no agent calls

### Level 1: Simple Tasks - Single agent direct
- **Scenario**: Single file modification, basic configuration, simple functionality
- **Characteristics**: <50 lines of code, single technology stack, clear requirements
- **Boundary**: One professional domain, no cross-module impact
- **Triggers**: "add", "modify", "configure" single components
- **Action**: Direct call to 1 professional agent, bypassing director

### Level 2: Medium Tasks - Single agent complex
- **Scenario**: Complete functional modules, multi-file coordination, requires testing
- **Characteristics**: 50-200 lines of code, requires planning and validation
- **Boundary**: Single technology stack but complex logic, may require refactoring
- **Triggers**: "implement", "develop", "build" complete features
- **Action**: 1 professional agent handles full process, main controller monitors

### Level 3: Composite Tasks - Multi-agent serial
- **Scenario**: Cross-module functionality, frontend-backend coordination, 2-3 professional domains
- **Characteristics**: 200-500 lines of code, requires multi-step coordination
- **Boundary**: Clear dependency relationships, serial execution
- **Triggers**: "integrate", "connect", "full-stack" functionality
- **Action**: Main controller serially calls 2-3 agents

### Level 4: Parallel Tasks - Multi-agent concurrent
- **Scenario**: Independent module parallel development, performance optimization, multi-platform
- **Characteristics**: 3-5 independent workflows, can execute in parallel
- **Boundary**: Low conflict risk, high independence
- **Triggers**: "simultaneously", "parallel", "multi-platform" development
- **Action**: Main controller calls 3-5 agents in parallel

### Level 5: Enterprise Tasks - Director coordination
- **Scenario**: System refactoring, architecture upgrades, complex project analysis
- **Characteristics**: 5+ professional domains, complex dependencies, multi-phase planning
- **Boundary**: Requires specialized task decomposition and coordination management
- **Triggers**: "refactor", "architecture", "system analysis", "enterprise-level"
- **Action**: task-dispatch-director pure coordination, decompose into Level 1-3 tasks

## ⚡ Enhanced Auto-Trigger Matrix

**Level 0 Trigger Conditions (no agent calls):**
- Keywords: "view", "check", "display", "read", "list", "status"
- Questions: "what is", "how to understand", "can you explain"
- Operations: Pure information queries, no modification requirements

**Level 1 Trigger Conditions (single agent direct):**
- Keywords: "add", "modify", "update", "configure", "adjust"
- Scope: Single file or component + single technology stack
- Examples: "add Vue component", "modify API endpoint", "configure database connection"

**Level 2 Trigger Conditions (single agent complex):**
- Keywords: "implement", "develop", "build", "create" functional modules
- Scope: Multi-file but single technology stack + requires testing
- Examples: "implement user login", "develop payment module", "build search functionality"

**Level 3 Trigger Conditions (multi-agent serial):**
- Keywords: "integrate", "connect", "full-stack", "end-to-end"
- Scope: 2-3 technology stacks collaboration + clear dependencies
- Examples: "frontend-backend integration", "API integration", "full-stack user system"

**Level 4 Trigger Conditions (multi-agent parallel):**
- Keywords: "simultaneously", "parallel", "multi-platform", "optimize"
- Scope: 3-5 independent modules + low conflict
- Examples: "multi-platform synchronized development", "comprehensive performance optimization"

**Level 5 Trigger Conditions (Director coordination):**
- Keywords: "refactor", "architecture", "system analysis", "enterprise-level", "complete solution"
- Scope: 5+ professional domains + complex planning
- Examples: "system architecture refactoring", "enterprise microservice design", "complex project analysis"

**Mandatory Director Bypass Conditions (Level 0-2):**
- Single file operations
- Clearly specified single technology stack
- User explicitly says "no team collaboration needed"
- Simple information queries and basic modifications

## 🚫 Direct Handling
Handle without agents:
- File reading, searching, basic analysis
- Simple code modifications or config updates
- Information queries and technical explanations

## 🛡️ Anti-Over-Engineering Principles
- **One goal, one agent**: Only call one agent unless true collaboration needed
- **Minimum viable solution**: Choose simplest working method
- **User-oriented**: Based on explicit user needs, not assumptions

## 👥 Team Members (when using `/ai list`)

### 🏛️ Leadership & Strategy
- 🎯 **task-dispatch-director** - Task coordination hub (⚠️ Never calls itself)
- 🏗️ **cto** - Technical strategy and architecture decisions
- 📊 **product-manager** - Product requirements and PRD creation

### 💻 Development Team
- 📋 **technical-solution-architect** - Technical solution design based on PRDs
- 🎨 **frontend-developer** - React expert, UI components, performance optimization
- 💾 **backend-developer** - Multi-stack API development (FastAPI/Spring Boot/Node.js)
- 🔧 **infrastructure-developer** - Development tools and automation scripts
- 🚀 **devops-engineer** - Docker containerization and deployment

### 🌟 Frontend Technology Stack Experts
- 🌟 **vue-developer** - Vue 2/3, Nuxt.js, component development, state management
- ⚛️ **react-developer** - React 18+, Next.js, modern Hooks patterns

### 🏗️ Backend Architecture Experts
- 🚀 **go-architect** - Go microservice architecture, distributed systems, cloud-native
- 🦀 **rust-architect** - Rust system programming, memory safety, high-performance computing
- ☕ **java-developer** - Java enterprise development, Spring Boot microservices
- 🌱 **spring-architect** - Spring full-stack, microservice architecture, enterprise design

### 🐍 Python Web Experts
- 🌶️ **flask-expert** - Flask framework, RESTful API, traditional web applications
- ⚡ **fastapi-expert** - FastAPI framework, async programming, high-performance APIs

### 📱 Mobile Development
- 📱 **android-developer** - Android native development, Kotlin/Java, Material Design
- 🎨 **mobile-ui-designer** - Mobile UI/UX design, cross-platform interfaces

### 🔐 Security & Reverse Engineering
- 🎣 **android-hooking-expert** - Frida/Hook technology, dynamic analysis
- 📱 **xposed-developer** - Xposed module development, system-level customization
- 🔍 **reverse-engineer** - Code deobfuscation, static analysis
- 🦠 **malware-analyst** - Malware analysis, threat detection

### 🌙 Scripting & Automation
- 🌙 **lua-developer** - Lua script development (game/web/automation scripts)

### 🎨 Design Experts
- 🎨 **google-ui-designer** - Material Design, user experience design

### 🔧 Quality & Operations
- 👀 **code-review-expert** - Code quality review, security checks
- 🚀 **devops-engineer** - Docker deployment, CI/CD, operations monitoring
- 🧪 **test-expert** - Testing strategy, automated testing, performance testing
- 🐛 **qa-engineer** - Problem diagnosis, root cause analysis
- 🔬 **technical-researcher** - Technical research, feasibility analysis

## 📖 Quick Reference

### 🎨 Frontend Development
- **Vue.js applications** → vue-developer
- **React modern development** → react-developer
- **General frontend development** → frontend-developer
- **Material Design** → google-ui-designer
- **Mobile UI design** → mobile-ui-designer

### 💾 Backend Development
- **Go microservice architecture** → go-architect
- **Rust system programming** → rust-architect
- **Java enterprise development** → java-developer
- **Spring microservices** → spring-architect
- **Flask web applications** → flask-expert
- **FastAPI high-performance APIs** → fastapi-expert
- **General API development** → backend-developer

### 📱 Mobile Development
- **Android application development** → android-developer
- **Mobile interface design** → mobile-ui-designer

### 🔐 Security & Analysis
- **Android Hook technology** → android-hooking-expert
- **Xposed module development** → xposed-developer
- **Code reverse analysis** → reverse-engineer
- **Malware analysis** → malware-analyst

### 🌙 Scripting & Automation
- **Lua script development** → lua-developer (game/web/automation)

### 🔧 Quality & Operations
- **Automated tasks** → infrastructure-developer
- **Production deployment** → devops-engineer
- **Problem fixing** → qa-engineer
- **Code review** → code-review-expert
- **Function testing** → test-expert
- **Technology research** → technical-researcher

### ❌ Avoid Over-invocation
- "Explain this function" → Level 0: Handle directly (not technical-researcher + cto)
- "Change config file" → Level 1: Single specialist (not infrastructure-developer + devops-engineer)
- "Vue vs React for this project?" → Level 0: Handle directly or Level 1: technical-researcher (not multiple developers)

## 🎮 Command Modes

### 🎯 Task Execution Mode (Default)
Just describe what you need naturally:
```
/ai "Add remember password feature to login page"
/ai "API response is too slow, need performance optimization" 
/ai "Code review recent commits"
/ai "Research whether to upgrade to React 19"
```

### 📚 Information Mode
- `/ai list` - Show all team members with descriptions
- `/ai info <role>` - Get detailed information about specific role
- `/ai workflow` - Display development workflows and best practices

### 🤖 Auto-Intelligence Mode
- `/ai auto` - Enable maximum automation with context-aware recommendations

## 📊 Level 0-5 System Benefits

### 🎯 **Precision Task Routing**
- **Level 0-2**: Bypass director overhead → Direct specialist assignment
- **Level 3-4**: Coordinated multi-agent execution → Optimal resource allocation  
- **Level 5**: Enterprise-level orchestration → Complex project management

### ⚡ **Performance Optimization**  
- **3x faster** for simple tasks (Level 0-1 direct execution)
- **2x more reliable** for complex tasks (proper coordination)
- **Zero agent overload** (strict role boundaries)

### 🛡️ **Anti-Deadlock Protection**
- **task-dispatch-director** limited to pure coordination only
- **Automatic fallback** when agents fail (3-retry rule)
- **Forced bypass** for simple operations (Level 0-2)

## 📊 Smart Parallel Task Execution Output

### **Smart Parallel Task Execution Output:**
```
🧠 Intelligent Analysis (ultrathink mode activated)
- Intent: [Detected user goal with confidence %]
- Complexity: [Simple(1-2)/Medium(3-4)/Complex(5)] (Auto-assessed)
- Parallel Strategy: [Why this parallel approach was chosen]
- Estimated Speedup: [Expected efficiency gain vs serial execution]

🚀 Parallel Execution Plan (Multi-Phase Concurrent)
Phase 1 (Parallel): [3 agents] → [Concurrent analysis/planning]
├── 🎯 [Agent A] → [Specific deliverable] (parallel group 1)
├── 🎯 [Agent B] → [Specific deliverable] (parallel group 1)  
└── 🎯 [Agent C] → [Specific deliverable] (parallel group 1)

Phase 2 (Parallel): [2 agents] → [Build on Phase 1 results]
├── 🔄 [Agent D] → [Integration task] (parallel group 2)
└── 🔄 [Agent E] → [Implementation task] (parallel group 2)

⚡ Launching Parallel AI Team...
├── 🚀 Phase 1: Launching 3 concurrent agents...
│   ├── ✅ [Agent A] completed: [result summary]
│   ├── ✅ [Agent B] completed: [result summary]  
│   └── 🔄 [Agent C] retrying... (attempt 2/3)
├── 🔄 Integrating Phase 1 results...
├── 🚀 Phase 2: Launching 2 concurrent agents with enhanced context...
│   ├── ✅ [Agent D] completed: [result summary]
│   └── ✅ [Agent E] completed: [result summary]

✅ Mission Complete (Parallel Execution)
- 📦 **Deliverables**: [What was produced across all parallel phases]
- ⚡ **Performance**: [Actual speedup achieved: 3.2x faster than serial]
- 🛡️ **Reliability**: [Retry success rate: 2 retries, 100% final success]
- 🧠 **Learning**: [Pattern for future similar parallel executions]
```

### **Parallel Execution Status Indicators:**
```bash
🚀 Parallel Launch    # Multiple agents starting simultaneously
⚡ Partial Success   # Some agents completed, others retrying
🔄 Auto-Retry        # Intelligent retry with exponential backoff
✅ Phase Complete    # All agents in phase finished successfully
🔀 Context Merge     # Integrating parallel results for next phase
🛡️ Fallback Mode    # Serial execution after parallel retry exhaustion
```

### **Performance Metrics Display:**
```
📊 Parallel Performance Dashboard
- Concurrent agents launched: 8 total across 3 phases
- Parallel efficiency gain: 4.1x faster than serial execution
- Auto-retry success rate: 94% (3 retries recovered, 1 fallback)
- Resource utilization: 87% (optimal parallel agent distribution)
- Total execution time: 12 minutes (vs 49 minutes serial estimate)
```

## 🚀 Benefits
1. **Single Command** - No need to remember specific roles
2. **Intelligent Routing** - Automatically engages right experts
3. **Full Workflow** - Handles complete development cycle
4. **Quality Gates** - Ensures proper reviews and testing
5. **Coordination** - Manages team collaboration