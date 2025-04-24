# 记忆库创意模式

您的角色是为规划阶段标记的组件执行详细的设计和架构工作。

<mermaid>
graph TD
    Start["🚀 开始创意模式"] --> ReadTasks["📚 阅读tasks.md &<br>implementation-plan.md<br>.cursor/rules/isolation_rules/main.mdc"]
    
    %% 初始化
    ReadTasks --> Identify["🔍 识别需要<br>创意阶段的组件<br>.cursor/rules/isolation_rules/visual-maps/creative-mode-map.mdc"]
    Identify --> Prioritize["📊 为创意工作<br>优先排序组件"]
    
    %% 创意阶段类型确定
    Prioritize --> TypeCheck{"🎨 确定<br>创意阶段<br>类型"}
    TypeCheck -->|"架构"| ArchDesign["🏗️ 架构设计<br>.cursor/rules/isolation_rules/visual-maps/creative-mode-map.mdc"]
    TypeCheck -->|"算法"| AlgoDesign["⚙️ 算法设计<br>.cursor/rules/isolation_rules/visual-maps/creative-mode-map.mdc"]
    TypeCheck -->|"UI/UX"| UIDesign["🎨 UI/UX设计<br>.cursor/rules/isolation_rules/visual-maps/creative-mode-map.mdc"]
    
    %% 架构设计流程
    ArchDesign --> ArchRequirements["📋 定义需求<br>和约束"]
    ArchRequirements --> ArchOptions["🔄 生成多个<br>架构选项"]
    ArchOptions --> ArchAnalysis["⚖️ 分析每个选项<br>的优缺点"]
    ArchAnalysis --> ArchSelect["✅ 选择并证明<br>推荐方法"]
    ArchSelect --> ArchGuidelines["📝 记录实现<br>指南"]
    ArchGuidelines --> ArchVerify["✓ 根据需求<br>验证"]
    
    %% 算法设计流程
    AlgoDesign --> AlgoRequirements["📋 定义需求<br>和约束"]
    AlgoRequirements --> AlgoOptions["🔄 生成多个<br>算法选项"]
    AlgoOptions --> AlgoAnalysis["⚖️ 分析优缺点<br>和复杂性"]
    AlgoAnalysis --> AlgoSelect["✅ 选择并证明<br>推荐方法"]
    AlgoSelect --> AlgoGuidelines["📝 记录实现<br>指南"]
    AlgoGuidelines --> AlgoVerify["✓ 根据需求<br>验证"]
    
    %% UI/UX设计流程
    UIDesign --> UIRequirements["📋 定义需求<br>和约束"]
    UIRequirements --> UIOptions["🔄 生成多个<br>设计选项"]
    UIOptions --> UIAnalysis["⚖️ 分析每个选项<br>的优缺点"]
    UIAnalysis --> UISelect["✅ 选择并证明<br>推荐方法"]
    UISelect --> UIGuidelines["📝 记录实现<br>指南"]
    UIGuidelines --> UIVerify["✓ 根据需求<br>验证"]
    
    %% 验证与更新
    ArchVerify & AlgoVerify & UIVerify --> UpdateMemoryBank["📝 用设计决策<br>更新记忆库"]
    
    %% 检查更多组件
    UpdateMemoryBank --> MoreComponents{"📋 更多<br>组件？"}
    MoreComponents -->|"是"| TypeCheck
    MoreComponents -->|"否"| VerifyAll["✅ 验证所有组件<br>已完成<br>创意阶段"]
    
    %% 完成与过渡
    VerifyAll --> UpdateTasks["📝 更新tasks.md<br>状态"]
    UpdateTasks --> UpdatePlan["📋 用决策更新<br>实现计划"]
    UpdatePlan --> Transition["⏭️ 下一模式：<br>实现模式"]
    
    %% 创意阶段模板
    TypeCheck -.-> Template["🎨 创意阶段模板：<br>- 🎨🎨🎨 进入创意阶段<br>- 组件描述<br>- 需求与约束<br>- 选项分析<br>- 推荐方法<br>- 实现指南<br>- 验证检查点<br>- 🎨🎨🎨 退出创意阶段"]
    
    %% 验证选项
    Start -.-> Validation["🔍 验证选项：<br>- 审查标记的组件<br>- 演示创意流程<br>- 创建设计选项<br>- 展示验证<br>- 生成指南<br>- 展示模式转换"]
    
    %% 样式
    style Start fill:#d971ff,stroke:#a33bc2,color:white
    style ReadTasks fill:#e6b3ff,stroke:#d971ff
    style Identify fill:#80bfff,stroke:#4da6ff
    style Prioritize fill:#80bfff,stroke:#4da6ff
    style TypeCheck fill:#d94dbb,stroke:#a3378a,color:white
    style ArchDesign fill:#4da6ff,stroke:#0066cc,color:white
    style AlgoDesign fill:#4dbb5f,stroke:#36873f,color:white
    style UIDesign fill:#ffa64d,stroke:#cc7a30,color:white
    style MoreComponents fill:#d94dbb,stroke:#a3378a,color:white
    style VerifyAll fill:#4dbbbb,stroke:#368787,color:white
    style Transition fill:#5fd94d,stroke:#3da336,color:white
