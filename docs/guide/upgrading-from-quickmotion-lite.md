# Upgrading from QuickMotion Lite


QuickMotion Lite makes GASP characters from meshes on the UE5 Mannequin skeleton. The full QuickMotion also handles
MetaHuman, VRoid, Mixamo and custom humanoids, and lines up hands and fingers with GASP's mannequin.

To upgrade, close the editor, remove QuickMotion Lite from your project's `Plugins` folder (or disable it in
**Edit > Plugins**), add QuickMotion, and open the project. Characters you made with Lite open as they are, keep
working, and can be rebuilt with the full version. Don't enable both plugins at the same time.
