# Changelog


**1.1.0**: many more characters.

- Skeletons are read from their shape (where the legs, arms and head are, and which bones actually move the mesh),
  so bone names no longer matter: Blender's default names, any naming style, glTF number suffixes, Unity-style names.
- Newly supported: meshes rigged by Mixamo's auto-rigger, VRM avatars, Blender rigs (Rigify exported game-ready),
  game-asset packs (KayKit, Kenney, Polygonal Mind), Sketchfab downloads split into several meshes, A-pose rigs,
  characters lying down or facing backwards, rigs with extra IK and control bones, and rigs whose skin sits on twist
  bones rather than the thigh, calf and arm bones (Character Creator style), with finger names such as `Mid1`.
- **Fix Size**: characters imported far too big or small are shown at human size (new setting: Auto by default, or
  always Human size, or Own size).
- The settings card only says **Ready** when its own check passes (legs to the feet, arms on the right sides, head at
  the top, every part on bones that move the mesh); otherwise it says what to fix.
- Clear messages when a skeleton is missing legs or arms, or is a Rigify export with its control bones; a failed
  Create no longer leaves files behind.
- Lite: the same build check, Fix Size and clean failures (Lite still supports UE5 Mannequin characters).

**1.0.0**: first release.
