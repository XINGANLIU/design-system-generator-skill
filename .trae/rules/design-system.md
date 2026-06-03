# Design System Generator

Generate a complete, production-ready design system from a single brand color.

## Instructions

When the user asks to create a design system, generate a color palette, build a theme,
create UI tokens, or set up brand styles, follow the workflow in:
`skills/design-system-generator/SKILL.md`

## Workflow Summary

1. **Brand Input** — Collect brand color, font, style preferences
2. **Color System** — Generate OKLCH palettes (see `skills/design-system-generator/references/color-system.md`)
3. **Tokens** — W3C Design Tokens + CSS variables (see `references/typography-scale.md`, `references/spacing-system.md`)
4. **Components** — Production CSS (see `references/component-patterns.md`)
5. **Preview** — HTML preview page (see `references/dark-mode-guide.md`)

## Constraints

- OKLCH color space for all colors
- Only CSS custom properties in components (no hardcoded values)
- WCAG 2.2 AA compliance
- Light + Dark theme support
- Output to `design-system/` directory
