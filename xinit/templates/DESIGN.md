# UI design standard

Applies to {{UI project}}.

## Principles
- {{Product type}}: {{density, speed, keyboard use}}. Clarity over decoration.
- Reuse shared components before building new ones.
- Use theme tokens only. No hard-coded colors or one-off styles.

## Foundation
- Stack: {{UI library}}. Brand color/font: {{tokens}}. Icons: {{set}}.
- Themes: {{light/dark}}. Responsive: {{breakpoints}}.
- Language: {{UI text language}}. Number/date formats: {{formats}}.

## Page patterns
| Pattern | Building blocks |
|---|---|
| {{List page}} | {{components}} |
| {{Form}} | {{components}} |

Reference implementation: `{{path}}`.

## Interaction
- Destructive actions confirm.
- Every data view handles loading, empty and error states.
- Visible labels, keyboard support, visible focus.
