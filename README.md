# Blender Smart Frame Colorizer

A powerful Blender addon that revolutionizes your node workflows by automatically coloring Frame nodes. Use a powerful, priority-based rule system to intelligently organize your Shader, Geometry, and Compositor node trees.

Stop wasting time manually coloring frames and let the addon do it for you. Define a set of rules, and let every frame automatically get the right color based on its content or label.

---

## ✨ Key Features

* **Works in 3 Editors:** Create and manage separate rule sets for the **Shader**, **Geometry**, and **Compositor** node editors.
* **Prioritized Rule System:** Rules are applied from top-to-bottom. The first rule that matches a frame wins. Simply drag rules up or down to change their priority.
* **Live Auto-Coloring:** Frames are colored automatically as you create them or update your node tree. No extra clicks needed.
* **Two Powerful Rule Types:**
    * **Keyword:** Colors a frame if its `Label` contains a specific word (e.g., "UVs", "Mask", "Control").
    * **Node Type:** Colors a frame if it contains a specific node (e.g., `Image Texture`, `Mix`, `Group Input`).
* **Advanced Color Palettes:** Go beyond single colors. Create palettes that assign colors using different modes:
    * **Uniform:** A random color from the palette.
    * **Weighted:** A random color, but with a defined probability for each.
    * **Gradient:** A random color sampled from a multi-stop gradient (with `Linear` or `Ease` interpolation).
    * **Sequential:** Cycles through the palette's colors in order.
* **Full Manual Control:** Use the N-Panel for quick operations like `Update All Frames`, `Reset Selected`, or use the `Quick Color` popup.
* **Full Shortcut Support:** All major operations are mapped to `Shift + Alt` shortcuts for maximum speed.
* **Import/Export Your Setup:** Save your entire rules and palettes configuration to a `.json` file to share, back up, or transfer to another computer.

---

## 🚀 Installation

1.  Download the latest `Smart_Frame_Colorizer.zip` file from the [Releases](https://github.com/BlenPy/Blender-Smart-Frame-Colorizer/releases) page.
2.  In Blender, go to `Edit` > `Preferences` > `Add-ons`.
3.  Click `Install...` and select the `.zip` file you downloaded.
4.  Enable the addon by checking the box next to "Smart Frame Colorizer".

---

## 📖 How to Use

The addon has two parts: the quick-access **Tool Panel** in the Node Editor and the main **Addon Preferences** where you build your logic.

### 1. Quick Controls (Node Editor N-Panel)

In the Node Editor, press `N` to open the sidebar and click the **"Tool"** tab. Here you will find the main operators:

* **Quick Color Popup:** (`Shift+Alt+Q`) Instantly apply any color to the selected frames.
* **Update Selected/All:** (`Shift+Alt+U` / `Shift+Alt+A`) Force the addon to re-apply your rules to the selected frames or all frames in the tree.
* **Reset Selected/All:** (`Shift+Alt+R` / `Shift+Alt+X`) Remove the custom color from frames.
* **Fallback to Random:** If no rules match a frame, this option will assign it a random color instead of leaving it gray.

### 2. The Main Setup (Addon Preferences)

This is the "brain" of the addon. Go to `Edit` > `Preferences` > `Add-ons` and find "Smart Frame Colorizer".

Set the **Color Mode** to **"By Rules"** to enable the system. The preferences are split into three tabs:

#### 🎨 **Palettes** Tab
This is where you create your color sets.

1.  Click `+` to add a new palette (e.g., "Texture Pal").
2.  Select its `Sampling Mode` (e.g., `Uniform`).
3.  Add colors to it using the `+` button in the right-hand list.

#### 룰 **Rules** Tab
This is where you define the logic.

1.  First, select which editor you want to create rules for: **Shader**, **Geometry**, or **Compositor**. Each editor has its own independent list of rules.
2.  Click the `+` button to add a new rule.
3.  **Set the Priority:** Use the **Up/Down arrows** to move the rule. **Rules are checked from top to bottom. The first one that matches wins.**
4.  **Configure the Rule:**
    * **Rule Type:** Choose `Keyword` or `Node Type`.
    * **Mode:** Choose `Single Color` (and pick a color) or `Use Palette` (and select a palette you made).

> **Example Rule:**
> * **Editor:** `Shader`
> * **Rule 1:** `Rule Type: Node Type` > `Node: Image Texture` > `Mode: Use Palette` > `Palette: Texture Pal`
> * **Rule 2:** `Rule Type: Keyword` > `Keyword: Math` > `Mode: Single Color` > `Color: (Blue)`
>
> Now, any frame containing an `Image Texture` node will get a color from your "Texture Pal," and any frame with "Math" in its label will turn blue.

#### ⚙️ **Settings** Tab
General settings for the addon.

* **Auto Color:** Automatically color frames when the node tree updates. Turn this off if you prefer to run updates manually.
* **Config Import/Export:** Save or load your complete setup (all rules and palettes) from a `.json` file.
* **Backward Compatibility:** This addon can successfully load `.json` files created by older versions. Old rules will be automatically placed in the **Shader** rule set.

---

## ⌨️ Shortcuts

All shortcuts are in the Node Editor and use the `Shift + Alt` modifier.

| Action | Shortcut |
| :--- | :--- |
| **Quick Color Popup** | `Shift + Alt + Q` |
| **Update Selected Frames** | `Shift + Alt + U` |
| **Update All Frames** | `Shift + Alt + A` |
| **Reset Selected Frames** | `Shift + Alt + R` |
| **Reset All Frames** | `Shift + Alt + X` |

---

## License

This project is licensed under the MIT License.
