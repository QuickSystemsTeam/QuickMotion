# Supported characters


QuickMotion reads your character's skeleton when you click **Create** and shows what it found in the confirmation
window. It works with humanoid characters (two arms, two legs, a head) from:

| Where your character comes from | Shown as |
|---|---|
| Epic's UE5 or UE4 Mannequin skeleton, or a character made for it | UE5 Mannequin / UE4 Mannequin |
| MetaHuman | MetaHuman |
| Mixamo | Mixamo |
| VRoid Studio (VRM) | VRoid / VRM |
| Anything else with a humanoid skeleton: Blender, Character Creator, Daz, your own rig | Custom humanoid |

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

**Other import problems** QuickMotion can't fix for you are named on the settings card's **Result** line, with what
to do: a mesh that's lying down (re-import it standing up), or one that's far too big or too small (re-import with a
different Import Uniform Scale). Characters exported facing the wrong way are turned around for you.

**More > Matched By** says how QuickMotion recognised the skeleton, and **Pelvis Bone** is the bone that moves the
whole body. You rarely need to change either.

