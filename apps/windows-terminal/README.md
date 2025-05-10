# Windows Terminal Installation

Follow these steps to install **Alchemist’s Orchid** in your Windows Terminal:

1. **Open** your Windows Terminal settings:

   * Via the UI: Open the dropdown next to the tab bar and click **Settings**.

2. **Locate** the `"schemes": []` array in `settings.json` (or create it if missing):

   ```jsonc
   "schemes": [
     // your other schemes
   ]
   ```

3. **Paste** this JSON snippet into the `"schemes"` array:

   ```jsonc
   {
     "name": "Alchemist's Orchid",
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

4. **Set** your profile’s color scheme by adding or updating the `"colorScheme"` property to `"Alchemist's Orchid"`:

   ```jsonc
   {
     "guid": "{your-profile-guid}",
     "name": "My Profile",
     "colorScheme": "Alchemist's Orchid"
   }
   ```

5. **Save** the file and **restart** Windows Terminal. Your new **Alchemist’s Orchid** palette will now be active!

