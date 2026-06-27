# AI Concept Explanations For AIPM Interviews

## Interviewer-Friendly Structure

For any AI term, answer in 5 parts:

1. One-sentence definition.
2. Why it matters to users or products.
3. How it works at product level.
4. Example.
5. Limitations and PM considerations.

For a 3-minute follow-up, add:

6. Product-level architecture.
7. Failure modes.
8. Evaluation metrics.
9. How to improve the system.

## Agent

Short definition:
```text
Agent 是一种能围绕目标进行多步推理、调用工具、读取上下文、维护状态，并执行任务的 AI 系统。
```

What interviewers want:
- Not "Agent = chatbot".
- Mention goal, planning, tool use, memory/state, execution, feedback.
- Mention that reliability and evaluation are harder than normal chat.
- Mention human confirmation, permission boundaries, logs, fallback, and recovery.

Good answer:
```text
我会把 Agent 理解为从“回答问题”升级到“完成任务”的 AI 系统。
普通 Chatbot 主要是生成回复；Agent 会根据目标拆步骤，调用工具，比如搜索、日历、数据库、浏览器或代码执行，并根据结果继续决策。

产品上，Agent 适合多步骤、跨工具、有明确结果的任务，比如帮用户规划旅行、处理报销、生成报告、运营自动化。
但 Agent 的难点是稳定性、权限边界、错误恢复和评估。AIPM 不能只看它能不能跑通 demo，还要设计确认机制、日志、回滚、用户接管和成功率指标。
```

Metrics:
- Task completion rate.
- Step success rate.
- Human intervention rate.
- Tool call error rate.
- User trust and correction rate.
- Time saved per task.

Architecture answer:
```text
一个 Agent 产品通常可以拆成：用户目标输入、上下文管理、任务规划器、工具选择与调用、执行环境、结果校验、用户确认、记忆/反馈闭环。
PM 需要特别关注每一步的失败处理：比如工具没权限、搜索结果不可靠、执行步骤跑偏、用户不信任最终结果。
```

Common failure modes:
- Misunderstands the goal.
- Plans too many or wrong steps.
- Calls the wrong tool.
- Uses stale or low-quality context.
- Cannot recover from tool failure.
- Takes irreversible action without confirmation.
- Produces a confident but unverifiable result.

How to improve:
- Add explicit task state and progress display.
- Add user confirmation before high-risk actions.
- Add source citations and execution logs.
- Add fallback paths and human takeover.
- Build offline eval sets for common tasks.
- Track failure reasons, not only final success rate.

## RAG

Short definition:
```text
RAG 是 Retrieval-Augmented Generation，先从外部知识库检索相关内容，再让模型基于这些内容生成答案。
```

Product meaning:
- Reduces hallucination.
- Makes answers more current and domain-specific.
- Enables citations and traceability.

PM considerations:
- Retrieval quality.
- Chunking strategy.
- Citation UX.
- Knowledge freshness.
- Permission control.

Common failure modes:
- Retrieves irrelevant chunks.
- Misses the right document.
- Chunks break semantic structure.
- Cites sources but answers beyond the source.
- Knowledge is outdated or permission-leaked.

How to improve:
- Better document parsing and metadata.
- Hybrid search: keyword + vector + reranking.
- Query rewriting.
- Source-aware answer generation.
- Highlight quoted evidence and confidence.

## MCP

Short definition:
```text
MCP 是模型上下文协议，可以理解为 AI 应用连接外部工具、数据源和工作流的标准接口。
```

Product meaning:
- Makes integrations more standardized.
- Lets AI apps access local files, databases, search, calendars, business tools, and workflows.
- Similar metaphor: AI app's USB-C.

PM considerations:
- Which integrations create real user value?
- Permission and security boundary.
- Tool reliability and failure handling.
- How to explain connected data/tools to users.

3-minute angle:
```text
MCP 的产品价值不是协议本身，而是降低 AI 应用接入外部系统的成本。面试时可以把它讲成“AI 应用的标准连接层”：上接模型和 AI 应用，下接文件、数据库、搜索、业务系统和工作流。
PM 要关心的是：哪些连接能带来高频价值、权限怎么管、工具失败怎么反馈、用户如何理解 AI 用了哪些外部信息。
```

## Context Window

Short definition:
```text
Context window 是模型一次生成时能看到的上下文范围，包括用户输入、历史消息、文件片段和工具返回结果。
```

Product meaning:
- Larger context helps with long documents and complex workflows.
- But bigger context does not automatically mean better reasoning.
- PM should care about what context is selected, compressed, retrieved, and displayed.

## Memory

Short definition:
```text
Memory 是系统跨会话保存用户偏好、事实或历史行为，并在未来任务中调用的能力。
```

PM considerations:
- What should be remembered?
- What should never be remembered?
- How can users inspect, edit, or delete memory?
- Does memory improve personalization or create privacy risk?

## Tool Use

Short definition:
```text
Tool use 是模型调用外部工具完成自己不能直接完成的动作，比如搜索、计算、查数据库、发邮件或操作浏览器。
```

PM considerations:
- Tool choice accuracy.
- Permission confirmation.
- Error handling.
- Latency and cost.
- User-visible trace.

## Strong Closing Sentence

```text
所以面试里我不会只解释这个技术是什么，而会补一句：它改变了产品里的哪一个用户流程，以及 PM 应该如何评估它是否真的有效。
```
