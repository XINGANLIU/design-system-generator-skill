# Design System Generator — Agent Instructions
#
# This file enables the Design System Generator skill for OpenAI Codex and similar agents.
# https://github.com/XINGANLIU/design-system-generator-skill

## Skill: Design System Generator

When the user asks to create a design system, generate a color palette, build a theme,
create UI tokens, or set up brand styles, follow the workflow defined in:

**Main instructions**: `skills/design-system-generator/SKILL.md`

### Quick Reference

This skill generates a complete, production-ready design system from a single brand color:

1. **Brand Input** → Collect brand color (hex/rgb/oklch), font family, border radius style
2. **Color System** → OKLCH palettes: primary (10 steps), neutral (10 steps), semantic (success/warning/error/info)
3. **Tokens** → W3C Design Tokens JSON + CSS custom properties with Light/Dark theme support
4. **Components** → Button, Card, Input, Badge, Alert, Avatar, Skeleton, Tooltip, Modal, Navbar, Divider
5. **Preview** → Self-contained HTML preview page with theme toggle

### Reference Documents

Read these as needed during generation:

| File | Content |
|------|---------|
| `skills/design-system-generator/references/color-system.md` | OKLCH color palette algorithm |
| `skills/design-system-generator/references/typography-scale.md` | Font size/weight/line-height scales |
| `skills/design-system-generator/references/spacing-system.md` | Spacing, radius, shadow, z-index, transitions |
| `skills/design-system-generator/references/component-patterns.md` | CSS patterns for each component |
| `skills/design-system-generator/references/dark-mode-guide.md` | light-dark(), theme toggle, semantic token mapping |

### Output Structure

```
design-system/
├── tokens.json       # W3C Design Tokens
├── tokens.css        # CSS Custom Properties
├── components.css    # Component styles
└── preview.html      # Visual preview page
```

### Key Constraints

- All colors MUST use OKLCH color space
- Components MUST only use `var(--token-name)` — no hardcoded values
- WCAG 2.2 AA contrast compliance required
- Support Light and Dark themes via `light-dark()` + `[data-theme]`
- Follow phases in order, confirm with user between phases
