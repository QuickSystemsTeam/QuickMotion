# Supported characters


QuickMotion reads your character's skeleton when you click **Create** and shows what it found in the confirmation
window. It works with humanoid characters (two arms, two legs, a head). It reads the skeleton's shape (where the
legs, arms and head are, and which bones actually move the mesh), so the bones can be named any way, or not named at
all. Tested kinds of characters:

| Where your character comes from | Shown as |
|---|---|
| Epic's UE5 or UE4 Mannequin skeleton, or a character made for it | UE5 Mannequin / UE4 Mannequin |
| MetaHuman | MetaHuman |
| Mixamo: its own characters, and your own mesh rigged by Mixamo's auto-rigger | Mixamo |
| VRoid Studio and other VRM avatars (see below for importing a .vrm) | VRoid / VRM, or Custom humanoid |
| Rigs made in Blender, with any bone names, even Blender's default Bone, Bone.001, … | Custom humanoid |
| Blender Rigify, exported game-ready (only the DEF- bones, in one hierarchy) | Custom humanoid |
| Game-asset characters: KayKit, Quaternius, Kenney, Polygonal Mind and similar packs | Custom humanoid (or Mixamo) |

Character Creator has been tested with one character so far, and Daz exports not yet: the [Roadmap](../roadmap.md) lists everything that has
been tested and what's next. If your character doesn't work, please tell us (Roadmap, *Report a character*).

**Importing a VRM (.vrm) file.** Unreal doesn't open .vrm files directly, but a .vrm is a glTF file inside: rename
it to `.glb` and drag it into the Content Browser. Then right-click the body mesh (the tallest one) → **Make GASP
Character**; the face and hair meshes are found as extra parts.

**QuickMotion Lite only works with characters on the UE5 Mannequin skeleton** (Manny, Quinn, or characters made for
them). Everything else in this table needs the full QuickMotion.

**If QuickMotion isn't sure about a part** (for example the fingers aren't named, or the head bone is called
something unusual), it still makes your character with its best guess. The notice after Create and the **Result**
line on the settings card name those parts. To fix one:

1. On the settings card, open **More > Bone Matching**. Parts QuickMotion guessed are marked **Needs Check**.
2. Set that part's **Start Bone** and **End Bone** to the right bones of your character.
3. Click **Rebuild**.

**Characters exported from Blender in metres.** Blender's default units often end up as a scale inside the
character's bones. Unreal shows the mesh fine, but characters like this float in the air when they move. QuickMotion
spots this and makes a corrected copy, `SK_<Name>_Fixed`, in the `GASP_<Name>` folder. It looks exactly the same, and
your character uses it. Your own mesh isn't changed. **Rebuild** refreshes the copy, so if you re-import your mesh,
click Rebuild. (To fix the source file too: in Blender set **Unit Scale** to 0.01, scale the armature up 100×, apply
the scale with Ctrl+A, and export again.)

**Characters imported at the wrong size.** Downloads often arrive far too big or too small (a character 4 m tall,
or 10 cm tall) because of the units they were exported in. **Fix Size** on the settings card has three choices:

| Fix Size | What it does |
|---|---|
| **Auto** (the default) | Characters under 50 cm or over 3 m tall (unit mistakes) are shown at the size of GASP's mannequin. Characters in between (children, chibis, ogres) keep their own size. |
| **Human size** | Always the mannequin's height. Use it when an adult character arrived small but not tiny (say 60 cm): GASP's vaults and climbs are made for human size. |
| **Own size** | Never resized. |

When your character is resized, QuickMotion makes a corrected copy at that size (**More > Fixed Copy**; **More >
Display Scale** shows by how much), and the **Result** line says so. Your mesh isn't changed. After changing Fix Size,
click **Rebuild**.

**Other import problems** QuickMotion can't fix for you are named on the settings card's **Result** line, with what
to do: a mesh that's lying down (re-import it standing up), or a skeleton that doesn't line up with its mesh (an
unapplied armature rotation or scale in the file: in Blender, Ctrl+A > All Transforms on the armature and mesh, then
export again). Characters exported facing the wrong way are turned around for you.

**The card only says Ready when the character will work.** After every build QuickMotion checks the result: legs
reaching down to the feet, arms on the right sides, the head at the top, and every body part using bones that
actually move your mesh. If something is off, the **Result** line starts with *Made, but it won't move right yet*
and says what to fix under **More > Bone Matching**.

**When QuickMotion can't make a character**, it says why and leaves nothing behind:

- *The skeleton has no leg bones* (or no arms, or only one): GASP characters need two legs, two arms and a head. If
  your rig does have legs, check they're parented to the hips: Unreal keeps only one root bone when it imports a
  file, so legs that are separate root bones are dropped on import.
- *A Blender Rigify rig exported with its control bones*: Rigify's skinned bones (DEF-) hang from control bones (ORG-,
  MCH-), so they don't form one skeleton a game engine can drive. Export a game-ready version (only the DEF- bones,
  each parented to the DEF- bone above it; Rigify game-export add-ons do this) and try again.

**More > Matched By** says how QuickMotion recognised the skeleton, and **Pelvis Bone** is the bone that moves the
whole body. You rarely need to change either.

