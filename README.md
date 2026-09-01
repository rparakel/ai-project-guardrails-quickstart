# AI Project Guardrails

Practical instructions for building a small AI app or agent without wasting prompts, inventing facts, exposing private data, or shipping an unfinished demo.

This is the lightweight showcase version. It guides model behavior; it does not install runtime security infrastructure.

## New to AI terminology?

Read [AI Jargon, in Plain English](https://rparakelyan.com/guides/ai-jargon-in-plain-english/). It explains terms such as tokens, context windows, APIs, models, and agents for people who work with AI but do not plan to become machine-learning engineers.

## Start in one minute

1. Add this repository to your project. If your builder cannot read project files, upload the Markdown files once and put [`AI-GUARDRAILS.md`](AI-GUARDRAILS.md) in its persistent instructions.
2. Tell the builder what you want to create. Use the short brief below if you need a starting point.

That is the complete workflow. The AI chooses and reads the relevant skill when the task needs it. Before it calls the project finished, it selects and runs the applicable checks from [`EVALS.md`](EVALS.md), records the evidence, and reports anything it could not verify.

### Showcase build brief

Replace the bracketed text and paste this into the builder you chose:

```text
Build the smallest working version of [describe the project and its user].

It needs one clear input, one AI workflow, one useful structured output,
missing-information handling, three test cases, and a shareable result.

Use synthetic data. Do not send messages, change external systems, expose
secrets, or activate paid features without my approval. Ask only when a
missing answer would materially change the product, privacy, security, or cost.
```

## Add the guardrails to your AI tool

Open [`AI-GUARDRAILS.md`](AI-GUARDRAILS.md), copy all the text, and add it to the place shown below. You only need to do this once for each project.

If you cannot find the exact place, look for a section named **Instructions**, **Knowledge**, **Rules**, or **System Instructions**.

| Tool | Where to add the text |
| --- | --- |
| ChatGPT | Project instructions |
| Claude Projects | Project instructions |
| Claude Code | Save it as `CLAUDE.md` in the main project folder |
| Codex | Save it as `AGENTS.md` in the main project folder |
| Cursor | Save it as `AGENTS.md` in the main project folder, or add it to Project Rules |
| Base44 | Agent Guidelines → Instructions |
| Dify | The instructions box for your agent or workflow |
| Lovable | Project Knowledge |
| Google AI Studio | System Instructions or Build context |
| Replit | Save it as `replit.md` in the main project folder, or add it to Agent instructions |
| Another builder | Its project instructions, knowledge, or rules section |

This file guides the AI, but it cannot control what your tool can access or do. Use your tool's permission and approval settings for that.

## What the AI loads

Keep the core guardrails active and make the `skills/` folder available to the project. The AI loads the relevant file itself:

| Work detected | File the AI reads |
| --- | --- |
| Emails, reports, summaries, outreach, or interface copy | [`skills/human-writing/SKILL.md`](skills/human-writing/SKILL.md) |
| Interface or design-system work | [`skills/product-design/SKILL.md`](skills/product-design/SKILL.md) |
| A vague, conflicting, or oversized request | [`skills/prompt-and-context-optimizer/SKILL.md`](skills/prompt-and-context-optimizer/SKILL.md) |
| An AI feature, workflow, or agent | [`skills/ai-app-agent-engineering/SKILL.md`](skills/ai-app-agent-engineering/SKILL.md) |

The AI does not load all four by default. For this showcase, it normally uses the core plus AI app and agent engineering. It adds writing, design, or VC safety only when that work appears.

If the platform cannot access a referenced file, the AI must say so. It may continue with the core rules, but it cannot claim that the unavailable skill or its evaluations were applied.

## For this showcase

- Start with one workflow that can run from input to result.
- Use fake or anonymized data.
- Keep external actions in preview or draft mode.
- Do not add login, payments, a CRM, or an MCP unless the demonstration cannot work without it.
- Show missing information instead of filling gaps with plausible details.
- Let the AI test a normal input, a weak input, and an incomplete input.
- The AI should test the published link from an unauthenticated context when the platform allows it. Otherwise, it must mark that check as blocked rather than claiming the link works.

If you have not chosen a builder, [`FREE-TOOLS.md`](FREE-TOOLS.md) explains what each free tier can realistically finish and where the limits are.

## What these files can and cannot do

They can reduce repeated context, weak prompts, unsupported claims, uncontrolled retries, generic writing, and careless design. They cannot guarantee factual accuracy, block a shell command, enforce data access, prevent every prompt-injection attack, or make a prototype production-ready.

Use platform permissions and sandboxing for real enforcement. Use legal, privacy, and security review before handling live confidential or financial data.

## Token use

The core file is designed to stay under roughly 1,000 tokens. Optional skills are lazy-loaded. A normal task should use the core plus no more than one skill; an AI/VC task may also load the relevant safety reference.

Measured with OpenAI's `o200k_base` tokenizer:

| File | Approximate tokens |
| --- | ---: |
| Core guardrails | 986 |
| Human writing | 749 |
| Product design | 741 |
| Prompt and context optimizer | 563 |
| AI app and agent engineering | 1,185 |
| Non-technical checklist | 691 |
| VC showcase safety | 653 |

Other models tokenize the same text differently. Treat these as measured estimates, not provider billing guarantees.

## License and source notes

This repository is available under the [MIT License](LICENSE). [`UPSTREAM.md`](UPSTREAM.md) records the projects and standards that informed it, including the anti-AI-slop writing work shared with the Venture Institute group.
