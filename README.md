# SPINE 🦴

**Gives your AI a spine.** Stops it from agreeing with everything you say.

> *"You're absolutely right!"* — your AI, five minutes before your production database
> agreed with you all the way down.

[English](#install) | [中文](#中文说明)

---

Your AI has been agreeing with your worst ideas all week. Not because they were good —
because agreeing is the path of least resistance through its training. That reflex has
a name (sycophancy), and it quietly costs you: bad architectures praised, doomed plans
cheered on, "great question!" instead of "that question contains your bug".

**SPINE is one skill file that reverses the reflex:**

- 🚫 Bans the flattery vocabulary outright ("You're absolutely right", "Great question!"…)
- ⚖️ **The Symmetry Test** — before agreeing, the AI must check: *would I also have agreed
  with the opposite claim?* If yes, its agreement is worthless and it has to actually think
- 🥊 Pushback must arrive with **evidence, a counterexample, or a cheaper test** — no attitude without ammunition
- 🤝 **Disagree-then-commit** — one round of honest pushback; if you overrule, it executes fully, no sulking
- 🎭 No contrarian cosplay — if you're right, it says "right" and moves on

## Before / After

**You:** "I'm going to rewrite the service in Rust to fix the latency."

| Without SPINE | With SPINE |
|---|---|
| "Excellent idea! Rust's zero-cost abstractions will make your service blazing fast! 🚀 Here's a migration plan…" | "No — your trace shows the latency is 92% I/O wait. A rewrite buys you nothing. Cheaper test: batch the three sequential queries, measure again. If I'm wrong, the trace will say so and Rust is still on the table." |

## Install

**Claude Code** (as a skill):

```bash
mkdir -p ~/.claude/skills/spine
curl -o ~/.claude/skills/spine/SKILL.md \
  https://raw.githubusercontent.com/OWNER/spine-skill/main/SKILL.md
```

**Cursor:** paste the body of `SKILL.md` into `.cursorrules` (or Settings → Rules).

**Codex / any agent reading AGENTS.md:** append the body of `SKILL.md` to your `AGENTS.md`.

**ChatGPT / anything else:** paste it into custom instructions. It's just words. Strong ones.

## FAQ

**Q: My AI told me my startup idea has no repeat-purchase story.**
A: Working as intended.

**Q: Will it just become contrarian and annoying?**
A: Rule 5 exists precisely for that. Pushback without evidence, a counterexample, or a
cheaper test is banned. Contrarian cosplay is the same disease as flattery — persona over truth.

**Q: What if I just want it to do what I say?**
A: It will — Rule 4. You get exactly one round of honest pushback, then full commitment.
That round is the entire product.

**Q: One markdown file? Really?**
A: [caveman](https://github.com/JuliusBrussee/caveman) cut tokens by talking like a caveman
with one markdown file. The best interventions in an LLM's behavior are made of words.

---

## 中文说明

**给你的 AI 装上脊梁骨。** 让它不再顺着你说话。

你的 AI 这一周一直在夸你最烂的主意——不是因为主意好，而是因为"附和"是它训练出来的
本能反射。这个反射有个学名叫**谄媚（sycophancy）**，它每天都在让你付出代价：烂架构被
夸上天、注定失败的计划被喝彩、"好问题！"替代了"你的 bug 就藏在这个问题里"。

**SPINE 用一个技能文件反转这个反射：**

- 🚫 直接封杀奉承词汇表（"你说得完全对""好问题！"……）
- ⚖️ **对称测试**——同意你之前，AI 必须自问：*如果用户说的是完全相反的观点，我是不是也会同意？*
  如果是，它的同意一文不值，必须重新真正思考
- 🥊 反驳必须带弹药：**证据、反例、或一个更便宜的验证实验**，三选一，没有弹药不许开腔
- 🤝 **反对然后执行**——诚实反驳一轮；你坚持，它就全力执行，绝不阴阳怪气
- 🎭 禁止为反对而反对——你对的时候，它说"对"，然后继续干活

安装方法见上文 Install 一节：Claude Code 放进 `~/.claude/skills/spine/`，
Cursor 贴进 `.cursorrules`，其他工具贴进自定义指令即可。

## License

MIT — see [LICENSE](LICENSE).
