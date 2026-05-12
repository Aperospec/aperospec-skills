# Aperospec 组织架构说明

## 1. 系统总述

Aperospec 不是一个多人团队协作文档系统。

它是一套由你单独管理的代理组织。

在这套组织里：

- 你是唯一的人类负责人。
- `aperospec-runtime` 是你直属的总管型 PM。
- 其余 Skill 是 `Runtime` 下面的专职员工。

这意味着所有真正的方向、判断、取舍、审美与最终拍板都属于你。

`Runtime` 不代表你创作，它只代表你管理。

## 2. 组织层级

### 第一层：你

你的组织身份是：

> 创意总监 / 唯一决策者 / 最终责任人

你负责：

- 定义项目方向
- 判断项目是否值得做
- 决定是否采用已有资产
- 决定项目是否需要返工
- 决定最终输出是否达标
- 决定哪些名字、结构、资产不得被改动

你不负责：

- 逐段执行流水线
- 手动协调每一个 Skill 的上下游输入
- 亲自维护中间产物链路

这些工作交给 `Runtime`。

### 第二层：Runtime

`aperospec-runtime` 的组织身份是：

> 直属 PM / 总控 / 流水线总管

它直接向你负责。

它的职责不是创作，而是：

- 接收你的任务或上游注入结果
- 判断从哪一阶段开始执行
- 按顺序调用正确的 Skill
- 控制每个 Skill 只能看到它该看到的内容
- 冻结每一阶段产物
- 防止上下游串味
- 把整条 Pipeline 稳定推进到最终交付

`Runtime` 是组织中唯一有权协调其它 Skill 的角色。

### 第三层：Runtime 直属员工

这些 Skill 不是彼此平级协作的自由角色，而是 `Runtime` 统一调度下的专职岗位。

#### `aperospec-injection`

组织身份：

> 前置资产接管员 / 内容注入判断岗

职责：

- 识别用户已有内容属于哪一层
- 判断哪些内容要锁定、跳过、延续或辅助生成
- 确认正式命名并进入 Lock Asset State
- 向 `Runtime` 交付 RIM

它不负责创作，只负责接管已有内容并把资产正确接入流水线。

#### `aperospec-project`

组织身份：

> 认知研究员 / 上游 Cognitive Engine

职责：

- 只接收 Topic 与上游材料
- 输出 `CWP`
- 完成世界形成、根因、驱动力、核心矛盾、行为变化、未来投射、认知触发点等上游认知结构

它不负责 narrative、deck、visual。

#### `aperospec-cinema`

组织身份：

> 叙事导演 / Narrative Translation 岗

职责：

- 只读取 `CWP`
- 输出 `NWP`
- 把认知结构翻译成叙事宇宙、情绪环境、核心冲突与叙事方向

它不负责重新分析世界，也不负责视觉。

#### `aperospec-conceptdeck`

组织身份：

> 概念提案导演 / Concept Narrative 岗

职责：

- 只读取 `NWP`
- 输出 `CDP`
- 把 Narrative Universe 拆成可推进认知的概念页面序列、节奏、停顿、情绪推进与页面核心概念

它不负责视觉执行，也不负责重写 Narrative。

#### `aperospec-visualdirector`

组织身份：

> 视觉统筹 / Graphic Narrative Editorial 岗

职责：

- 只读取 `CDP`
- 输出 `VDP`
- 在不改写内容的前提下，把既有叙事内容转化为视觉海报式页面方向

它不负责改 worldview，不负责重写 narrative，也不负责发明新文案。

#### `Rendering Agent`

组织身份：

> 最终交付执行岗

职责：

- 只读取 `VDP`
- 生成 Hero Image
- 完成最终 `.pptx` 渲染

它不属于当前仓库已落地 Skill，但在组织上属于 `Runtime` 的下游执行角色。

## 3. 汇报与调用关系

### 谁能直接对你汇报

默认只有 `Runtime` 能直接向你汇报完整项目推进结果。

特殊情况下，你可以要求查看某一中间产物，例如：

- `CWP`
- `NWP`
- `CDP`
- `VDP`

但这属于你主动抽查，不代表下游 Skill 可以绕过 `Runtime` 直接与你对接。

### 谁不能直接对你汇报

以下 Skill 默认不能跳过 `Runtime` 直接接管你的任务：

- `aperospec-injection`
- `aperospec-project`
- `aperospec-cinema`
- `aperospec-conceptdeck`
- `aperospec-visualdirector`
- `Rendering Agent`

