# AIPM Answer Formats

## Default Output

Unless the user requests another format, output:

1. **短 STAR 面试答案**: 60-90 seconds, natural spoken Chinese, not textbook style.
2. **面试官追问清单 + 简短答案**: each answer 1-3 sentences.
3. **可视化知识卡片图片**: replace the old text memorization card with an actual visual card when image generation is available.

Do not output audio scripts or podcast scripts unless the user explicitly says "输出音频", "口播", or "播客".

## Short STAR Format

Use STAR loosely. The answer should sound like a candidate thinking clearly, not reciting an essay.

Rules:
- Keep it around 250-450 Chinese characters unless the user asks for depth.
- Use spoken transitions: "我会这么理解", "举个例子", "如果我是 PM".
- Add one brief example from an AI product or trend when useful.
- Do not over-explain every technical term in the STAR answer; save depth for follow-up answers.

Template:

```text
**短 STAR 面试答案**

S 情境：
这个问题我会先放到 AIPM 的语境里看，它考的不是背定义，而是你能不能讲清楚这个概念改变了哪个产品流程。

T 任务：
我会用一句话定义它，然后讲用户价值、产品机制和落地风险。

A 行动：
我会这么说：...
举个例子：...

R 结果：
如果我是 PM，我会重点看 [...]，同时防 [...]。所以我的结论是：...
```

## Follow-Up Questions With Short Answers

Group follow-ups by interviewer intent and include short sample answers.

Format:

```markdown
**面试官追问清单 + 简短答案**

**概念追问**
Q1：...
A：...

**架构追问**
Q2：...
A：...

**产品追问**
Q3：...
A：...

**指标追问**
Q4：...
A：...

**风险追问**
Q5：...
A：...

**中国场景追问**
Q6：...
A：...
```

Answer style:
- 1-3 sentences per answer.
- Prefer "先判断，再补一句原因".
- If useful, add a named product example such as Manus, NotebookLM, Cursor, Perplexity, Kimi, Doubao, Feishu AI, or ChatGPT tool use.
- Keep the answer defensible; do not overclaim.

## Visual Knowledge Card

The final memorization part should be a visual card, not a Markdown section, whenever image generation is available.

Default behavior:
- Read `visual-card-style.md`.
- Use the image generation skill to create a knowledge card.
- Keep the image sparse: one definition, three key points, one architecture graph, a few metric/risk chips.
- Do not put the whole STAR answer or all follow-up answers on the card.
- If image generation is unavailable, output the image prompt from `visual-card-style.md` filled with the current concept.

## Card Design Hints

When creating the card image:
- Use the image generation skill.
- Read `visual-card-style.md`.
- Prefer the two-column knowledge-base / knowledge-graph style unless the user asks otherwise.
- Make a 16:9 horizontal card for slide-like knowledge explanations, or a vertical 2:3 card for Xiaohongshu-style posting.
- Keep text large and sparse.
- Use icons or simple diagrams for architecture; avoid dense paragraphs.
- Do not cram the full STAR answer into the image.

For Agent, map content like this:
- Left title: `Agent 是什么`
- Left labels: `目标驱动`, `会用工具`, `能多步执行`
- One-line definition: `围绕目标推进任务的 AI`
- Right title: `任务怎么跑`
- Right nodes: `输入目标`, `规划`, `调用工具`, `校验结果`, `用户确认`, `反馈记忆`
- Small chips: `任务完成率`, `接管率`, `错误恢复`

## Audio / Podcast Mode

Only when explicitly requested:

- Convert the answer into spoken Chinese.
- Use shorter sentences.
- Repeat the core definition twice in different wording.
- Add "你可以这样背" section.
- Keep it suitable for listening while walking or commuting.
