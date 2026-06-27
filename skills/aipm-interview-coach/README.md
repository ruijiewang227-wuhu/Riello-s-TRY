# AIPM Interview Coach

这是一个面向 AI 产品经理面试的 Codex skill。它的目标不是帮你背一堆概念，而是把 AI 产品、技术名词和产品分析问题，整理成面试官愿意继续追问、你也能短时间讲清楚的回答。

## 它适合解决什么问题

- 解释 AI 概念：Agent、RAG、MCP、Context Window、Tool Use、Memory、Multimodal 等。
- 准备 3 分钟技术追问：架构怎么讲、失败模式是什么、指标怎么设计、怎么改进。
- 分析 AI 产品好在哪里：Manus、NotebookLM、ChatGPT、豆包、Kimi、Perplexity、Cursor、飞书妙记、小红书等。
- 比较不同产品差异：用户场景、上下文能力、工作流深度、信任机制、生态集成、商业模式。
- 输出短 STAR 面试答案：自然、口语化、能在 60-90 秒内讲完。
- 生成面试官追问清单：每个追问配 1-3 句简短答案。
- 生成图文知识卡片：把复杂概念压缩成一张可背诵、可复习的视觉卡片。

## 使用方式

直接在 Codex 里这样提问：

```text
用 aipm-interview-coach 给我解释 Agent，按 3 分钟追问来。
```

```text
用 aipm-interview-coach 给我解释 RAG，要短 STAR、追问清单和图文背诵卡片。
```

```text
用 aipm-interview-coach 分析 NotebookLM 好在哪里，要贴合 AIPM 面试。
```

```text
用 aipm-interview-coach 对比 Manus、ChatGPT、Kimi 和 Perplexity 的产品差异。
```

## 默认输出结构

### 1. 短 STAR 面试答案

不是传统长篇 STAR，而是适合面试现场说出口的版本：

- 先一句话判断或定义。
- 再讲用户场景和痛点。
- 接着讲产品机制或 AI 机制。
- 最后补指标、风险和 PM 视角。

目标长度：大约 60-90 秒。

### 2. 面试官追问清单

通常会覆盖：

- 概念追问：这个东西和普通聊天有什么区别？
- 架构追问：系统大概怎么搭？
- 产品追问：适合什么场景，不适合什么场景？
- 指标追问：怎么证明它有效？
- 风险追问：会出什么错，怎么兜底？
- 中国场景追问：在国内产品和 B 端落地里要注意什么？

每个答案控制在 1-3 句，方便临场使用。

### 3. 图文知识卡片

默认会把最后的背诵内容做成视觉卡片，而不是一大段文字。

卡片风格：

- 浅紫背景。
- 深紫圆角标题条。
- 左右双栏。
- 左边是 `Knowledge base`：定义、三要点、例子。
- 右边是 `Knowledge graph`：架构图、流程图、关系节点。
- 底部有紫色、黄色、青绿色几何装饰条。

卡片只放短标签，不塞完整 STAR。

## 回答风格

这个 skill 默认使用中文，语气要像一个清醒的 AIPM 候选人：

- 不只背定义，要讲“这个技术改变了哪个用户流程”。
- 不空喊“提升效率”，要说明提升了哪一步、用什么指标验证。
- 不把 Agent、RAG、MCP 讲成玄学，要能落到架构、工具、数据、权限、反馈闭环。
- 不过度包装个人经历，除非用户明确要求加入项目背景。
- 遇到具体产品或最新市场信息，要先查资料并引用来源，不能胡编。

## 常用回答框架

### AI 概念解释

```text
一句话定义
为什么对用户或产品有价值
产品层面怎么工作
举一个产品例子
局限和 PM 需要关注的点
```

3 分钟追问时继续展开：

```text
产品架构
失败模式
评估指标
改进方案
```

### 产品好在哪里

```text
目标用户是谁
核心痛点是什么
产品进入了哪个工作流
AI 在哪里产生杠杆
差异化来自哪里
指标和风险是什么
```

### 产品对比

```text
核心任务
输入和上下文
工作流深度
输出质量和信任
工具与生态集成
用户与分发
商业模式和壁垒
弱点与失败模式
```

## 文件结构

```text
aipm-interview-coach/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
└── references/
    ├── ai-concepts.md
    ├── answer-formats.md
    ├── product-analysis.md
    ├── research-rules.md
    └── visual-card-style.md
```

## 可以继续补充的方向

- 增加更多 AI 概念：Function Calling、Workflow、Evaluation、Long Context、Fine-tuning、Embedding、Rerank、多模态。
- 增加产品案例库：Manus、NotebookLM、Cursor、Perplexity、Kimi、豆包、飞书 AI、小红书搜索/推荐。
- 增加国内 AIPM 面试题库：B 端 AI、C 端 AI、内容社区、办公协同、教育学习、AI Agent 平台。
- 增加更固定的图文卡片模板：横版知识卡、竖版小红书卡、面试速记卡、概念对比卡。

