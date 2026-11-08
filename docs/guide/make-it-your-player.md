# Make it your player


The Tutorial has you place `BP_GASP_<Name>` in the level and set **Auto Possess Player** to **Player 0**. That's
the quickest way to try it. To play as your character every time you press Play, without placing it first:

1. In the Content Browser, open `Content/Blueprints`, right-click **GM_Sandbox** (GASP's game mode) and choose
   **Create Child Blueprint Class**. Name it, for example, `GM_MyGame`.
2. Open `GM_MyGame`. In **Class Defaults**, set **Default Pawn Class** to **BP_GASP_\<Name\>**. Compile and save.
3. Choose where it applies:
   - **One level:** open the level, then **Window > World Settings** > **GameMode Override** > `GM_MyGame`.
   - **Every level:** **Edit > Project Settings > Maps & Modes** > **Default GameMode** > `GM_MyGame`.
4. Press **Play**. You start as your character.

If you placed a `BP_GASP_<Name>` with Auto Possess Player in the level earlier, delete it or set Auto Possess Player
back to **Disabled**, so you don't get two players.

**As an NPC:** drag `BP_GASP_<Name>` into the level and leave Auto Possess Player on **Disabled**. It stands in the
level with GASP's animation. Moving it around is up to your own AI.

**Your own character class:** `BP_GASP_<Name>` is a child of GASP's `SandboxCharacter_Mover`. Add your gameplay to it
directly, or make child Blueprints of it for variations.

