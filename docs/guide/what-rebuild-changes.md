# What Rebuild changes


Rebuild only refreshes the helper files: `IKR_<Name>`, `RTG_UEFN_To_<Name>`, `ABP_GASP_<Name>` and
`BPV_GASP_<Name>`, plus `SK_<Name>_Fixed` and `ABP_GASP_<Name>_Parts` when your character has them. Don't edit these
by hand, because Rebuild replaces them. The Reference lists [what each file is](../reference/what-quickmotion-makes.md#what-quickmotion-makes).

Rebuild **never** changes:

- **`BP_GASP_<Name>`**, your character Blueprint. QuickMotion makes it once. Components, variables and graphs you add
  to it stay after every Rebuild, even after you swap the mesh.
- **Your mesh, its skeleton, its physics asset, or any other Blueprint of yours.** QuickMotion reads them and never
  saves them.
- **The Game Animation Sample's own files.**

