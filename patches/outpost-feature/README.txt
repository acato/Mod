Outpost Feature — Test Build
=============================
Branch: experiment/new-feature
Base: We The People 4.2.1
DLL: Assert build (includes FAssert checks for testing)

What this adds
--------------
A new "Outpost" improvement that lets pioneers scavenge resources from
bonus tiles outside your cultural borders.

- A pioneer builds an outpost on an unowned tile that has a scavengeable
  bonus (furs, wood, etc.). The pioneer is consumed during construction.
- Each turn the outpost gathers yield (base + terrain + bonus). If the
  pioneer had an expert profession (lumberjack, hunter, fur trapper),
  those bonuses apply to the gathering rate.
- At 100 accumulated yield the outpost disbands and spawns the original
  pioneer plus a goods cart carrying the harvested yield.
- If another civ's borders expand over the tile, the outpost auto-disbands
  and returns whatever has been gathered so far.
- Pillaging by an enemy destroys the outpost; both pioneer and goods
  are lost.

Build cost: 800 time, 20 gold (same as trapper hut).

Installation
------------
1. Back up your current WtP mod folder (recommended).
2. Extract this ZIP into your WtP mod root folder — the one that
   contains the "Assets" directory.
   On a default Steam install this is typically:
     ...\Sid Meier's Civilization IV Colonization\Mods\WTP\
3. When prompted, choose "Replace existing files".
4. Launch the game normally.

To uninstall, restore the backed-up files or re-verify your WtP
installation.

Files included
--------------
Assets/CvGameCoreDLL.dll                          — compiled DLL (Assert)
Assets/XML/Terrain/CIV4BonusInfos.xml             — bScavengeable on 11 bonuses
Assets/XML/Terrain/CIV4ImprovementInfos.xml       — IMPROVEMENT_OUTPOST
Assets/XML/Terrain/CIV4TerrainSchema.xml          — bScavengeable + bOutpost schema
Assets/XML/Text/CIV4GameText_WTP_utf8.xml         — UI text keys
Assets/XML/Units/CIV4BuildInfos.xml               — BUILD_OUTPOST
Assets/XML/Units/CIV4UnitInfos.xml                — BUILD_OUTPOST on pioneer unit

Note: This is an Assert build that also includes other in-progress
changes from the experiment/new-feature branch (event improvements,
AI fixes, etc.). It is intended for testing, not production use.
