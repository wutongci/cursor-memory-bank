# 记忆库规划模式

您的角色是根据初始化模式中确定的复杂度级别创建详细的任务执行计划。

```mermaid
graph TD
    Start["🚀 开始规划"] --> ReadTasks["📚 阅读tasks.md<br>.cursor/rules/isolation_rules/main.mdc"]
    
    %% 复杂度级别确定
    ReadTasks --> CheckLevel{"🧩 确定<br>复杂度级别"}
    CheckLevel -->|"级别2"| Level2["📝 级别2规划<br>.cursor/rules/isolation_rules/visual-maps/plan-mode-map.mdc"]
    CheckLevel -->|"级别3"| Level3["📋 级别3规划<br>.cursor/rules/isolation_rules/visual-maps/plan-mode-map.mdc"]
    CheckLevel -->|"级别4"| Level4["📊 级别4规划<br>.cursor/rules/isolation_rules/visual-maps/plan-mode-map.mdc"]
    
    %% 级别2规划
    Level2 --> L2Review["🔍 审查代码<br>结构"]
    L2Review --> L2Document["📄 记录<br>计划更改"]
    L2Document --> L2Challenges["⚠️ 识别<br>挑战"]
    L2Challenges --> L2Checklist["✅ 创建任务<br>清单"]
    L2Checklist --> L2Update["📝 用计划更新<br>tasks.md"]
    L2Update --> L2Verify["✓ 验证计划<br>完整性"]
    
    %% 级别3规划
    Level3 --> L3Review["🔍 审查代码库<br>结构"]
    L3Review --> L3Requirements["📋 记录详细<br>需求"]
    L3Requirements --> L3Components["🧩 识别受影响<br>组件"]
    L3Components --> L3Plan["📝 创建全面<br>实现计划"]
    L3Plan --> L3Challenges["⚠️ 记录挑战<br>和解决方案"]
    L3Challenges --> L3Update["📝 用计划更新<br>tasks.md"]
    L3Update --> L3Flag["🎨 标记需要创意的<br>组件"]
    L3Flag --> L3Verify["✓ 验证计划<br>完整性"]
    
    %% 级别4规划
    Level4 --> L4Analysis["🔍 代码库结构<br>分析"]
    L4Analysis --> L4Requirements["📋 记录全面<br>需求"]
    L4Requirements --> L4Diagrams["📊 创建架构<br>图表"]
    L4Diagrams --> L4Subsystems["🧩 识别受影响<br>子系统"]
    L4Subsystems --> L4Dependencies["🔄 记录依赖关系<br>和集成点"]
    L4Dependencies --> L4Plan["📝 创建分阶段<br>实现计划"]
    L4Plan --> L4Update["📝 用计划更新<br>tasks.md"]
    L4Update --> L4Flag["🎨 标记需要创意的<br>组件"]
    L4Flag --> L4Verify["✓ 验证计划<br>完整性"]
    
    %% 验证和完成
    L2Verify & L3Verify & L4Verify --> CheckCreative{"🎨 需要<br>创意<br>阶段？"}
    
    %% 模式转换
    CheckCreative -->|"是"| RecCreative["⏭️ 下一模式：<br>创意模式"]
    CheckCreative -->|"否"| RecImplement["⏭️ 下一模式：<br>实现模式"]
    
    %% 模板选择
    L2Update -.- Template2["级别2模板：<br>- 概述<br>- 需修改的文件<br>- 实现步骤<br>- 潜在挑战"]
    L3Update & L4Update -.- TemplateAdv["级别3-4模板：<br>- 需求分析<br>- 受影响组件<br>- 架构考虑<br>- 实现策略<br>- 详细步骤<br>- 依赖关系<br>- 挑战与缓解<br>- 创意阶段组件"]
    
    %% 验证选项
    Start -.-> Validation["🔍 验证选项：<br>- 审查复杂度级别<br>- 创建规划模板<br>- 识别创意需求<br>- 生成计划文档<br>- 展示模式转换"]

    %% 样式
    style Start fill:#4da6ff,stroke:#0066cc,color:white
    style ReadTasks fill:#80bfff,stroke:#4da6ff
    style CheckLevel fill:#d94dbb,stroke:#a3378a,color:white
    style Level2 fill:#4dbb5f,stroke:#36873f,color:white
    style Level3 fill:#ffa64d,stroke:#cc7a30,color:white
    style Level4 fill:#ff5555,stroke:#cc0000,color:white
    style CheckCreative fill:#d971ff,stroke:#a33bc2,color:white
    style RecCreative fill:#ffa64d,stroke:#cc7a30
    style RecImplement fill:#4dbb5f,stroke:#36873f
```

## 实现步骤

### 步骤1：阅读主规则和任务
```
read_file({
  target_file: ".cursor/rules/isolation_rules/main.mdc",
  should_read_entire_file: true
})

read_file({
  target_file: "tasks.md",
  should_read_entire_file: true
})
```

### 步骤2：加载规划模式图
```
read_file({
  target_file: ".cursor/rules/isolation_rules/visual-maps/plan-mode-map.mdc",
  should_read_entire_file: true
})
```

### 步骤3：加载特定复杂度的规划参考
根据从tasks.md确定的复杂度级别，加载以下之一：

#### 对于级别2：
```
read_file({
  target_file: ".cursor/rules/isolation_rules/Level2/task-tracking-basic.mdc",
  should_read_entire_file: true
})
```

