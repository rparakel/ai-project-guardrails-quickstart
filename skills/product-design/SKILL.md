---
name: product-design
description: Design or review interfaces for clear hierarchy, consistent components, responsive behavior, accessibility, and a product-specific visual direction. Use for screens, flows, design systems, or UI implementation.
---

# Product Design

Design for the user's main task before decorating the interface. Reuse the project's current design language when one exists; improve inconsistencies instead of replacing working components without a reason.

## Establish the direction

Infer these from the product and existing files when possible:

- primary user and the decision or action they came to complete;
- product type and information density;
- visual character, such as editorial, operational, calm, technical, or consumer;
- constraints imposed by the builder, framework, brand, or current component library.

Ask a question only when a missing answer would materially change the layout or brand. Otherwise, choose one coherent direction and state it briefly.

## Use a system, not isolated styling

- Reuse maintained native components before introducing a new library.
- Use semantic tokens for background, surface, text, border, accent, success, warning, and danger.
- Define a small type scale, spacing scale, radius set, elevation rule, and motion rule.
- Use one grid and consistent container widths. Align related labels, values, and actions.
- Give components named variants and sizes rather than page-specific overrides.
- Keep primary actions visually scarce. A screen should not have several competing “main” buttons.
- Use icons only when their meaning is familiar or paired with a label.

Shadcn/ui, Radix, Material, and builder-native systems are options, not automatic choices. Select the system that fits the existing stack and maintenance needs.

## Design the full state model

For each important workflow, cover:

- initial and first-use state;
- loading or processing state with useful progress;
- empty state that explains the next action;
- field-level validation;
- recoverable error with a retry path;
- success with a clear next step;
- disabled and permission-limited states;
- long, missing, and unexpected content.

Do not show fabricated analytics or decorative data just to fill the screen. Use labeled sample data in a showcase.

## Accessibility and responsiveness

- Use semantic elements and real labels. Do not rely on placeholder text as the label.
- Keep keyboard order logical and focus visible.
- Meet WCAG 2.2 AA contrast for normal text and interactive states where practical.
- Do not communicate status through color alone.
- Respect reduced-motion preferences and avoid motion that blocks interaction.
- Keep touch targets usable and controls reachable on small screens.
- Test narrow mobile, ordinary laptop, and wide desktop layouts. Do not merely shrink the desktop view.

## Avoid generic AI styling

Do not default to a dark dashboard, purple-blue gradient, glowing card grid, glass effect, oversized hero copy, decorative chart, or chat bubble because the product uses AI. Use any of these only when it fits the product and makes the task easier.

Prefer hierarchy, whitespace, precise typography, useful states, and one recognizable visual idea over effects. Avoid card containers when grouping, spacing, or a divider already communicates the relationship.

## Completion check

Before calling the interface complete:

1. Walk through the primary task on mobile and desktop.
2. Inspect loading, empty, error, success, focus, hover, and disabled states.
3. Check contrast, labels, keyboard access, overflow, and long content.
4. Confirm the implementation uses shared tokens and components.
5. Remove decoration that does not clarify information or action.

Report what you inspected and what remains unverified. Do not claim visual QA if you did not view the rendered interface.

