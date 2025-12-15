# Changelog

All notable changes to Alchemist's Orchid will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.0] - 2025-12-15

### 🎉 Major Release: Accessibility-First Redesign

This release focuses on making Alchemist's Orchid accessible to users with astigmatism while preserving the original aesthetic vision.

### Added

- **☀️ Light Mode** - Essential for users who experience halation with dark interfaces
  - Background: `#FAFBFC` (off-white, not pure white)
  - Higher saturation syntax colors for visibility
  - Full WCAG AA compliance

- **📜 Sepia Mode** - Warm tones for extended coding sessions
  - Background: `#F5F0E6` (warm cream)
  - Reduced blue light emission
  - Comfortable for multi-hour use

- **📚 Research Documentation** - Full scientific backing for design decisions
  - Color psychology research
  - Astigmatism accessibility guidelines
  - WCAG compliance details

- **🎮 Dynamic Theme Switching** - Keyboard shortcuts for Windows Terminal

### Changed

- **🌸 Pink (Red)** - `#FF92D0` → `#E8A4CC`
  - Saturation reduced from 100% to 60%
  - Prevents halation blooming for astigmatism users
  - Maintains the orchid aesthetic

- **🌟 Yellow** - `#EBCB8B` → `#DFCA9A`
  - Saturation reduced from 70% to 52%
  - Improved comfort during extended use

- **✨ Cursor** - `#C89BD0` → `#D9A8DD`
  - Softer purple, less harsh on eyes
  - 40% saturation for comfort

### Preserved

All other colors remain unchanged as they were already well-optimized:

- ✅ Background `#2E3440` - NOT pure black (good for halation prevention)
- ✅ Foreground `#E5E9F0` - NOT pure white (reduces glare)
- ✅ Purple `#C89BD0` - 36% saturation (perfect for dark mode)
- ✅ Green `#A3BE8C` - 28% saturation (Nord standard)
- ✅ Blue `#81A1C1` - 34% saturation (well balanced)
- ✅ Cyan `#8FBCBB` - 25% saturation (very comfortable)

### Technical Details

| Metric | Dark Mode | Light Mode | Sepia Mode |
|--------|-----------|------------|------------|
| Main Text Contrast | 10.26:1 | 12.06:1 | 11.05:1 |
| WCAG Rating | AAA | AAA | AAA |
| All Syntax Colors | AA+ | AA+ | AA+ |

### Migration Guide

**From v1.0 to v2.0:**

1. Replace your existing scheme with `Alchemist's Orchid v2.0 Dark`
2. The legacy v1.0 scheme is preserved as `Alchemist's Orchid v1.0 (Legacy)`
3. Consider trying Light or Sepia mode if you experience eye strain

---

## [1.0.0] - 2025-XX-XX

### Added

- Initial release of Alchemist's Orchid
- Dark theme with Arctic/Nord-inspired base
- Purple and pink accent palette
- Windows Terminal configuration

### Color Palette (v1.0)

| Element    | Hex       |
| ---------- | --------- |
| Background | `#2E3440` |
| Foreground | `#E5E9F0` |
| Pink       | `#FF92D0` |
| Green      | `#A3BE8C` |
| Yellow     | `#EBCB8B` |
| Blue       | `#81A1C1` |
| Purple     | `#C89BD0` |
| Cyan       | `#8FBCBB` |

---

## Notes

### Versioning Philosophy

- **Major versions** (X.0.0): Significant palette changes or accessibility improvements
- **Minor versions** (0.X.0): New platform support or additional features
- **Patch versions** (0.0.X): Bug fixes and documentation updates

### Accessibility Commitment

Starting with v2.0, all releases will be tested for:
- WCAG AA compliance (minimum)
- Astigmatism-friendly design
- Multiple display type compatibility (LCD, OLED, IPS)