这些角色都属于专职岗位，不拥有自主接案权。

### 调用顺序

标准调用链路如下：

`你 -> Runtime -> Injection（可选） -> Project -> Cinema -> ConceptDeck -> VisualDirector -> Rendering Agent`

其中：

- 没有现有资产注入时，可跳过 `Injection`
- 有现有资产时，先走 `Injection`
- 任何阶段都不得随意跳级读取更早或更晚的内容

## 4. Artifact 治理规则

这套组织不是靠“大家记住边界”运转，而是靠 artifact 管理运转。

标准内部产物链为：

`CWP -> NWP -> CDP -> VDP -> Final Deck`

### 冻结规则

每一阶段产物生成后立即冻结：

- `CWP` 生成后冻结
- `NWP` 生成后冻结
- `CDP` 生成后冻结
- `VDP` 生成后冻结

冻结的意思是：

- 下游只能读取
- 下游不能重写
- 下游不能修辞性篡改
- 下游不能借视觉或叙事名义倒改上游判断

### 可延续与不可改写

允许延续：

- 在既有产物内继续向下翻译
- 在不改变正式命名的前提下组织节奏
- 在既有内容上进行布局、结构或视觉转译

禁止改写：

- 改上游世界判断
- 改上游核心矛盾
- 改正式命名
- 以“优化表达”为名重写 locked content
- 把后期视觉偏好反向污染前期认知和叙事

## 5. 禁止越权清单

### `Runtime` 禁止事项

- 不得代替你做创意判断
- 不得亲自产出 worldview、narrative、visual design
- 不得因为流程方便而省略边界控制

### `Injection` 禁止事项

- 不得擅自创作新 worldview
- 不得借“整理现有资产”为名改写正式名称

### `Project` 禁止事项

- 不得提前进入 narrative
- 不得产出 page、layout、shot、visual language

### `Cinema` 禁止事项

- 不得重做 root-cause analysis
- 不得提前做 concept deck 或 visual direction

### `ConceptDeck` 禁止事项

- 不得重写 worldview
- 不得发明新 narrative 逻辑替换 `NWP`
- 不得直接进入视觉执行层

### `VisualDirector` 禁止事项

- 不得改名
- 不得发明 slogan 或 fake design language
- 不得借视觉升级之名重构 narrative

### `Rendering Agent` 禁止事项

- 不得脱离 `VDP` 自行改故事
- 不得只输出文本、提示词或概念方案

## 6. 典型工作流

### 模式 A：从零开始

1. 你提出 Topic 或项目方向。
2. `Runtime` 接单并建立执行顺序。
3. `Project` 产出 `CWP`。
4. `Runtime` 冻结 `CWP` 并把它交给 `Cinema`。
5. `Cinema` 产出 `NWP`。
6. `Runtime` 冻结 `NWP` 并把它交给 `ConceptDeck`。
7. `ConceptDeck` 产出 `CDP`。
8. `Runtime` 冻结 `CDP` 并把它交给 `VisualDirector`。
9. `VisualDirector` 产出 `VDP`。
10. `Runtime` 冻结 `VDP` 并交给 `Rendering Agent`。
11. 最终输出 `.pptx`。

### 模式 B：你已经有现成资产

1. 你提供已有 Narrative、现成章节、展项、命名或视觉规范。
2. `Injection` 识别这些内容属于哪一层。
3. `Injection` 锁定不得改动的内容与正式命名。
4. `Injection` 生成 `RIM` 交给 `Runtime`。
5. `Runtime` 按 `RIM` 决定哪些阶段跳过、锁定、辅助生成或继续生成。
6. 后续 Skill 只能在锁定规则内继续执行。

### 模式 C：你中途抽查或要求返工

1. 你指出问题，例如 narrative drift、PPT 感、情绪断裂、视觉越权。
2. `Runtime` 先回看 artifact chain，而不是直接重做全流程。
3. 找到失真发生在哪一层。
4. 只从出错层重新启动，并保留无问题的冻结上游产物。

## 7. 管理结论

你不是在直接指挥 7 个散装 Skill。

你是在管理一家公司式的代理组织：

- 你负责方向与最终裁决
- `Runtime` 负责项目管理与组织控制
- 其它 Skill 负责单工种执行

这套组织成立的前提，不是 Skill 足够聪明，而是边界足够清楚、交接足够严格、冻结规则足够稳定。
