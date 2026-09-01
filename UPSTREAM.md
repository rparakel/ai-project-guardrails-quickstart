# Sources, Influences, and Reuse

Created and consolidated by **Arpine Arakelyan**.

The repository contains independently written instructions. It does not vendor third-party code, prompts, word lists, components, or evaluation configurations. The projects below informed the structure or the problems covered; their wording was not copied into this repository.

## Agent instructions and engineering

| Source | What it informed | Reuse status |
| --- | --- | --- |
| [AGENTS.md](https://github.com/agentsmd/agents.md) | A predictable repository-level location for agent instructions | Format reference only; no text copied |
| [12-Factor Agents](https://github.com/humanlayer/12-factor-agents) | Bounded context, tools as structured outputs, controlled state, and human approval | Conceptual comparison only; no text or images copied |
| [SWE-agent](https://github.com/SWE-agent/SWE-agent) | Inspect, edit narrowly, execute, and use environment feedback | Conceptual comparison only; no code or prompt copied |
| [Fabric](https://github.com/danielmiessler/Fabric) | Small, task-focused prompt patterns rather than one universal prompt | Conceptual comparison only; no patterns copied |
| [Model Context Protocol](https://modelcontextprotocol.io/) | Tool discovery, transport, and permission boundaries | Official specification reference; no implementation copied |

The `12-factor-agents` prose and images are CC BY-SA 4.0 and its code is Apache 2.0. This repository does not adapt or include that material, which avoids importing its share-alike terms into the MIT-licensed files.

## Evaluation and security

| Source | What it informed | Reuse status |
| --- | --- | --- |
| [Promptfoo](https://github.com/promptfoo/promptfoo) | Test cases with inputs, assertions, and repeatable pass/fail outcomes | Structure reference only; no configuration or code copied |
| [OWASP Top 10 for LLM Applications](https://genai.owasp.org/llm-top-10/) | Prompt injection, sensitive information, excessive agency, and output-handling risks | Security reference only; no standard text copied |
| [OWASP Application Security Verification Standard](https://owasp.org/www-project-application-security-verification-standard/) | Separating advisory instructions from runtime verification | Security reference only; no requirements copied |
| [HumanLayer](https://github.com/humanlayer/humanlayer) | Human approval before consequential tool actions | Conceptual comparison only; no code copied |

## Product design

| Source | What it informed | Reuse status |
| --- | --- | --- |
| [WCAG 2.2](https://www.w3.org/TR/WCAG22/) | Accessibility outcomes for contrast, focus, input, and motion | Standards reference; no normative text copied |
| [shadcn/ui](https://github.com/shadcn-ui/ui) | Reusable component variants and design tokens | Product comparison only; no components copied |
| [Radix Primitives](https://github.com/radix-ui/primitives) | Accessible component behavior | Product comparison only; no components copied |
| [Front-End Checklist](https://github.com/thedaviddias/Front-End-Checklist) | A manual pre-publish review for non-technical builders | Checklist concept only; every item here was independently written |
| [Anti-AI Slop Writing](https://github.com/jalaalrd/anti-ai-slop-writing) | Human writing checks for stock language, repetition, fabricated specificity, formatting, and voice | Source reviewed; the writing skill was independently rewritten with no text or word lists copied |

## Free-builder facts

`FREE-TOOLS.md` links directly to the official pricing, credit, publishing, and export documentation for Base44, Dify, Google AI Studio, Lovable, and Replit. Those facts are time-sensitive and include a verification date. No platform documentation is reproduced beyond short factual summaries.

## Publishing rule

Before accepting future contributions that adapt outside material:

1. record the exact repository and source file;
2. verify the license from the repository, not a search snippet;
3. identify copied or modified material precisely;
4. retain required notices; and
5. exclude material whose terms are incompatible with this repository's MIT license unless the repository license and distribution plan are changed first.
