# What QuickMotion makes


Everything goes into one new folder next to your mesh, `GASP_<Name>` (the name comes from your mesh, without its
`SK_` or `SKM_` prefix; change the pattern in Project Settings). Nothing else in your project is changed.

| File | What it is | Rebuild |
|---|---|---|
| `GASP_<Name>_Setup` | The settings card. | Keeps it, and updates **Result** |
| `BP_GASP_<Name>` | Your character: a child of GASP's `SandboxCharacter_Mover`. Place it, play as it, add to it. | **Never** changes it |
| `BPV_GASP_<Name>` | What your character looks like: your mesh (and its extra parts), shown in GASP's character in place of the mannequin. | Refreshes it |
| `ABP_GASP_<Name>` | Moves your mesh with GASP's mannequin, every frame. | Refreshes it |
| `IKR_<Name>` | Your character's IK Rig, with body parts named the standard way. Also use it to [retarget animation packs](../guide/retarget-an-animation-pack.md#retarget-an-animation-pack). | Refreshes it |
| `RTG_UEFN_To_<Name>` | The IK Retargeter from GASP's mannequin to your character, with the hands lined up (Fix Hands). | Refreshes it |
| `SK_<Name>_Fixed` and its skeleton | Only for meshes with the Blender units problem: a corrected copy your character shows instead. | Refreshes it |
| `ABP_GASP_<Name>_Parts` | Only when an extra part has bones of its own (like separately rigged hair): keeps those bones on the body. Full version. | Refreshes it |

**Characters from plugin or engine content** (for example QuickMotion's own sample character) are first copied into
your project's `Content/QuickMotion/` folder, with their materials and textures, and the character is made from the
copy. Your project then never depends on another plugin's files.

