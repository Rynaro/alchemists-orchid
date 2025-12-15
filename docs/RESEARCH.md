# Alchemist's Orchid v2.0
## Astigmatism-Optimized Color Palette Research Report

**Prepared by:** UI/UX Color Research Team  
**Date:** December 2025  
**Version:** 2.0

---

## Executive Summary

This document presents a comprehensive analysis and revision of the **Alchemist's Orchid** colorscheme, specifically optimized for users with astigmatism while preserving the original anxiety-reducing, purple/pink aesthetic goals.

### Key Findings

1. **Your core design instincts were correct** — Purple and pink ARE research-backed for anxiety reduction
2. **The Nord-inspired base was an excellent choice** — `#2E3440` background prevents worst halation effects
3. **Critical issue identified:** Pink (`#FF92D0`) has 100% saturation, causing halation blooming for astigmatism users
4. **Missing feature:** A light mode is essential — ~50% of astigmatism sufferers prefer light mode

---

## Part 1: The Science Behind the Revisions

### 1.1 Astigmatism and Dark Mode: The Halation Problem

When someone with astigmatism views dark interfaces, their pupils dilate to allow more light in. Due to the irregular curvature of the cornea (shaped more like a rugby ball than a sphere), this dilation causes light to focus at multiple points instead of one, creating a "halation" or "blooming" effect where light text appears to bleed into dark backgrounds.

**Key Research Findings:**

- ~47-50% of the population has some degree of astigmatism
- Halation is most severe with **pure white text on pure black backgrounds**
- High-saturation colors exacerbate the effect
- The effect worsens on OLED displays due to higher contrast ratios

**Citation:** Jason Harrison, Sensory Perception and Interaction Research Group, University of British Columbia (2002)

### 1.2 Color Psychology: Your Instincts Were Right

Research strongly supports your choice of purple and pink for an anxiety-reducing palette:

| Color | Effect | Research Source |
|-------|--------|-----------------|
| **Pink** | Tranquilizing effect within minutes; suppresses aggression and anxiety | Lubos (2012) |
| **Purple/Lavender** | Decreases amygdala activity (fear/anxiety center); highest "emotional trustworthiness" rating | Click2Pro Design Psychology Survey |
| **Blue** | Associated with relief (35% of people); calming and stabilizing | WebMD Cross-Cultural Survey |
| **Green** | Easiest color for human eye to perceive; improves working memory | Takemura et al. (2021) |

**Key insight:** Purple is a fusion of calming blue and nurturing pink — neuropsychology research shows it has a "quieting effect on stress circuits of the brain."

### 1.3 Saturation and Dark Mode: The Critical Relationship

For dark mode interfaces, the relationship between saturation and accessibility is **inverse** to light mode:

| Mode | Saturation Requirement | Reason |
|------|------------------------|--------|
| **Dark Mode** | LOWER saturation | High saturation causes color vibration and halation blooming |
| **Light Mode** | HIGHER saturation | More saturation needed for visibility against bright backgrounds |

---

## Part 2: Original Palette Analysis

### 2.1 What Was Already Good ✅

| Element | Hex | Status | Reason |
|---------|-----|--------|--------|
| Background | `#2E3440` | ✅ Excellent | NOT pure black — prevents worst halation |
| Foreground | `#E5E9F0` | ✅ Excellent | NOT pure white — reduces glare |
| Purple | `#C89BD0` | ✅ Perfect | 36% saturation — ideal for dark mode |
| Green | `#A3BE8C` | ✅ Perfect | 28% saturation — Nord standard |
| Blue | `#81A1C1` | ✅ Perfect | 34% saturation — well balanced |
| Cyan | `#8FBCBB` | ✅ Perfect | 25% saturation — very comfortable |

### 2.2 Issues Identified ⚠️

| Element | Hex | Issue | Impact |
|---------|-----|-------|--------|
| **Pink (Red)** | `#FF92D0` | **100% saturation** | Severe halation blooming for astigmatism users |
| Yellow | `#EBCB8B` | 70% saturation | Moderate halation risk |
| **No Light Mode** | — | Missing feature | Excludes ~50% of astigmatism users who prefer light mode |

---

## Part 3: Proposed Revisions

### 3.1 Dark Mode v2.0

```
Background:   #2E3440  (unchanged - Deep Arctic Night)
Foreground:   #E5E9F0  (unchanged - Soft Snowfall)
Cursor:       #D9A8DD  (softer purple)
```

#### Syntax Colors — Dark Mode

