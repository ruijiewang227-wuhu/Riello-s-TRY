# Visual Knowledge Card Style

Use this reference when the user asks for a visual knowledge card, 图文卡片, 知识卡片, "做成图", or when `answer-formats.md` requests the final visual memorization card.

## Default Visual Style

Create a clean, playful knowledge-card layout inspired by educational slides:

- Light lavender background.
- Deep purple rounded title bars.
- Two-column composition.
- Left side: "Knowledge base" concept card, book/manual stack, or structured note object.
- Right side: "Knowledge graph" relationship diagram with connected nodes.
- Accent colors: deep purple, lavender, teal, warm yellow, white.
- Bottom strip: geometric blocks with semicircles, triangles, and rectangles.
- Small sparkles or dots may be used sparingly.
- Overall feeling: clear, friendly, structured, modern learning aid.

## Palette

- Background: `#EFE7F7` or soft lavender.
- Main purple: `#5E2D79`.
- Light purple: `#B276D4`.
- Teal: `#63BDB7`.
- Yellow: `#F2C14E`.
- White: `#FFFFFF`.

## Layout

For a horizontal card:

```text
[Top left title pill]                         [Top right title pill]
Knowledge base                                Knowledge graph

      [book/card illustration]                [node-link diagram]
      3 key bullets / formula                 central concept + branches

[bottom geometric strip across full width]
```

For a vertical card:

```text
[Main title pill]
[Concept explanation card]
[Mini graph / architecture flow]
[Metrics + risks chips]
[bottom geometric strip]
```

## Content Mapping For AIPM

Map interview content into the layout:

- Left "Knowledge base":
  - One plain-language definition.
  - 3 key points.
  - 1 tiny example product only if it fits.

- Right "Knowledge graph":
  - Architecture or relationship map.
  - Input -> context -> planner -> tools -> output.
  - Metrics and risks as small chips or branch nodes.

## Text Rules

- Use very short text. Prefer 4-8 words per label.
- Use big title text and sparse labels.
- Do not put the full STAR answer on the image.
- Put the detailed STAR and follow-up answers in chat; the image is only the memory card.
- Use Chinese labels by default, with short English keywords only when helpful.
- If exact Chinese text rendering may be unreliable, keep Chinese labels short and simple.

## Image Prompt Template

```text
Create a clean horizontal educational knowledge card, light lavender background, deep purple rounded title pills, two-column layout.
Left title pill: "[left title]"; right title pill: "[right title]".
Left side shows a deep purple book/manual or stacked card illustration labeled "[concept]"; include one short definition "[definition]" and three short Chinese labels: "[point 1]", "[point 2]", "[point 3]".
Right side shows a knowledge graph / architecture node diagram with yellow nodes and purple/teal connecting lines, labeled with short Chinese terms: "[node 1]", "[node 2]", "[node 3]", "[node 4]", "[node 5]", "[node 6]".
Add 2-3 small chips for metrics or risks: "[chip 1]", "[chip 2]", "[chip 3]".
Bottom has a decorative geometric strip with teal, yellow, purple, and lavender shapes.
Modern friendly learning slide style, crisp vector-like illustration, high readability, large sparse text, no watermark, no clutter.
```

## Example For Agent

Left title: `Agent 是什么`
Right title: `任务怎么跑`

Left labels:
- `目标驱动`
- `会用工具`
- `能多步执行`

Definition:
- `围绕目标推进任务的 AI`

Right nodes:
- `输入目标`
- `规划`
- `调用工具`
- `校验结果`
- `用户确认`
- `反馈记忆`

Chips:
- `任务完成率`
- `接管率`
- `错误恢复`
