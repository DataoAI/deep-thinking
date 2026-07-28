# Deep Thinking — AI深度思考框架

> 🌐 中文 · [English](./README.en.md)（待翻译）

让AI在回答任何问题之前，先经过一个系统化的深度思考过程，而不是直接给出表层答案。

---

## 痛点 / Problem

当你问AI一个问题，它往往会立刻给出一个"听起来合理"的答案。但真正复杂的、需要深度分析的问题，第一反应往往是错的。你需要的是AI像一个人一样——先停下来想一想，再回答。

这个技能就是解决这个问题的。

---

## 什么是Deep Thinking

Deep Thinking 是一个结构化的思考框架，要求AI在输出最终回答之前，依次经过6个步骤：

| 步骤 | 英文 | 说明 |
|:----:|:----|:----|
| 1 | Restate | 重述问题，确认理解正确 |
| 2 | Decompose | 分解问题，拆成可处理的部分 |
| 3 | Hypothesize | 多假设并行，不只找"一个答案" |
| 4 | Challenge | 质疑初始假设，推翻自己的第一反应 |
| 5 | Verify | 测试与验证，用逻辑检验哪个假设站得住 |
| 6 | Synthesize | 整合结论，把分析过程变成清晰的回答 |

这6步不是硬性的模版，而是让AI的思考路径从"直线"变成"网状"。

---

## 安装方式 / Installation

### 作为Claude Code技能

将 `SKILL.md` 放入 `~/.claude/skills/deep-thinking/` 目录即可。

### 作为独立提示词

直接将 `自述版.md` 的内容复制到对话中，AI会按照框架深度思考。

---

## 建议：配置为强制执行

如果你希望AI**每次响应前都自动执行深度思考**（而不是每次手动粘贴），可以在你的 `CLAUDE.md` 或 `AGENT.md` 规则文件中加入以下内容：

```markdown
## ⛔ 第零条铁律：深度思考先于一切

**做任何事之前，必须先调用深度思考框架，再输出回答。**

跳过思考直接执行 = 严重违规
```

> 如果觉得每次都用太繁琐，也可以加一条例外规则：用户说"快速回答"或"简单回复"时可以跳过。

---

## 最佳配合：思路碰撞（Deep Question）

Deep Thinking 负责"想清楚"，[思路碰撞（Deep Question）](https://github.com/DataoAI/deep-question) 负责"说明白"。

实际使用中，它们是**循环配合**的：

1. 你有一个模糊的想法 → 先用 Deep Thinking 自己深度思考，理出大概方向和问题
2. 拿着这个方向去跟AI思路碰撞，在对话中进一步澄清
3. 碰撞中产生新的问题 → 再让AI深度思考一轮
4. 再碰撞、再思考...

**思考→碰撞→再思考→再碰撞**，每一次循环，思路就更清晰一层。

---

## 项目关联 / Related Projects

- [Deep Question（思路碰撞）](https://github.com/DataoAI/deep-question) — 深度问答碰撞框架
- [TTS分镜流程](https://github.com/DataoAI/tts-storyboard-pipeline) — AI漫剧生产管线（即将发布）

---

## License

MIT