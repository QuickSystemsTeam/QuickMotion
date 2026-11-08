# 2. Make your GASP character



1. In the **Content Browser**, find your character's Skeletal Mesh.
2. Right-click it and choose **Make GASP Character**.
3. A small window shows what QuickMotion found (for example "Skeleton: UE5 Mannequin") and where it will put the new
   files. Click **Create**.

After a few seconds a notice says the character is ready and its **settings card** opens. Next to your mesh there's
a new folder, `GASP_<Name>`:

| File | What it is |
|---|---|
| `BP_GASP_<Name>` | **Your GASP character.** A normal Blueprint: it's yours to use and edit. |
| `GASP_<Name>_Setup` | The settings card. Change things here and click Rebuild. |
| `IKR_<Name>`, `RTG_UEFN_To_<Name>`, `ABP_GASP_<Name>`, `BPV_GASP_<Name>` | Helper files QuickMotion keeps up to date. You don't need to open them. |

