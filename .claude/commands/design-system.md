# Design System Generator — Claude Code Command
#
# Usage: /design-system <brand-color> [font-family] [style]
# Example: /design-system #6366f1 "Outfit" rounded
#
# This command generates a complete, production-ready design system from a single brand color.

Read the skill instructions at: `skills/design-system-generator/SKILL.md`

Follow the 5-phase workflow defined there:
1. Brand Input Collection
2. Color System Generation (reference: `skills/design-system-generator/references/color-system.md`)
3. Token Architecture (references: typography-scale.md, spacing-system.md)
4. Component Styles (reference: component-patterns.md)
5. Preview & Delivery (reference: dark-mode-guide.md)

Output all generated files to the `design-system/` directory.

If the user provided arguments with this command, use them as the brand parameters:
- First argument: brand color (hex, rgb, oklch, or color name)
- Second argument (optional): font family
- Third argument (optional): border radius style (sharp, rounded, or pill)

If no arguments were provided, ask the user for at least a brand color.