| Role | Original | Revised | Saturation Change | Contrast |
|------|----------|---------|-------------------|----------|
| Pink (strings) | `#FF92D0` | `#E8A4CC` | 100% → 60% | 6.31:1 AA |
| Purple (keywords) | `#C89BD0` | `#C89BD0` | unchanged | 5.39:1 AA |
| Green (comments) | `#A3BE8C` | `#A3BE8C` | unchanged | 6.13:1 AA |
| Blue (functions) | `#81A1C1` | `#81A1C1` | unchanged | 4.64:1 AA |
| Yellow (types) | `#EBCB8B` | `#DFCA9A` | 70% → 52% | 7.76:1 AAA |
| Cyan (constants) | `#8FBCBB` | `#8FBCBB` | unchanged | 5.99:1 AA |

#### ANSI Colors — Dark Mode

```json
{
  "black":        "#3B4252",
  "red":          "#E8A4CC",
  "green":        "#A3BE8C",
  "yellow":       "#DFCA9A",
  "blue":         "#81A1C1",
  "purple":       "#C89BD0",
  "cyan":         "#8FBCBB",
  "white":        "#D8DEE9",
  
  "brightBlack":  "#4C566A",
  "brightRed":    "#F0C0DD",
  "brightGreen":  "#C3E4A8",
  "brightYellow": "#EBD9AF",
  "brightBlue":   "#A3C2E8",
  "brightPurple": "#DAC0F2",
  "brightCyan":   "#9EECE8",
  "brightWhite":  "#ECEFF4"
}
```

### 3.2 Light Mode (NEW — Essential for Astigmatism)

```
Background:   #FAFBFC  (off-white, NOT pure white)
Foreground:   #2E3440  (same dark gray)
Cursor:       #B266B2  (visible purple)
```

#### Syntax Colors — Light Mode

| Role | Hex | Contrast | Rating |
|------|-----|----------|--------|
| Pink (strings) | `#C41585` | 5.34:1 | AA |
| Purple (keywords) | `#8839AA` | 6.31:1 | AA |
| Green (comments) | `#4D7028` | 5.53:1 | AA |
| Blue (functions) | `#2D6299` | 6.11:1 | AA |
| Yellow (types) | `#8A6000` | 5.40:1 | AA |
| Cyan (constants) | `#1D7A78` | 4.93:1 | AA |

### 3.3 Sepia Mode (NEW — Extended Sessions)

```
Background:   #F5F0E6  (warm cream)
Foreground:   #3B3228  (warm brown)
Cursor:       #A35BA3  (muted purple)
```

#### Syntax Colors — Sepia Mode

| Role | Hex | Contrast | Rating |
|------|-----|----------|--------|
| Pink (strings) | `#B52080` | 5.31:1 | AA |
| Purple (keywords) | `#7B3399` | 6.66:1 | AA |
| Green (comments) | `#4A6A28` | 5.46:1 | AA |
| Blue (functions) | `#2E5E8A` | 5.99:1 | AA |
| Yellow (types) | `#806000` | 5.15:1 | AA |
| Cyan (constants) | `#1A6B69` | 5.52:1 | AA |

---

## Part 4: Implementation

### 4.1 Windows Terminal — Dark Mode

```json
{
  "name": "Alchemist's Orchid v2.0",
  "foreground": "#E5E9F0",
  "background": "#2E3440",
  "cursorColor": "#D9A8DD",
  
  "black":        "#3B4252",
  "red":          "#E8A4CC",
  "green":        "#A3BE8C",
  "yellow":       "#DFCA9A",
  "blue":         "#81A1C1",
  "purple":       "#C89BD0",
  "cyan":         "#8FBCBB",
  "white":        "#D8DEE9",
  
  "brightBlack":  "#4C566A",
  "brightRed":    "#F0C0DD",
  "brightGreen":  "#C3E4A8",
  "brightYellow": "#EBD9AF",
  "brightBlue":   "#A3C2E8",
  "brightPurple": "#DAC0F2",
  "brightCyan":   "#9EECE8",
  "brightWhite":  "#ECEFF4"
}
```

### 4.2 Windows Terminal — Light Mode

```json
{
  "name": "Alchemist's Orchid v2.0 Light",
  "foreground": "#2E3440",
  "background": "#FAFBFC",
  "cursorColor": "#B266B2",
  
  "black":        "#2E3440",
  "red":          "#C41585",
  "green":        "#4D7028",
  "yellow":       "#8A6000",
  "blue":         "#2D6299",
  "purple":       "#8839AA",
  "cyan":         "#1D7A78",
  "white":        "#D8DEE9",
  
  "brightBlack":  "#4C566A",
  "brightRed":    "#E31C97",
  "brightGreen":  "#5E8A32",
  "brightYellow": "#A57800",
  "brightBlue":   "#3A7AB8",
  "brightPurple": "#9F47C4",
  "brightCyan":   "#248E8B",
  "brightWhite":  "#ECEFF4"
}
```

