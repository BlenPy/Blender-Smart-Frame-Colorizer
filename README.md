# Blender Smart Frame Colorizer

A powerful Blender addon to automatically, intelligently, and stylishly color Frame nodes in the Shader Editor. Say goodbye to gray, disorganized node trees and work more efficiently with a visually appealing system.

---

## ✨ Key Features

* **🎨 Auto-Coloring:** Every newly created Frame node is instantly colored.
* **룰 Rule-Based System:** Define custom rules to color frames based on their **label (keywords)** or the **nodes they contain**.
* **🎨 Advanced Color Palettes:** Create color palettes and pick colors from them using various modes:
    * **Uniform:** Selects a random color from the palette.
    * **Weighted:** Selects colors based on a probability you define.
    * **Sequential:** Cycles through the colors of the palette in order.
    * **Gradient:** Generates colors from a gradient that you can define with multiple color stops (including linear and ease interpolation).
* **⚡️ Quick Manual Control:**
    * A **Quick-Color Popup** to swiftly assign a color to selected frames.
    * Operators to apply rules to all or only selected frames.
    * Easily reset colors back to their default.
* **⌨️ Full Shortcut Support:** All important functions are accessible via shortcuts in the Node Editor.
* **💾 Config Import/Export:** Save and load your entire set of rules and palettes as a `.json` file. Perfect for sharing your configuration across projects or for backups.
* **🛠️ Developer Tools:** An experimental "Palette Tester" that generates an image to visualize the color distribution of your palettes.

---

## 🚀 Installation

1.  Download the latest version of the addon from the [Releases page](https://github.com/BlenPy/Blender-Smart-Frame-Colorizer/releases) (download the `.zip` file).
2.  Open Blender and go to `Edit -> Preferences -> Add-ons`.
3.  Click `Install...` and select the downloaded `.zip` file.
4.  Enable the addon by checking the box next to "Smart Frame Colorizer".

---

## 📖 Usage

You can find the main panel of the addon in the **Shader Editor**. Press `N` to open the sidebar, and click on the **"Tool"** tab.

### Basics

* **Auto Color:** Toggles the automatic coloring of new frames on or off.
* **Color Mode:** Choose between two main modes:
    * **Random:** Colors new frames with a completely random color (default).
    * **By Rules:** Uses the rule and palette system described below.

### Creating Rules and Palettes (in the Addon Preferences)

To create rules, open the addon preferences (`Edit -> Preferences -> Add-ons` and search for "Smart Frame Colorizer").

1.  **Set the `Color Mode` to `By Rules`.**
2.  **Create Palettes:**
    * Go to the "Palettes" section and create a new palette.
    * Give it a name and choose a `Sampling Mode` (e.g., `Gradient`).
    * Add colors ("Swatches"). Depending on the mode, you can also set the `Weight` or the `Position` on the gradient here.
3.  **Create Rules:**
    * **Keyword-Based Rules:** Triggered if the frame's label contains the keyword (e.g., a rule with the keyword "UVs" will color all frames that have "UVs" in their label).
    * **Node-Based Rules:** Triggered if a node of a specific type (e.g., an `Image Texture` node) is inside the frame.
4.  **Link Rules to Palettes:**
    * In each rule, you can set the `Mode` to `Use Palette` and enter the name of one of your created palettes.

### Manual Control (in the N-Panel)

* **Quick Color Popup:** Select one or more frames and click this to choose a color from a picker and apply it directly.
* **Update Selected/All:** Manually apply your defined rules to the selected frames or to all frames in the current node tree.
* **Reset Selected/All:** Removes the custom color from the selected or all frames.

### Shortcuts (in the Node Editor)

All shortcuts use the `Shift + Alt` combination.

| Action                 | Shortcut            |
| :--------------------- | :------------------ |
| Quick Color Popup      | `Shift + Alt + Q`   |
| Update Selected Frames | `Shift + Alt + U`   |
| Update All Frames      | `Shift + Alt + A`   |
| Reset Selected Frames  | `Shift + Alt + R`   |
| Reset All Frames       | `Shift + Alt + X`   |
| Toggle Developer Mode  | `Ctrl + Alt + D`    |

### Saving & Loading Configuration

In the addon preferences, you can specify a file path for a `.json` file.
* **Save:** Saves all your current rules and palettes to this file.
* **Load:** Clears your current settings and loads the configuration from the file.

---

## 🛠️ Developer Tools

Activate "Developer Mode" in the addon preferences or by using `Ctrl + Alt + D`.
This will make the **"Test Palette Distribution"** button visible in the palette settings. Clicking it will generate a new image in the **Image Editor**, showing a visual preview of your palette's color distribution based on the selected sampling mode.

---
