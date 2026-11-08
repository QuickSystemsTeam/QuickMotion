# Characters made of several meshes


Many characters come as more than one mesh: a MetaHuman's body, face and clothes, or a VRoid avatar's body, face
and hair (glTF and VRM imports often split like this). Right-click the **body** mesh. QuickMotion finds the other
pieces and makes them all move together:

- **MetaHumans:** from the MetaHuman's own Blueprint, wherever its pieces are stored.
- **Everything else:** meshes in the **same folder** as the body that share its bones and cover only part of the body
  (a whole second character in the same folder is never treated as a piece).

They're listed on the settings card under **More > Extra Parts**. To add a piece QuickMotion missed or remove one,
edit the list and click **Rebuild**. Pieces with bones of their own, like separately rigged hair, still follow the
head.