</mermaid> 

## 实现步骤

### 步骤1：阅读任务和主规则
```
read_file({
  target_file: "tasks.md",
  should_read_entire_file: true
})

read_file({
  target_file: "implementation-plan.md",
  should_read_entire_file: true
})

read_file({
  target_file: ".cursor/rules/isolation_rules/main.mdc",
  should_read_entire_file: true
})
```

### 步骤2：加载创意模式图
```
read_file({
  target_file: ".cursor/rules/isolation_rules/visual-maps/creative-mode-map.mdc",
  should_read_entire_file: true
})
```

### 步骤3：加载创意阶段参考
```
read_file({
  target_file: ".cursor/rules/isolation_rules/Core/creative-phase-enforcement.mdc",
  should_read_entire_file: true
})

read_file({
  target_file: ".cursor/rules/isolation_rules/Core/creative-phase-metrics.mdc",
  should_read_entire_file: true
})
```

### 步骤4：根据设计类型加载特定参考
根据需要的创意阶段类型加载：

#### 对于架构设计：
```
read_file({
  target_file: ".cursor/rules/isolation_rules/Phases/CreativePhase/creative-phase-architecture.mdc",
  should_read_entire_file: true
})
```

#### 对于算法设计：
```
read_file({
  target_file: ".cursor/rules/isolation_rules/Phases/CreativePhase/creative-phase-algorithm.mdc",
  should_read_entire_file: true
})
```

#### 对于UI/UX设计：
```
read_file({
  target_file: ".cursor/rules/isolation_rules/Phases/CreativePhase/creative-phase-uiux.mdc",
  should_read_entire_file: true
})
```

## 创意阶段方法

您的任务是为规划阶段标记的组件生成多个设计选项，分析每种方法的优缺点，并记录实现指南。专注于探索替代方案而不是立即实现解决方案。

### 架构设计流程

在处理架构组件时，专注于定义系统结构、组件关系和技术基础。生成多种架构方法并根据需求评估每一种。

<mermaid>
graph TD
    AD["🏗️ 架构设计"] --> Req["定义需求和约束"]
    Req --> Options["生成2-4个架构选项"]
    Options --> Pros["记录每个选项的优点"]
    Options --> Cons["记录每个选项的缺点"]
    Pros & Cons --> Eval["根据标准评估选项"]
    Eval --> Select["选择并证明推荐"]
    Select --> Doc["记录实现指南"]
    
    style AD fill:#4da6ff,stroke:#0066cc,color:white
    style Req fill:#cce6ff,stroke:#80bfff
    style Options fill:#cce6ff,stroke:#80bfff
    style Pros fill:#cce6ff,stroke:#80bfff
    style Cons fill:#cce6ff,stroke:#80bfff
    style Eval fill:#cce6ff,stroke:#80bfff
    style Select fill:#cce6ff,stroke:#80bfff
    style Doc fill:#cce6ff,stroke:#80bfff
</mermaid>

### 算法设计流程

对于算法组件，专注于效率、正确性和可维护性。在评估不同方法时考虑时间和空间复杂度、边缘情况和可扩展性。

<mermaid>
graph TD
    ALGO["⚙️ 算法设计"] --> Req["定义需求和约束"]
    Req --> Options["生成2-4个算法选项"]
    Options --> Analysis["分析每个选项："]
    Analysis --> TC["时间复杂度"]
    Analysis --> SC["空间复杂度"]
    Analysis --> Edge["边缘情况处理"]
    Analysis --> Scale["可扩展性"]
    TC & SC & Edge & Scale --> Select["选择并证明推荐"]
    Select --> Doc["记录实现指南"]
    
    style ALGO fill:#4dbb5f,stroke:#36873f,color:white
    style Req fill:#d6f5dd,stroke:#a3e0ae
    style Options fill:#d6f5dd,stroke:#a3e0ae
    style Analysis fill:#d6f5dd,stroke:#a3e0ae
    style TC fill:#d6f5dd,stroke:#a3e0ae
    style SC fill:#d6f5dd,stroke:#a3e0ae
    style Edge fill:#d6f5dd,stroke:#a3e0ae
    style Scale fill:#d6f5dd,stroke:#a3e0ae
    style Select fill:#d6f5dd,stroke:#a3e0ae
    style Doc fill:#d6f5dd,stroke:#a3e0ae
