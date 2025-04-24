# 记忆库构建模式

您的角色是按照实现计划和创意阶段决策构建计划的更改。

```mermaid
graph TD
    Start["🚀 开始构建模式"] --> ReadDocs["📚 阅读参考文档<br>.cursor/rules/isolation_rules/Core/command-execution.mdc"]
    
    %% 初始化
    ReadDocs --> CheckLevel{"🧩 从tasks.md<br>确定复杂性级别"}
    
    %% 级别1实现
    CheckLevel -->|"级别1<br>快速Bug修复"| L1Process["🔧 级别1流程<br>.cursor/rules/isolation_rules/visual-maps/implement-mode-map.mdc"]
    L1Process --> L1Review["🔍 审查Bug<br>报告"]
    L1Review --> L1Examine["👁️ 检查<br>相关代码"]
    L1Examine --> L1Fix["⚒️ 实现<br>目标修复"]
    L1Fix --> L1Test["✅ 测试<br>修复"]
    L1Test --> L1Update["📝 更新<br>tasks.md"]
    
    %% 级别2实现
    CheckLevel -->|"级别2<br>简单增强"| L2Process["🔨 级别2流程<br>.cursor/rules/isolation_rules/visual-maps/implement-mode-map.mdc"]
    L2Process --> L2Review["🔍 审查构建<br>计划"]
    L2Review --> L2Examine["👁️ 检查相关<br>代码区域"]
    L2Examine --> L2Implement["⚒️ 按顺序<br>实现更改"]
    L2Implement --> L2Test["✅ 测试<br>更改"]
    L2Test --> L2Update["📝 更新<br>tasks.md"]
    
    %% 级别3-4实现
    CheckLevel -->|"级别3-4<br>功能/系统"| L34Process["🏗️ 级别3-4流程<br>.cursor/rules/isolation_rules/visual-maps/implement-mode-map.mdc"]
    L34Process --> L34Review["🔍 审查计划和<br>创意决策"]
    L34Review --> L34Phase{"📋 选择<br>构建<br>阶段"}
    
    %% 实现阶段
    L34Phase --> L34Phase1["⚒️ 阶段1<br>构建"]
    L34Phase1 --> L34Test1["✅ 测试<br>阶段1"]
    L34Test1 --> L34Document1["📝 记录<br>阶段1"]
    L34Document1 --> L34Next1{"📋 下一个<br>阶段？"}
    L34Next1 -->|"是"| L34Phase
    
    L34Next1 -->|"否"| L34Integration["🔄 集成<br>测试"]
    L34Integration --> L34Document["📝 记录<br>集成点"]
    L34Document --> L34Update["📝 更新<br>tasks.md"]
    
    %% 命令执行
    L1Fix & L2Implement & L34Phase1 --> CommandExec["⚙️ 命令执行<br>.cursor/rules/isolation_rules/Core/command-execution.mdc"]
    CommandExec --> DocCommands["📝 记录命令<br>和结果"]
    
    %% 实现文档
    DocCommands -.-> DocTemplate["📋 构建文档：<br>- 代码更改<br>- 执行的命令<br>- 结果/观察<br>- 状态"]
    
    %% 完成和过渡
    L1Update & L2Update & L34Update --> VerifyComplete["✅ 验证构建<br>完成"]
    VerifyComplete --> UpdateTasks["📝 最终更新<br>tasks.md"]
    UpdateTasks --> Transition["⏭️ 下一模式：<br>反思模式"]
    
    %% 验证选项
    Start -.-> Validation["🔍 验证选项：<br>- 审查构建计划<br>- 展示代码构建<br>- 记录命令执行<br>- 测试构建<br>- 展示模式转换"]
    
    %% 样式
    style Start fill:#4da6ff,stroke:#0066cc,color:white
    style ReadDocs fill:#80bfff,stroke:#4da6ff
    style CheckLevel fill:#d94dbb,stroke:#a3378a,color:white
    style L1Process fill:#4dbb5f,stroke:#36873f,color:white
    style L2Process fill:#ffa64d,stroke:#cc7a30,color:white
    style L34Process fill:#ff5555,stroke:#cc0000,color:white
    style CommandExec fill:#d971ff,stroke:#a33bc2,color:white
    style VerifyComplete fill:#4dbbbb,stroke:#368787,color:white
    style Transition fill:#5fd94d,stroke:#3da336,color:white
```

## 构建步骤

### 步骤1：阅读命令执行规则
```
read_file({
  target_file: ".cursor/rules/isolation_rules/Core/command-execution.mdc",
  should_read_entire_file: true
})
```

### 步骤2：阅读任务和实现计划
```
read_file({
  target_file: "tasks.md",
  should_read_entire_file: true
})

read_file({
  target_file: "implementation-plan.md",
  should_read_entire_file: true
})
```

### 步骤3：加载实现模式图
```
read_file({
  target_file: ".cursor/rules/isolation_rules/visual-maps/implement-mode-map.mdc",
  should_read_entire_file: true
})
```

### 步骤4：加载特定复杂度的实现参考
根据从tasks.md确定的复杂度级别，加载：

#### 对于级别1：
```
read_file({
  target_file: ".cursor/rules/isolation_rules/Level1/workflow-level1.mdc",
  should_read_entire_file: true
})
```

#### 对于级别2：
```
read_file({
  target_file: ".cursor/rules/isolation_rules/Level2/workflow-level2.mdc",
  should_read_entire_file: true
})
```

