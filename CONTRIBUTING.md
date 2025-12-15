# Contributing to Alchemist's Orchid

Thank you for your interest in contributing to Alchemist's Orchid! 🌸

## How to Contribute

### 🐛 Reporting Issues

- Check existing issues first to avoid duplicates
- Include your terminal/editor, OS, and display type (LCD/OLED/IPS)
- Screenshots are extremely helpful, especially for color-related issues
- If you have astigmatism, please mention it — your feedback is especially valuable

### 🎨 Adding New Platform Support

We'd love to expand to more platforms! Here's what we need:

**Wanted:**
- [ ] VS Code theme
- [ ] iTerm2 configuration
- [ ] Vim/Neovim colorscheme
- [ ] JetBrains IDE theme
- [ ] Alacritty configuration
- [ ] Kitty configuration
- [ ] tmux theme
- [ ] Warp terminal theme

**How to add a new platform:**

1. Create a new folder in `apps/` (e.g., `apps/vscode/`)
2. Include all three modes: Dark, Light, and Sepia
3. Add a README.md with installation instructions
4. Test on actual hardware if possible
5. Submit a PR with screenshots

### 🔬 Accessibility Testing

If you have:
- Astigmatism
- Color vision deficiency
- Photosensitivity
- Other visual conditions

Your feedback on the palette is incredibly valuable. Please:

1. Try all three modes (Dark, Light, Sepia)
2. Note which mode works best for you
3. Report any colors that cause discomfort
4. Include your display type (OLED screens show more halation)

### 📝 Documentation

- Fix typos and improve clarity
- Add examples and use cases
- Translate documentation (we'd love Portuguese, Chinese, Japanese, Spanish)

## Development Guidelines

### Color Changes

Before proposing color changes:

1. **Check WCAG compliance** - Use [contrastchecker.com](https://contrastchecker.com)
2. **Consider saturation** - Dark mode should use <60% saturation for accent colors
3. **Test on multiple displays** - LCD, IPS, and OLED render colors differently
4. **Document the rationale** - Why is this change better?

### Code Style

- Use consistent formatting in JSON files
- Comments in configuration files should be brief
- README files should follow the existing structure

### Commit Messages

```
feat: Add VS Code theme support
fix: Adjust pink saturation for better contrast
docs: Add iTerm2 installation instructions
```

## Pull Request Process

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/vscode-theme`)
3. Make your changes
4. Test thoroughly
5. Update documentation if needed
6. Submit a PR with:
   - Clear description of changes
   - Screenshots (for visual changes)
   - Testing notes

## Questions?

Open an issue with the `question` label or reach out to the maintainers.

---

Made with 💜 by the Alchemist's Orchid community
