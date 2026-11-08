# Settings


Every setting QuickMotion shows, with the same help text you see when you hover it in the editor.

### The settings card

One card per character, named `GASP_<Name>_Setup`, in the character's folder. Double-click it to open it. Change a setting, then click **Rebuild**. Settings under **More** start folded away.

**Character**

| Setting | What it does | Notes |
|---|---|---|
| **Character Mesh** | Your character's Skeletal Mesh. QuickMotion reads it and never changes it. To use a different mesh, pick it here and click Rebuild: your character Blueprint stays the same. | you can change it |
| **Fix Hands** | Line up wrists and fingers with GASP's own mannequin so hands look right while walking, running and vaulting. Leave on unless you're fixing hands yourself. | you can change it, full version |
| **Result** | What the last Create or Rebuild found and did. Click Rebuild to refresh it. | shown, not editable |

**More**

| Setting | What it does | Notes |
|---|---|---|
| **Detected Rig** | The kind of skeleton QuickMotion detected on your mesh. | shown, not editable |
| **Extra Parts** | Your character's other meshes, like face, hair and clothes. QuickMotion finds them (the MetaHuman's own set, or meshes next to your body mesh that share its bones and cover only part of it). Add or remove entries, then click Rebuild. | you can change it, full version |
| **Pelvis Bone** | The bone that moves your whole character, usually called hips or pelvis. QuickMotion finds it; change it only if it picked the wrong bone, then click Rebuild. | you can change it |
| **Matched By** | How QuickMotion recognised your character's skeleton. | shown, not editable |
| **Bone Matching** | How each body part maps onto your character's bones. Items marked 'needs check' were best guesses: fix them if needed, then click Rebuild. | you can change it |
| **Output Folder Name** | The folder that holds everything QuickMotion made for this character. To put it somewhere else, move the whole folder in the Content Browser: Rebuild keeps working. | shown, not editable |
| **Fixed Copy** | Only set when your mesh's bones carry a scale (the common Blender metre-units export problem), which makes characters float. QuickMotion then uses this corrected copy instead. Your own mesh is never changed; Rebuild refreshes the copy. | shown, not editable |
| **Character Blueprint** | The character Blueprint QuickMotion made. It's yours to edit: Rebuild never overwrites it. | shown, not editable |

### Bone Matching entries

Each entry under **More > Bone Matching** is one body part.

| Setting | What it does | Notes |
|---|---|---|
| **Chain** | The body part, named like on GASP's own mannequin (for example LeftArm or LeftIndex). | you can change it |
| **Start Bone** | The first bone of this body part on your character (for example upperarm_l). | you can change it |
| **End Bone** | The last bone of this body part on your character (for example hand_l). | you can change it |
| **Needs Check** | QuickMotion wasn't sure about this match. Check that the bones are right, then click Rebuild. | shown, not editable |

### Project Settings

**Edit > Project Settings > Plugins > QuickMotion**. Most projects never change these.

**Game Animation Sample**

| Setting | What it does | Notes |
|---|---|---|
| **GASP Character Class Override** | Leave empty: QuickMotion finds the Game Animation Sample's character by itself. Set this only if you moved or renamed GASP's character Blueprint. | you can change it |
| **Mannequin Mesh Override** | Leave empty: QuickMotion finds GASP's mannequin (SKM_UEFN_Mannequin) by itself. Set this only if you moved or renamed it. | you can change it |

**Output**

| Setting | What it does | Notes |
|---|---|---|
| **Output Folder Pattern** | Name of the folder QuickMotion makes next to each character. {Name} becomes the mesh name without its SK_ or SKM_ prefix. | you can change it |