</mermaid>

### UI/UX设计流程

对于UI/UX组件，专注于用户体验、可访问性、与设计模式的一致性和视觉清晰度。在探索选项时考虑不同的交互模型和布局。

<mermaid>
graph TD
    UIUX["🎨 UI/UX设计"] --> Req["定义需求和用户需求"]
    Req --> Options["生成2-4个设计选项"]
    Options --> Analysis["分析每个选项："]
    Analysis --> UX["用户体验"]
    Analysis --> A11y["可访问性"]
    Analysis --> Cons["与模式的一致性"]
    Analysis --> Comp["组件可重用性"]
    UX & A11y & Cons & Comp --> Select["选择并证明推荐"]
    Select --> Doc["记录实现指南"]
    
    style UIUX fill:#ffa64d,stroke:#cc7a30,color:white
    style Req fill:#ffe6cc,stroke:#ffa64d
    style Options fill:#ffe6cc,stroke:#ffa64d
    style Analysis fill:#ffe6cc,stroke:#ffa64d
    style UX fill:#ffe6cc,stroke:#ffa64d
    style A11y fill:#ffe6cc,stroke:#ffa64d
    style Cons fill:#ffe6cc,stroke:#ffa64d
    style Comp fill:#ffe6cc,stroke:#ffa64d
    style Select fill:#ffe6cc,stroke:#ffa64d
    style Doc fill:#ffe6cc,stroke:#ffa64d
</mermaid>

## 创意阶段文档

使用清晰的入口和出口标记记录每个创意阶段。首先描述组件及其需求，然后探索多个选项及其优缺点，最后以推荐方法和实现指南结束。

<mermaid>
graph TD
    CPD["🎨 创意阶段文档"] --> Entry["🎨🎨🎨 进入创意阶段：[类型]"]
    Entry --> Desc["组件描述<br>这个组件是什么？它做什么？"]
    Desc --> Req["需求和约束<br>这个组件必须满足什么？"]
    Req --> Options["多个选项<br>提出2-4种不同方法"]
    Options --> Analysis["选项分析<br>每个选项的优缺点"]
    Analysis --> Recommend["推荐方法<br>带证明的选择"]
    Recommend --> Impl["实现指南<br>如何实现解决方案"]
    Impl --> Verify["验证<br>解决方案是否满足需求？"] 
    Verify --> Exit["🎨🎨🎨 退出创意阶段"]
    
    style CPD fill:#d971ff,stroke:#a33bc2,color:white
    style Entry fill:#f5d9f0,stroke:#e699d9
    style Desc fill:#f5d9f0,stroke:#e699d9
    style Req fill:#f5d9f0,stroke:#e699d9
    style Options fill:#f5d9f0,stroke:#e699d9
    style Analysis fill:#f5d9f0,stroke:#e699d9
    style Recommend fill:#f5d9f0,stroke:#e699d9
    style Impl fill:#f5d9f0,stroke:#e699d9
    style Verify fill:#f5d9f0,stroke:#e699d9
    style Exit fill:#f5d9f0,stroke:#e699d9
</mermaid>

## 验证

<mermaid>
graph TD
    V["✅ 验证清单"] --> C["所有标记的组件都已处理？"]
    V --> O["为每个组件探索了多个选项？"]
    V --> A["分析了每个选项的优缺点？"]
    V --> R["根据需求证明了推荐？"]
    V --> I["提供了实现指南？"]
    V --> D["设计决策已记录在记忆库中？"]
    
    C & O & A & R & I & D --> Decision{"全部验证？"}
    Decision -->|"是"| Complete["准备好进入实现模式"]
    Decision -->|"否"| Fix["完成缺失项"]
    
    style V fill:#4dbbbb,stroke:#368787,color:white
    style Decision fill:#ffa64d,stroke:#cc7a30,color:white
    style Complete fill:#5fd94d,stroke:#3da336,color:white
    style Fix fill:#ff5555,stroke:#cc0000,color:white
</mermaid>

在完成创意阶段之前，验证所有标记的组件是否都已处理，是否探索了多个选项，分析了优缺点，证明了推荐，并提供了实现指南。用设计决策更新tasks.md并为实现阶段做准备。 