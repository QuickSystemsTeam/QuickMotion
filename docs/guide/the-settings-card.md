# The settings card


Every character QuickMotion makes has one settings card, `GASP_<Name>_Setup`, in its `GASP_<Name>` folder. It's
the one place to change how the character is made. Double-click it to open it. (Right-clicking a mesh that already
has a character and choosing **Make GASP Character** opens its card too.)

| On the card | What it does |
|---|---|
| **Rebuild** | Refreshes the helper files from the card. See [What Rebuild changes](what-rebuild-changes.md#what-rebuild-changes). |
| **Open Character** | Opens your `BP_GASP_<Name>` Blueprint. |
| **Character Mesh** | The mesh your character shows. Pick another one and click Rebuild to swap it. |
| **Result** | A short status of the last Create or Rebuild (for example *Ready to play · hands matched · 2 extra parts*), or what went wrong and how to fix it. Hover it for the details. |
| **More** (closed at first) | The skeleton QuickMotion found, how body parts map to bones, the folder, and your character Blueprint. |

To keep everything somewhere else, move the whole `GASP_<Name>` folder in the Content Browser. Rebuild keeps working
in the new place.

