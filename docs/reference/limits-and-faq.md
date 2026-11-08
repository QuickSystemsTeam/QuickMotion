# Limits and FAQ


**Which Unreal Engine and Game Animation Sample versions?**
Unreal Engine **5.8** with the Game Animation Sample **5.8** (the Mover-based version), Windows 64-bit editor.
Characters are tested in a packaged Windows game.

**Do I need the Game Animation Sample?**
Yes, in the same project. It's free on Fab. QuickMotion doesn't include, copy or change any of its files: it only
reads them to build your character.

**Which characters work?**
Humanoids with two arms, two legs and a head: MetaHuman, VRoid / VRM, Mixamo, UE4 and UE5 Mannequin characters, and
custom humanoids (Blender, Character Creator, Daz, your own rigs). See [Supported characters](../guide/supported-characters.md#supported-characters).
Quadrupeds, creatures with extra limbs and other non-humanoids don't work.

**What's the difference between QuickMotion and QuickMotion Lite?**

| | Lite | QuickMotion |
|---|---|---|
| Right-click → Make GASP Character, settings card, Rebuild | ✓ | ✓ |
| Characters on the UE5 Mannequin skeleton | ✓ | ✓ |
| MetaHuman, VRoid, Mixamo, UE4 Mannequin, custom humanoids | | ✓ |
| Fix Hands (wrists and fingers lined up with GASP's mannequin) | | ✓ |
| Characters made of several meshes (face, hair, clothes) | | ✓ |
| Detect Rig for scripts | | ✓ |
| Sample character to try it on | GASP's own Quinn | ✓ (included) |

Don't enable both plugins in one project. To move up, see [Upgrading from QuickMotion Lite](../guide/upgrading-from-quickmotion-lite.md#upgrading-from-quickmotion-lite).

**Will it change my mesh, skeleton or Blueprints?**
No. QuickMotion only makes new files in a new folder (see [What QuickMotion makes](what-quickmotion-makes.md#what-quickmotion-makes)). If your
mesh needs fixing (the Blender units problem), it makes a corrected copy and leaves yours as it is.

**My character is lying down, or far too big or small.**
That comes from how the mesh was imported, and the settings card's **Result** line says so with the fix: re-import it
standing up, or with a different Import Uniform Scale, then click **Rebuild**. Characters exported facing backwards,
or with the Blender units problem, are fixed for you.

**How much does each character cost in performance?**
Very little: the character's own mesh is animated from GASP's mannequin every frame. On our test PC, each QuickMotion
character took about 0.15 ms more game-thread time than one of GASP's own characters, measured with 11 characters on
screen. Large crowds (dozens of GASP characters) aren't something QuickMotion or GASP aims for.

**Can I add weapons, combat or my own moves?**
QuickMotion makes characters move with GASP. Gameplay (combat, weapons, abilities, input) is up to your project. For
extra animations, [retarget an animation pack](../guide/retarget-an-animation-pack.md#retarget-an-animation-pack) onto your character with the
IK Rig QuickMotion made. Holding props in the hands with IK isn't included.

**Can I put GASP into an existing project, or replace Lyra's movement with it?**
Not with QuickMotion. Start from a project that has the Game Animation Sample, or add the sample to your project
first (see [Use your character in another project](../guide/use-your-character-in-another-project.md#use-your-character-in-another-project)).

**Something looks wrong in GASP itself.**
QuickMotion doesn't change GASP, so issues in GASP's own animation or movement show on GASP's mannequin too. Check
Epic's Game Animation Sample forum threads for known issues.

**Does it swap my character to a different skeleton?**
No. Your character keeps its own skeleton; QuickMotion drives it from GASP's mannequin as it plays.

