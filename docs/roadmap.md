# Roadmap

QuickMotion 1.0 is out on Fab (full and Lite). This page says honestly what it has been tested with, what we're
testing next, and what we plan to add. It has no dates: things move up when testing or your reports show they
matter. If your character doesn't work, please tell us (see **Report a character** below): that's how this list
gets shorter.

## Tested with in 1.0

Every release is checked in a fresh Game Animation Sample (UE 5.8) project, installed the way Fab installs it, and in
packaged Windows games (a player plus 10 characters).

| Character | Where it came from | How it was imported |
|---|---|---|
| Kellan (MetaHuman, face and clothing) | Epic's Game Animation Sample | As shipped in the sample |
| VRoid AvatarSample | VRoid Studio | The `.vrm` file through Unreal's own glTF importer |
| Y Bot | Mixamo | Mixamo's FBX |
| Universal Base Characters "Superhero" (the try-it character) | Quaternius, CC0 | Their Unreal-ready glTF |
| UE5 Mannequin (Manny, Quinn) | Epic | As shipped |

We also test made-up skeletons for each family (UE5, UE4, MetaHuman-style, Mixamo, VRoid, custom names, and one
with unusual names), and common import problems: a mesh facing backwards, a Blender export in metres, a spine
attached to the root instead of the hips, arms down instead of a T-pose, no finger bones. QuickMotion fixes these or,
for a mesh lying down or imported far too big or small, tells you what to change.

## Testing next

Characters the way most people get them. Each one gets the same check: Make GASP Character, press Play, and look at
walking, running, vaulting and climbing, hands included. We'll publish what works and what doesn't here.

- **VRoid through the VRM4U plugin** (the most common way to bring VRoid characters into Unreal).
- **Your own mesh rigged by Mixamo's auto-rigger** (not only Mixamo's own characters).
- **Sketchfab rigged humanoids** with their own bone names.
- **Character Creator and Daz exports.**
- **Ready Player Me and other avatar services.**
- **Quaternius' FBX files** (we tested their glTF; their FBX has a known scale issue).
- **Unfinished skeletons**, for example a rig with only the upper body done, or no fingers yet: what you get, and what
  QuickMotion tells you.
- **Rest poses other than a T-pose** (A-pose, relaxed arms).

## Planned

- Fixes for whatever the tests above turn up, starting with the most common character sources.
- Clearer messages when a skeleton is missing parts GASP needs (legs, arms, head), so you know what to add.
- Batch setup: make GASP characters for several meshes at once and reuse one setup for characters that share a
  skeleton.
- Newer engine versions when Epic releases a matching Game Animation Sample.

Ideas we're considering, depending on demand: help bringing GASP into an existing project, weapon sockets and hand
IK for held items, and crowds of NPCs.

## Report a character

Email [quicksystemssupport@gmail.com](mailto:quicksystemssupport@gmail.com) with where the character came from (a link if it's public), how you imported it, and the
**Result** line from the settings card. A screenshot of the confirmation window after you click Create helps too.
