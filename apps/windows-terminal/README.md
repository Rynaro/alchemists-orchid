# Windows Terminal Installation

Follow these steps to install **Alchemist's Orchid v2.0** themes in your Windows Terminal.

## Available Themes

- **Dark Mode** - Default, optimized for reduced halation
- **Light Mode** - For users who prefer light backgrounds
- **Sepia Mode** - Warm tones for extended sessions

---

## Quick Installation (All Themes)

1. **Open** your Windows Terminal settings:
   - Via the UI: Open the dropdown next to the tab bar and click **Settings**
   - Or press `Ctrl + ,`

2. **Locate** the `"schemes": []` array in `settings.json` (or create it if missing)

3. **Paste** all three themes from [`schemes.json`](schemes.json) into the array

4. **Set** your preferred theme in your profile:
   ```jsonc
   {
     "guid": "{your-profile-guid}",
     "name": "My Profile",
     "colorScheme": "Alchemist's Orchid v2.0 Dark"
   }
   ```

5. **Save** and enjoy! 🌸

---

## Individual Theme Installation

### 🌙 Dark Mode (Recommended Default)

Best for: Most users, evening coding, reduced eye strain in dark environments

```jsonc
{
  "name": "Alchemist's Orchid v2.0 Dark",
  "foreground": "#E5E9F0",
  "background": "#2E3440",
  "cursorColor": "#D9A8DD",
  "selectionBackground": "#4C566A",

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

### ☀️ Light Mode

Best for: Users with astigmatism who experience halation, bright environments, daytime coding

```jsonc
{
  "name": "Alchemist's Orchid v2.0 Light",
  "foreground": "#2E3440",
  "background": "#FAFBFC",
  "cursorColor": "#B266B2",
  "selectionBackground": "#D8DEE9",

  "black":        "#2E3440",
  "red":          "#C41585",
  "green":        "#4D7028",
  "yellow":       "#8A6000",
  "blue":         "#2D6299",
  "purple":       "#8839AA",
  "cyan":         "#1D7A78",
  "white":        "#E5E9F0",

  "brightBlack":  "#4C566A",
  "brightRed":    "#E31C97",
  "brightGreen":  "#5E8A32",
  "brightYellow": "#A57800",
  "brightBlue":   "#3A7AB8",
  "brightPurple": "#9F47C4",
  "brightCyan":   "#248E8B",
  "brightWhite":  "#FAFBFC"
}
```

### 📜 Sepia Mode

Best for: Extended coding sessions, evening use, reduced blue light exposure

```jsonc
{
  "name": "Alchemist's Orchid v2.0 Sepia",
  "foreground": "#3B3228",
  "background": "#F5F0E6",
  "cursorColor": "#A35BA3",
  "selectionBackground": "#E5DFD5",

  "black":        "#3B3228",
  "red":          "#B52080",
  "green":        "#4A6A28",
  "yellow":       "#806000",
  "blue":         "#2E5E8A",
  "purple":       "#7B3399",
  "cyan":         "#1A6B69",
  "white":        "#E5E0D6",

  "brightBlack":  "#5A5045",
  "brightRed":    "#D42995",
  "brightGreen":  "#5C8432",
  "brightYellow": "#997300",
  "brightBlue":   "#3972A8",
  "brightPurple": "#9440B3",
  "brightCyan":   "#238280",
  "brightWhite":  "#F5F0E6"
}
```

---

## Legacy Theme (v1.0)

If you prefer the original high-saturation pink, the legacy theme is preserved:

```jsonc
{
  "name": "Alchemist's Orchid v1.0 (Legacy)",
  "foreground": "#E5E9F0",
  "background": "#2E3440",
  "cursorColor": "#C89BD0",

  "black":        "#3B4252",
  "red":          "#FF92D0",
  "green":        "#A3BE8C",
  "yellow":       "#EBCB8B",
  "blue":         "#81A1C1",
  "purple":       "#C89BD0",
  "cyan":         "#8FBCBB",
  "white":        "#E5E9F0",

  "brightBlack":  "#4C566A",
  "brightRed":    "#FFB3DE",
  "brightGreen":  "#C3E4A8",
  "brightYellow": "#F5E27A",
  "brightBlue":   "#A3C2E8",
  "brightPurple": "#DAC0F2",
  "brightCyan":   "#9EECE8",
  "brightWhite":  "#ECEFF4"
}
```

⚠️ **Note:** The legacy theme uses 100% saturation pink which may cause halation for users with astigmatism.

---

## Switching Themes Dynamically

You can set up keyboard shortcuts to switch between modes:

1. Open Settings (`Ctrl + ,`)
2. Go to **Actions**
3. Add custom actions:

```jsonc
{
  "command": {
    "action": "setColorScheme",
    "colorScheme": "Alchemist's Orchid v2.0 Dark"
  },
  "keys": "ctrl+shift+1"
},
{
  "command": {
    "action": "setColorScheme",
    "colorScheme": "Alchemist's Orchid v2.0 Light"
  },
  "keys": "ctrl+shift+2"
},
{
  "command": {
    "action": "setColorScheme",
    "colorScheme": "Alchemist's Orchid v2.0 Sepia"
  },
  "keys": "ctrl+shift+3"
}
```

---

## Troubleshooting

### Text looks blurry or has a "glow" effect
You may be experiencing halation. Try:
1. Switching to Light or Sepia mode
2. Increasing font size
3. Using a font with heavier weight (e.g., Cascadia Code SemiBold)

### Colors look washed out
Ensure your terminal is using the correct color scheme and your display is calibrated properly.

### Theme not appearing
Make sure you've saved `settings.json` and restarted Windows Terminal.

---

## Need Help?

Open an issue on GitHub or check the [main documentation](../../README.md).
