# Use your character in another project


The character needs GASP, so the other project needs GASP too:

1. Add the Game Animation Sample to the other project, following Epic's guidance on the sample's Fab page.
2. Enable **QuickMotion** in the other project (Edit > Plugins). The character uses a small QuickMotion component at
   runtime, so the plugin must be there.
3. In this project, right-click your `GASP_<Name>` folder > **Migrate**, and pick the other project's `Content`
   folder. Unreal brings your mesh along with it.
4. In the other project, open the settings card and click **Rebuild** once.

