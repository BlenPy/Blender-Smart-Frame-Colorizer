# Smart Frame Colorizer

Automatically or manually color your Frame nodes in the Shader Editor based on random tints, keyword-based rules, or node-based rules.

Persist palettes (in development) and rules across projects using JSON import/export.

> **Note:** The addon is functional but not yet complete — especially the palette system, which is still being improved for easier editing and persistence.

![Blender](https://img.shields.io/badge/blender-addon-orange)

---

## Features

### Auto Coloring

- **Random Mode**  
  New frames are tinted once with a random color.

- **Rules Mode**  
  Frames are tinted based on your custom rules. Renaming a frame or moving nodes in/out triggers recoloring.

- **Fallback Random Color**  
  If no rule matches, an optional fallback assigns a random color.

#### Keyword Rules

- Frame label contains a keyword → assigns a single color or palette.

#### Node Rules

- Frame contains a matching shader node → assigns a single color or palette.  
- Any Shader Editor node is supported, including custom/addon nodes.

---

### Manual Coloring (Sidebar)

In the **Shader Editor**, press `N` to open the sidebar and go to the **SFC** tab:

- `Color Selected Frame(s)` — apply current mode to selected frames  
- `Color All Frames` — apply current mode to all frames in the node tree
