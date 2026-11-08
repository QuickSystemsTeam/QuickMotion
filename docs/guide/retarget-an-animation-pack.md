# Retarget an animation pack


GASP covers moving around. For other moves (a sword pack, emotes), retarget the pack's animations onto your character
with Unreal's own tools. QuickMotion already made the part you need: **`IKR_<Name>`**, an IK Rig for your character
with its body parts named the standard way.

1. In the Content Browser, select the pack's animations, right-click and choose **Retarget Animations**.
2. Set **Source Skeletal Mesh** to the pack's character (for example `SKM_Manny` for packs made for the UE5
   Mannequin) and **Target Skeletal Mesh** to your character's mesh.
3. If Unreal asks for an IK Retargeter, make one (right-click > Animation > Retargeting > IK Retargeter) with the
   pack's IK Rig as **Source** (for UE5 Mannequin packs: `IK_UE5_Mannequin_Retarget`) and **`IKR_<Name>`** as
   **Target**. Because QuickMotion names the body parts the standard way, the chains pair up on their own.
4. Click **Export Animations**.

Packs made for GASP's own mannequin can use **`RTG_UEFN_To_<Name>`** directly as the retargeter.

