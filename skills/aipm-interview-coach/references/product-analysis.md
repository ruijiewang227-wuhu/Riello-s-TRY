# Product Analysis For AIPM Interviews

## The Interviewer Usually Wants

- User insight: who has the pain, how frequent, how painful, why now.
- Workflow fit: where the product enters the user's existing process.
- AI fit: why AI is suitable, and what non-AI baseline it beats.
- Differentiation: why this product is better or worse than alternatives.
- Metrics: how to prove it works.
- Risks: what can go wrong and how the PM would manage it.
- China fit: local scenarios, local competitors, distribution, compliance, trust, and payment/enterprise procurement.

## Framework: Why Is This Product Good?

Answer with 6 layers:

1. **Target User**
   - Who is it for?
   - Is the user expert, beginner, team, creator, operator, student?

2. **Core Pain**
   - What task is slow, hard, uncertain, expensive, boring, or high-stakes?
   - Is the pain frequent enough to create retention?

3. **Product Moment**
   - What is the "aha moment"?
   - What does the user get in the first 1-3 minutes?

4. **AI Leverage**
   - Does AI understand, generate, decide, retrieve, automate, or personalize?
   - Does the product provide context, tools, memory, or feedback loops?

5. **Moat / Differentiation**
   - Better workflow?
   - Better data?
   - Better distribution?
   - Better trust and evaluation?
   - Better domain depth?

6. **Metrics and Risks**
   - Activation: first successful output.
   - Retention: repeated weekly use.
   - Quality: acceptance rate, edit rate, task success.
   - Efficiency: time saved, steps reduced.
   - Trust: error rate, user correction rate.
   - Risk: hallucination, privacy, over-automation, unclear accountability.

## Product Comparison Framework

Use this when comparing Manus, NotebookLM, ChatGPT, Doubao, Kimi, Perplexity, Cursor, Feishu Minutes, Xiaohongshu, or similar products.

Compare across 8 axes:

1. **Core Job**
   - What job does each product help users finish?
   - Is it answering, researching, creating, coding, automating, summarizing, or distributing?

2. **Input and Context**
   - What context can the product ingest: chat history, files, webpages, repo, enterprise docs, audio/video, user behavior?
   - Does it support long context, RAG, memory, multimodal input, or source citation?

3. **Workflow Depth**
   - Is it a single-turn answer, multi-turn assistant, research workflow, agent workflow, or embedded productivity tool?

4. **Output Quality and Trust**
   - Does it cite sources?
   - Can users verify or edit results?
   - Does it preserve structure, formatting, or traceability?

5. **Tool and Ecosystem Integration**
   - Browser, search, calendar, file system, code editor, enterprise docs, collaboration suite, publishing platform.

6. **User Segment and Distribution**
   - Global vs China, consumer vs enterprise, professional vs general user.
   - Distribution through app, browser, workspace suite, creator ecosystem, developer ecosystem.

7. **Business Model and Moat**
   - Subscription, enterprise seats, API, ecosystem lock-in, data loop, workflow lock-in, brand, community, model capability.

8. **Weakness and Failure Mode**
   - Hallucination, shallow retrieval, latency, high cost, poor source quality, weak integration, privacy risk, unclear ROI.

## China Context Checklist

- Does the product fit WeChat/DingTalk/Feishu-style collaboration habits?
- Does it handle Chinese documents, policies, local platforms, and local search well?
- Is there a domestic competitor with better distribution or compliance?
- Does the use case depend on external websites that may be inaccessible or unstable in China?
- For B-side products, who buys: user, team lead, IT, procurement, or business owner?
- For C-side products, what drives retention: habit, content, identity, community, or utility?

## 60-Second Answer Template

```text
我觉得这个产品好的地方有三点。

第一，它切中了一个明确场景：[用户]在[任务]里经常遇到[痛点]。
第二，它不是把 AI 当聊天入口，而是嵌入到[工作流]，帮用户完成[具体动作]。
第三，它的壁垒可能来自[数据/场景/分发/反馈闭环/领域 know-how]。

如果我是 PM，我会重点看三个指标：
[激活指标]、[质量指标]、[留存或复用指标]。
同时也要控制[主要风险]，比如[幻觉/隐私/成本/延迟/可解释性]。
```

## Example: Analyze NotebookLM

```text
NotebookLM 好的地方不是“能总结文档”，而是把 AI 放进了学习和研究工作流。

用户痛点是：资料很多、上下文分散、读完难以形成结构化理解。
它的产品价值是：基于用户上传资料回答问题、生成摘要和音频，使 AI 的回答有明确来源。
AI fit 在于长文理解、检索、总结和转化表达。

我会看：上传资料后的首次有效回答率、摘要采纳率、用户是否持续上传资料、用户对引用来源的信任度。
风险是资料隐私、引用准确性和生成内容过度简化。
```

## Common Mistakes

- Only saying "界面好看".
- Only saying "用了大模型".
- Ignoring why the user will come back.
- Ignoring how quality is measured.
- Ignoring bad cases and trust.
- Comparing products by feature list only, without explaining the user job and workflow depth.
- Claiming product facts without sources.
