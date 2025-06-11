Smart Frame Colorizer

Automatically or manually color your Frame nodes in the Shader Editor based on random tints, keyword-based rules, or node-based rules. Persist palettes (a feature I work on currently) and rules across projects with import/export to JSON.

⸻

Features
	•	Auto Color on Frame Creation
	•	Random mode: each new Frame gets a one-time random color.
	•	By Rules mode: apply colors based on:
	•	Keyword rules: Frame label contains a substring → single color or palette.
	•	Node rules: Frame contains a child node type → single color or palette.
	•	Fallback Random Color: if no rule matches, optionally assign a random color.
	•	Manual Color (Sidebar Panel)
	•	Color Selected Frame(s) and Color All Frames buttons.
	•	Works in both Random and Rules modes.
	•	Add/remove node and keyword rules in Preferences.
	•	Import/export palettes and rules via JSON file.
	•	Immediate Recolor on Edits
	•	Renaming a Frame label or moving nodes in/out instantly triggers rule-based recolor.

⸻

Usage

Preferences Panel

Open Edit → Preferences → Add-ons → Smart Frame Colorizer. Configure:
	1.	Auto Color on Frame Creation: toggle on/off.
	2.	Color Mode:
	•	Random: frames get a one-time random color.
	•	By Rules: frames colored by your defined rules.
	3.	Fallback Random Color (Rules mode only): if no rule matches, assign a random tint.
	4.	Config File Path: import/export your palettes & rules.
	5.	Node-Based Rules: add rules by selecting a node type from the dropdown.
	6.	Keyword-Based Rules: add rules by defining a text keyword.
	7.	Palette Editor: create named palettes and add/remove RGB swatches.

Auto Coloring
	•	In Random mode, new frames are tinted once automatically.
	•	In Rules mode, frames are tinted according to your rules. Rename or move nodes to trigger recolor.

Manual Coloring Sidebar

In the Shader Editor, press N to open the sidebar and select the SFC tab. Use:
	•	Color Selected Frame(s): apply current mode coloring to selected frames.
	•	Color All Frames: apply current mode coloring to all frames in the node tree.

⸻

JSON Configuration Schema

{
  "palettes": [
    { "name": "Sunset", "colors": [[0.9,0.3,0.1], [0.9,0.6,0.2]] }
  ],
  "node_rules": [
    { "node_type": "ShaderNodeBsdfDiffuse", "mode": "SINGLE", "color": [0.8,0.2,0.1] },
    { "node_type": "ShaderNodeEmission", "mode": "PALETTE", "palette_name": "Sunset" }
  ],
  "keyword_rules": [
    { "label": "AO", "mode": "SINGLE", "color": [0.3,0.3,0.3] }
  ]
}

⸻

Contributing
	•	Fork the repo and submit pull requests for bug fixes or enhancements.
	•	Please keep code style consistent and update this README when adding features.