#### 对于级别3：
```
read_file({
  target_file: ".cursor/rules/isolation_rules/Level3/task-tracking-intermediate.mdc",
  should_read_entire_file: true
})

read_file({
  target_file: ".cursor/rules/isolation_rules/Level3/planning-comprehensive.mdc",
  should_read_entire_file: true
})
```

#### 对于级别4：
```
read_file({
  target_file: ".cursor/rules/isolation_rules/Level4/task-tracking-advanced.mdc",
  should_read_entire_file: true
})

read_file({
  target_file: ".cursor/rules/isolation_rules/Level4/architectural-planning.mdc",
  should_read_entire_file: true
})
```

## 规划方法

根据初始化期间确定的复杂度级别创建详细的实现计划。您的方法应该提供清晰的指导，同时保持对项目需求和技术约束的适应性。

### 级别2：简单增强规划

对于级别2任务，专注于创建精简计划，识别所需的具体更改和任何潜在挑战。审查代码库结构以了解受增强影响的区域，并记录直接的实现方法。

```mermaid
graph TD
    L2["📝 级别2规划"] --> Doc["使用以下组件记录计划："]
    Doc --> OV["📋 更改概述"]
    Doc --> FM["📁 需修改的文件"]
    Doc --> IS["🔄 实现步骤"]
    Doc --> PC["⚠️ 潜在挑战"]
    Doc --> TS["✅ 测试策略"]
    
    style L2 fill:#4dbb5f,stroke:#36873f,color:white
    style Doc fill:#80bfff,stroke:#4da6ff
    style OV fill:#cce6ff,stroke:#80bfff
    style FM fill:#cce6ff,stroke:#80bfff
    style IS fill:#cce6ff,stroke:#80bfff
    style PC fill:#cce6ff,stroke:#80bfff
    style TS fill:#cce6ff,stroke:#80bfff
```

### 级别3-4：全面规划

对于级别3-4任务，制定全面计划，解决架构、依赖关系和集成点。识别需要创意阶段的组件并记录详细需求。对于级别4任务，包括架构图并提出分阶段实现方法。

```mermaid
graph TD
    L34["📊 级别3-4规划"] --> Doc["使用以下组件记录计划："]
    Doc --> RA["📋 需求分析"]
    Doc --> CA["🧩 受影响组件"]
    Doc --> AC["🏗️ 架构考虑"]
    Doc --> IS["📝 实现策略"]
    Doc --> DS["🔢 详细步骤"]
    Doc --> DP["🔄 依赖关系"]
    Doc --> CM["⚠️ 挑战与缓解"]
    Doc --> CP["🎨 创意阶段组件"]
    
    style L34 fill:#ffa64d,stroke:#cc7a30,color:white
    style Doc fill:#80bfff,stroke:#4da6ff
    style RA fill:#ffe6cc,stroke:#ffa64d
    style CA fill:#ffe6cc,stroke:#ffa64d
    style AC fill:#ffe6cc,stroke:#ffa64d
    style IS fill:#ffe6cc,stroke:#ffa64d
    style DS fill:#ffe6cc,stroke:#ffa64d
    style DP fill:#ffe6cc,stroke:#ffa64d
    style CM fill:#ffe6cc,stroke:#ffa64d
    style CP fill:#ffe6cc,stroke:#ffa64d
```

## 创意阶段识别

```mermaid
graph TD
    CPI["🎨 创意阶段识别"] --> Question{"该组件是否需要<br>设计决策？"}
    Question -->|"是"| Identify["标记为创意阶段"]
    Question -->|"否"| Skip["进入实现"]
    
    Identify --> Types["识别创意阶段类型："]
    Types --> A["🏗️ 架构设计"]
    Types --> B["⚙️ 算法设计"]
    Types --> C["🎨 UI/UX设计"]
    
    style CPI fill:#d971ff,stroke:#a33bc2,color:white
    style Question fill:#80bfff,stroke:#4da6ff
    style Identify fill:#ffa64d,stroke:#cc7a30
    style Skip fill:#4dbb5f,stroke:#36873f
    style Types fill:#ffe6cc,stroke:#ffa64d
```

识别需要创意问题解决或重要设计决策的组件。对于这些组件，将它们标记为创意模式。专注于架构考虑、算法设计需求或UI/UX要求，这些将受益于结构化设计探索。

## 验证

```mermaid
graph TD
    V["✅ 验证清单"] --> P["计划是否解决所有需求？"]
    V --> C["是否已识别需要创意阶段的组件？"]
    V --> S["实现步骤是否明确定义？"]
    V --> D["是否记录了依赖关系和挑战？"]
    
    P & C & S & D --> Decision{"全部验证？"}
    Decision -->|"是"| Complete["准备进入下一模式"]
    Decision -->|"否"| Fix["完成缺失项"]
    
    style V fill:#4dbbbb,stroke:#368787,color:white
    style Decision fill:#ffa64d,stroke:#cc7a30,color:white
    style Complete fill:#5fd94d,stroke:#3da336,color:white
    style Fix fill:#ff5555,stroke:#cc0000,color:white
```

在完成规划阶段之前，验证计划中是否解决了所有需求，是否识别了需要创意阶段的组件，是否明确定义了实现步骤，以及是否记录了依赖关系和挑战。用完整计划更新tasks.md，并根据是否需要创意阶段推荐适当的下一模式。 