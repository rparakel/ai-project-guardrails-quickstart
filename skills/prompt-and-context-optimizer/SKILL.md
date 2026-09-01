---
name: prompt-and-context-optimizer
description: Turn a vague, conflicting, oversized, or repeatedly failing project request into a focused execution brief while minimizing questions and context. Do not use for requests that are already clear.
---

# Prompt and Context Optimizer

Clarify the work without turning it into a prompt-engineering exercise. Preserve the user's desired outcome and reduce only what is vague, conflicting, unnecessary, or too expensive for the stated project.

## First decide whether optimization is needed

Do not rewrite a clear request. Correct spelling, formatting, and harmless omissions silently.

Optimize when at least one of these is true:

- the expected result or primary user is unclear;
- requirements conflict;
- the request would trigger a large build without completion criteria;
- a tool, framework, data source, or integration is assumed but unavailable;
- the same request has produced repeated failed or unwanted results;
- the scope does not fit the time, credit, or technical limits.

## Build the internal brief

Extract:

```text
Goal: the outcome that must exist
User: who uses it and for what decision or action
Context: only the files, facts, and constraints needed now
Output: the required artifact, format, or behavior
Boundaries: cost, privacy, permissions, time, and excluded work
Done: observable checks that prove completion
```

Do this internally unless the user asks to see the rewritten prompt or the brief is needed for approval or handoff.

## Clarification threshold

- Ask only when the answer would materially change architecture, data handling, privacy, permissions, paid services, or core behavior.
- Ask no more than three short questions in one turn.
- Offer a reasonable default with each question when possible.
- Do not ask about details the existing project or files can answer.
- For a minor unknown, state one safe, reversible assumption and proceed.
- In a non-interactive run, record the assumption and choose the least destructive option.

## Reduce context and cost

- Remove duplicated instructions and stale background.
- Separate information needed now from material that can be retrieved later.
- Request targeted files or sections rather than entire repositories or document collections.
- Prefer one complete workflow over several partial features.
- Combine related edits; separate unrelated tasks.
- Define a retry limit and stop condition before a tool-heavy run.

## Replace vague iteration

Translate “make it better,” “fix everything,” or “make it professional” into observable defects: unclear hierarchy, missing error state, unsupported claim, failed test, inconsistent component, slow response, malformed output, or another specific issue supported by evidence.

When the user requests a rewritten prompt, return a compact build brief with explicit completion criteria. Do not add role-play, motivational language, duplicated rules, or a long preamble.