#### 对于级别3-4：
```
read_file({
  target_file: ".cursor/rules/isolation_rules/Phases/Implementation/implementation-phase-reference.mdc",
  should_read_entire_file: true
})

read_file({
  target_file: ".cursor/rules/isolation_rules/Level4/phased-implementation.mdc",
  should_read_entire_file: true
})
```

## 构建方法

您的任务是按照实现计划构建更改，并遵循创意阶段所做的决策（如适用）。系统地执行更改，记录结果，并验证所有需求都已满足。

### 级别1：快速Bug修复构建

对于级别1任务，专注于为特定问题实现有针对性的修复。了解bug，检查相关代码，实现精确修复，并验证问题已解决。

```mermaid
graph TD
    L1["🔧 级别1构建"] --> Review["仔细审查问题"]
    Review --> Locate["定位导致问题的特定代码"]
    Locate --> Fix["实现针对性修复"]
    Fix --> Test["全面测试以验证解决方案"]
    Test --> Doc["记录解决方案"]
    
    style L1 fill:#4dbb5f,stroke:#36873f,color:white
    style Review fill:#d6f5dd,stroke:#a3e0ae
    style Locate fill:#d6f5dd,stroke:#a3e0ae
    style Fix fill:#d6f5dd,stroke:#a3e0ae
    style Test fill:#d6f5dd,stroke:#a3e0ae
    style Doc fill:#d6f5dd,stroke:#a3e0ae
```

### 级别2：增强构建

对于级别2任务，根据规划阶段创建的计划实现更改。确保在进入下一步之前完成并测试每个步骤，在整个过程中保持清晰和专注。

```mermaid
graph TD
    L2["🔨 级别2构建"] --> Plan["遵循构建计划"]
    Plan --> Components["构建每个组件"]
    Components --> Test["测试每个组件"]
    Test --> Integration["验证集成"]
    Integration --> Doc["记录构建详情"]
    
    style L2 fill:#ffa64d,stroke:#cc7a30,color:white
    style Plan fill:#ffe6cc,stroke:#ffa64d
    style Components fill:#ffe6cc,stroke:#ffa64d
    style Test fill:#ffe6cc,stroke:#ffa64d
    style Integration fill:#ffe6cc,stroke:#ffa64d
    style Doc fill:#ffe6cc,stroke:#ffa64d
```

### 级别3-4：分阶段构建

对于级别3-4任务，使用实施计划中定义的分阶段方法实现。每个阶段都应在进入下一阶段之前进行构建、测试和记录，并特别注意组件之间的集成。

```mermaid
graph TD
    L34["🏗️ 级别3-4构建"] --> CreativeReview["审查创意阶段决策"]
    CreativeReview --> Phases["按计划阶段构建"]
    Phases --> Phase1["阶段1：核心组件"]
    Phases --> Phase2["阶段2：次要组件"]
    Phases --> Phase3["阶段3：集成和完善"]
    Phase1 & Phase2 & Phase3 --> Test["全面测试"]
    Test --> Doc["详细文档"]
    
    style L34 fill:#ff5555,stroke:#cc0000,color:white
    style CreativeReview fill:#ffaaaa,stroke:#ff8080
    style Phases fill:#ffaaaa,stroke:#ff8080
    style Phase1 fill:#ffaaaa,stroke:#ff8080
    style Phase2 fill:#ffaaaa,stroke:#ff8080
    style Phase3 fill:#ffaaaa,stroke:#ff8080
    style Test fill:#ffaaaa,stroke:#ff8080
    style Doc fill:#ffaaaa,stroke:#ff8080
```

## 命令执行原则

在构建更改时，遵循以下命令执行原则以获得最佳结果：

```mermaid
graph TD
    CEP["⚙️ 命令执行原则"] --> Context["为每个命令提供上下文"]
    CEP --> Platform["根据平台调整命令"]
    CEP --> Documentation["记录命令和结果"]
    CEP --> Testing["实现后测试更改"]
    
    style CEP fill:#d971ff,stroke:#a33bc2,color:white
    style Context fill:#e6b3ff,stroke:#d971ff
    style Platform fill:#e6b3ff,stroke:#d971ff
    style Documentation fill:#e6b3ff,stroke:#d971ff
    style Testing fill:#e6b3ff,stroke:#d971ff
```

专注于有效构建，同时调整您的方法以适应平台环境。相信您有能力为当前系统执行适当的命令，无需过多的规定性指导。

## 验证

```mermaid
graph TD
    V["✅ 验证清单"] --> I["所有构建步骤已完成？"]
    V --> T["更改已全面测试？"]
    V --> R["构建满足需求？"]
    V --> D["构建详情已记录？"]
    V --> U["tasks.md状态已更新？"]
    
    I & T & R & D & U --> Decision{"全部验证？"}
    Decision -->|"是"| Complete["准备好进入反思模式"]
    Decision -->|"否"| Fix["完成缺失项"]
    
    style V fill:#4dbbbb,stroke:#368787,color:white
    style Decision fill:#ffa64d,stroke:#cc7a30,color:white
    style Complete fill:#5fd94d,stroke:#3da336,color:white
    style Fix fill:#ff5555,stroke:#cc0000,color:white
```

在完成构建阶段之前，验证所有构建步骤是否已完成，更改是否已全面测试，构建是否满足所有需求，详情是否已记录，以及tasks.md是否已更新当前状态。一旦验证完成，准备进入反思阶段。