### 4.3 VS Code (settings.json snippet)

```json
"workbench.colorCustomizations": {
  "[Alchemist's Orchid v2.0]": {
    "editor.background": "#2E3440",
    "editor.foreground": "#E5E9F0",
    "editorCursor.foreground": "#D9A8DD",
    "editor.selectionBackground": "#4C566A80"
  }
}
```

---

## Part 5: Design Rationale

### 5.1 Why Reduce Pink Saturation?

The original pink `#FF92D0` at 100% saturation creates several problems for astigmatism users:

1. **Halation blooming**: Highly saturated colors on dark backgrounds appear to "glow" and bleed beyond their boundaries
2. **Color vibration**: When colors share extreme saturation values, they create uncomfortable visual vibration at edges
3. **Chromostereopsis**: Different wavelengths focus at different depths in the eye — saturated pink appears to "float" above the background

The revised pink `#E8A4CC` at 60% saturation:
- Maintains the pink identity and anxiety-reducing properties
- Reduces halation effect significantly
- Passes WCAG AA with 6.31:1 contrast ratio
- Feels "softer" and more comfortable for extended use

### 5.2 Why Light Mode is Essential

For astigmatism users, the choice between light and dark mode isn't preference — it's accessibility:

| Factor | Dark Mode | Light Mode |
|--------|-----------|------------|
| Pupil state | Dilated | Constricted |
| Lens deformation impact | HIGH | LOW |
| Halation effect | Severe | Minimal |
| Text clarity | Reduced | Improved |

**Recommendation:** Always provide users the choice. Never force dark mode as the only option.

### 5.3 Why Sepia Mode?

Sepia mode provides:
- Reduced blue light emission for evening coding
- Warm tones that reduce eye strain during extended sessions
- A comfortable middle ground between dark and light modes
- Research-backed benefits for reading comprehension

---

## Part 6: Testing Recommendations

### 6.1 User Testing Checklist

- [ ] Test with users who have diagnosed astigmatism
- [ ] Test on OLED displays (higher contrast exacerbates halation)
- [ ] Test on LCD/IPS displays
- [ ] Test in different ambient lighting conditions
- [ ] Test during extended coding sessions (2+ hours)
- [ ] A/B test original vs. revised pink saturation

### 6.2 Contrast Verification

All colors should be verified against WCAG guidelines:
- **AA minimum**: 4.5:1 for normal text
- **AAA target**: 7:1 for normal text
- **Large text**: 3:1 minimum

Use: https://contrastchecker.com or https://webaim.org/resources/contrastchecker/

---

## References

1. Harrison, J. (2002). "WWW Colors and Readability." Sensory Perception and Interaction Research Group, University of British Columbia.

2. Lubos, L.C. (2012). "The Role of Colors in Stress Reduction." ResearchGate.

3. H. Locke. (2023). "Why dark mode causes more accessibility issues than it solves." Medium.

4. Level Access. (2024). "Accessibility for People with Astigmatism."

5. WGSN. (2020). "Colours to Soothe Anxiety & Promote Wellness."

6. Takemura, K. et al. (2021). "Effects of Green Color Exposure on Stress, Anxiety, and Pain." International Journal of Environmental Research and Public Health.

7. PMC. (2024). "Color difference threshold of chromostereopsis induced by flat display emission."

8. NCBI Bookshelf. (2023). "Chromatic Aberration." StatPearls.

---

## Appendix A: Color Psychology Quick Reference

| Color | Psychological Effect | Best Use |
|-------|---------------------|----------|
| Pink | Tranquilizing, calming | Strings, highlights |
| Purple | Reduces anxiety, emotional trust | Keywords, UI elements |
| Blue | Relief, security | Functions, links |
| Green | Nature, balance, easy to perceive | Comments, success states |
| Yellow/Gold | Joy, warmth | Warnings, types |
| Cyan | Cool, refreshing | Constants, info |

---

## Appendix B: Saturation Guidelines

| Context | Recommended Saturation |
|---------|------------------------|
| Dark background (coding) | 25-50% |
| Dark background (accent) | 50-65% |
| Light background (text) | 45-60% |
| Light background (accent) | 60-85% |
| Sepia background | 40-55% |

---

**Document prepared with 💜 for the Alchemist's Orchid community**

*"A colorscheme should make your eyes rest, not work."*
