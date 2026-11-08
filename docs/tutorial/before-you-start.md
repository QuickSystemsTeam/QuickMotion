# 1. Before you start

You'll turn your own character into a Game Animation Sample (GASP) character and play it in GASP's level. You don't
change any settings and you don't need to know anything about IK Rigs or retargeting.

<!-- Screenshots: captured at M1 per Docs/ShotList.md (S01, S02, S03, S08). -->



You need:

- **Unreal Engine 5.8.**
- **The Game Animation Sample** in your project. It's free from Epic on Fab: search for "Game Animation Sample",
  add it to your library, and either create a new project from it or add it to an existing UE 5.8 project.
- **QuickMotion** (or QuickMotion Lite) enabled: **Edit > Plugins**, search "QuickMotion", tick it, restart the editor.
- **A character mesh** (a Skeletal Mesh) in your project. No character yet? Use one of these to try it:
  - **QuickMotion's sample character** (full version): in the Content Browser, open **Settings** and tick **Show
    Plugin Content**, then go to `Plugins/QuickMotion Content/Demo/QMDemo_Explorer/SkeletalMeshes` and use
    **SK_QMDemo_Explorer**. QuickMotion copies it into your project's `Content/QuickMotion` folder first, so your
    project never depends on the plugin's own files.
  - **GASP's Quinn** (works in QuickMotion Lite too): `SKM_Quinn_Simple` in `Content/Characters/UE5_Mannequins/Meshes`.
    QuickMotion Lite works with meshes on the UE5 Mannequin skeleton, such as Manny, Quinn, or characters made for them.

QuickMotion never changes your mesh, its skeleton or your Blueprints. It only adds new files in a new folder.

