# Script it


Everything the right-click menu does is available to Editor Utility Blueprints and Python (editor only), under the
**QuickMotion** category:

| Function | What it does |
|---|---|
| **Make GASP Character** (Mesh) → Setup, Error | Same as right-click → Make GASP Character, without the confirmation window. Returns the new settings card, or none plus a plain-language Error. |
| **Rebuild GASP Character** (Setup) → OK, Error | Same as the settings card's Rebuild button. Keeps your character Blueprint and everything you added. |
| **Detect Rig** (Mesh) → Report | What QuickMotion finds on a skeleton without creating anything: rig type, how it was matched, the pelvis, each body part's bones and the parts to check. Full version only. |

And two events on the **QuickMotion Subsystem** (Editor Subsystem), for pipelines that react to new characters:

| Event | When |
|---|---|
| **On GASP Character Created** (Setup) | After Make GASP Character made a new character |
| **On GASP Character Rebuilt** (Setup) | After Rebuild refreshed a character |

**Example: make GASP characters for a whole folder** (Tools > Execute Python Script):

```python
# QuickMotion: make GASP characters for every Skeletal Mesh in a folder (Tools > Execute Python Script).
import unreal

FOLDER = "/Game/Characters/MyHeroes"  # change to your folder

for path in unreal.EditorAssetLibrary.list_assets(FOLDER, recursive=False):
    mesh = unreal.load_asset(path)
    if isinstance(mesh, unreal.SkeletalMesh):
        setup, error = unreal.QuickMotionLibrary.make_gasp_character(mesh)
        print(f"{mesh.get_name()}: {setup.get_editor_property('result') if setup else error}")
```

Each character gets its own `GASP_<Name>` folder next to its mesh, exactly as with the right-click menu.

