# Deep Thinking — AI Deep Thinking Framework

> English · [中文](./README.md)

Forces AI to think systematically before answering, instead of giving surface-level responses.

---

## The Problem

When you ask AI a complex question, it often responds immediately with a "sounds right" answer — because that answer is the most *probable*, not the most *correct*.

The root cause: **AI's default thinking path is "straight-shot."** Faced with a question, it jumps directly to the most likely answer, without exploring the question's multiple dimensions first. It's like someone answering a quiz before the question is fully read — fast, but often shallow and off-target.

Human experts follow a completely different path when facing complex problems: pause to understand the question → decompose it into manageable parts → consider multiple hypotheses in parallel → challenge their first instinct → verify which one holds → and only then organize a response.

**What this skill does is simple: equip AI with an "expert thinking process," so it thinks through the problem like a seasoned expert before answering.**

---

## Design Philosophy

### Why these 6 steps

Deep Thinking isn't 6 steps pulled out of thin air. It's **the implicit thinking process of human experts, made explicit as an executable framework for AI**.

| Step | Human expert's implicit behavior | AI flaw it addresses |
|:----:|:-------------------------------|:---------------------|
| 1. Restate | "Let me confirm I understood correctly" | AI answers without confirming understanding, missing the point without knowing it |
| 2. Decompose | "This problem is too big, let me break it down" | AI swallows complex problems whole, missing the key points |
| 3. Hypothesize | "There could be several cases, let me consider them all" | AI only gives the most probable answer, ignoring alternatives |
| 4. Challenge | "Is my first instinct right? What if it's the opposite?" | AI's first response is often the surface answer |
| 5. Verify | "Let me test which hypothesis holds" | AI takes things for granted without verification |
| 6. Synthesize | "Let me organize my thoughts before answering" | AI analyzes a lot but can't explain clearly |

**Core insight:** These 6 steps don't burden AI — they **correct its default path** from "straight-line guess" to "networked exploration." Complex problems need the latter.

### Why "Restate" is step one

Many people underestimate restating. But most AI answer errors stem from **misunderstanding** — it didn't understand the question, yet rushed to answer. Restate is the cheapest step with the highest payoff in correctness.

### Design principles

- **Not a rigid template**: These 6 steps define a thinking path, not an answer format. AI doesn't need to output "Step 1... Step 2..." — it just walks the path internally and outputs the synthesized result.
- **Judge first, then decide depth**: Even simple questions pass through the framework first — only after confirming the question is genuinely simple may AI answer quickly. This is a *judgment process*, not an automatic skip.

---

## What is Deep Thinking

Deep Thinking is a structured thinking framework that requires AI to go through 6 steps before producing a final answer:

| Step | Description |
|:----:|:----|
| 1 | Restate — confirm understanding of the question |
| 2 | Decompose — break down into manageable parts |
| 3 | Hypothesize — generate multiple hypotheses, not just one answer |
| 4 | Challenge — question your own assumptions |
| 5 | Verify — test each hypothesis logically |
| 6 | Synthesize — integrate findings into a clear response |

These 6 steps aren't a rigid template — they shift AI's thinking path from "linear" to "networked."

---

## Installation

### As a Claude Code skill

Copy `SKILL.md` into one of the following directories:

**Claude Code skill directory (available across all projects):**
```
# Windows
C:\Users\your-username\.claude\skills\deep-thinking\SKILL.md

# macOS / Linux
~/.claude/skills/deep-thinking/SKILL.md
```

**Agent global skill directory (for cross-environment use):**
```
# Windows
C:\Users\your-username\.agents\skills\deep-thinking\SKILL.md

# macOS / Linux
~/.agents/skills/deep-thinking/SKILL.md
```

> Tip: Replace `your-username` with your actual Windows username, e.g. `C:\Users\zhangsan\.claude\skills\deep-thinking\SKILL.md`

### As a standalone prompt

Copy the content of `自述版.md` into your conversation to activate the framework.

---

## Recommended: Configure as a forced rule

If you want AI to **automatically run deep thinking before every response** (instead of pasting it manually each time), add this to your `CLAUDE.md` or `AGENT.md` rules file:

```markdown
## ⛔ Rule Zero: Deep thinking before everything

**Before doing anything, you must invoke the deep thinking framework, then respond.**

Skipping thinking and responding directly = severe violation
```

> If it feels too heavy to use every time, add an exception: users can say "quick answer" or "simple reply" to skip.

---

## Best paired with: Deep Question

Deep Thinking handles "thinking clearly," while [Deep Question](https://github.com/DataoAI/deep-question) handles "articulating clearly."

In practice, they work in **cycles**:

1. You have a vague idea → use Deep Thinking first to sort out the rough direction and questions
2. Take that direction into a Deep Question conversation to clarify further
3. New questions arise from the conversation → run Deep Thinking again
4. Think → collide → think → collide — each cycle clarifies your thinking one more level

**Think → Collide → Think → Collide** — every cycle makes the thinking clearer.

---

## Related Projects

- [Deep Question](https://github.com/DataoAI/deep-question) — Collaborative thinking framework
- [TTS Storyboard Pipeline](https://github.com/DataoAI/tts-storyboard-pipeline) — AI-powered manga drama production (coming soon)

---

## License

MIT
