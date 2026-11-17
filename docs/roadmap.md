# Roadmap

QuickMotion is on Fab (full and Lite). This page says honestly what it has been tested with, what we're testing next,
and what we plan to add. It has no dates: things move up when testing or your reports show they matter. If your
character doesn't work, please tell us (see **Report a character** below): that's how this list gets shorter.

## Tested with (1.1)

Every release is checked in a fresh Game Animation Sample (UE 5.8) project, installed the way Fab installs it, and in
packaged Windows games (a player plus 10 characters).

**Real characters from the community**, each imported with Unreal's default settings and made with one right-click:

| Kind | Characters tested |
|---|---|
| Epic | UE5 Mannequin (Manny, Quinn), MetaHuman Kellan (face and clothing) |
| Mixamo | Y Bot, Remy, Kaya, and a mesh rigged by Mixamo's auto-rigger |
| VRoid / VRM | VRoid Studio sample avatars, a VRoid Hub avatar, other VRM avatars (Orion, Seed-san, a voxel Meebit) |
| Game-asset packs | KayKit Adventurers (Knight, Mage, Rogue), Kenney Animated Characters, Quaternius Universal Base Characters (glTF and FBX), Polygonal Mind 100 Avatars |
| Sketchfab and itch.io downloads | rigs with Blender's default bone names, a Unity-style humanoid, a body scan split into several meshes, hand-named rigs ("Upper Arm L") |
| Blender | A-pose rigs, Rigify exported game-ready |

**Generated variants of five rigs** (Quaternius, Mixamo, VRoid, Kenney, Rigify), each with a known answer the test
checks automatically: bones renamed in every common style (Blender `.L`/`.R`, `Upper Arm L`, Unity `LeftUpperArm`,
`l_` prefixes, glTF number suffixes) or not named at all, bone rolls flipped or random, joints moved by up to 3% of
the height, extra IK and control bones, missing fingers, neck, toes or clavicles, A-pose at 30° and 50°, 100× too big
and too small, facing backwards, spine on the root, no root bone, and combinations of these. Rigs with only an upper
body, one arm or no arms must be refused with a clear message.

## What doesn't work yet

- **Blender Rigify exported with its control bones.** QuickMotion explains this and how to export a game-ready
  version (only the DEF- bones, in one hierarchy).
- **Rigs whose legs aren't parented to the hips.** Unreal keeps only one root bone on import, so separate leg roots
  are dropped before QuickMotion sees them; QuickMotion says so.
- **Files whose skeleton doesn't line up with the mesh** (an unapplied armature rotation or scale). QuickMotion
  points to the fix in Blender.

## Testing next

- **Character Creator and Daz exports.**
- **VRoid through the VRM4U plugin** (we test VRM files through Unreal's own glTF importer today).
- **More Sketchfab and itch.io downloads**: send us the ones you use.
- **Very stylised bodies** (tiny legs, huge heads, very long arms) in more poses.

## Planned

- Fixes for whatever the tests above and your reports turn up, most common character sources first.
- Batch setup: make GASP characters for several meshes at once, and reuse one setup for characters that share a
  skeleton.
- Newer engine versions when Epic releases a matching Game Animation Sample.

Ideas we're considering, depending on demand: help bringing GASP into an existing project, weapon sockets and hand
IK for held items, and crowds of NPCs.

## Report a character

Email [quicksystemssupport@gmail.com](mailto:quicksystemssupport@gmail.com) with where the character came from (a
link if it's public), how you imported it, and the **Result** line from the settings card. A screenshot of the
confirmation window after you click Create helps too.
