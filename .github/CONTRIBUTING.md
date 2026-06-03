# Contributing to Design System Generator

Thank you for your interest in contributing! 🎨

## How to Contribute

### Report Issues

- Use GitHub Issues to report bugs or suggest features
- Include your AI agent name and version
- Provide the brand color you used and the expected vs actual output

### Add Example Themes

1. Fork the repository
2. Create a new directory in `examples/` (e.g., `examples/forest-green/`)
3. Include all 4 files: `tokens.json`, `tokens.css`, `components.css`, `preview.html`
4. Submit a Pull Request

### Improve Components

1. Edit `skills/design-system-generator/references/component-patterns.md`
2. Update the template in `skills/design-system-generator/templates/components.css.tmpl`
3. Ensure all components use only CSS custom properties (no hardcoded values)
4. Test in both Light and Dark themes
5. Submit a Pull Request

### Improve Color Algorithm

1. Edit `skills/design-system-generator/references/color-system.md`
2. Validate all generated palettes meet WCAG 2.2 AA contrast ratios
3. Provide before/after comparisons
4. Submit a Pull Request

## Code Style

- CSS: Use BEM-ish naming (`.component`, `.component--variant`, `.component__element`)
- Tokens: Follow W3C Design Tokens spec (`$value`/`$type`)
- Colors: OKLCH color space only
- Documentation: Bilingual (English + Chinese) preferred

## License

By contributing, you agree that your contributions will be licensed under the Apache 2.0 License.
