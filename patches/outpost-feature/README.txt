Outpost Feature Patch
=====================

This patch adds a new "Outpost" improvement that lets pioneers scavenge
resources from bonus tiles outside your cultural borders.

How it works:
- A pioneer builds an outpost on an unowned tile with a scavengeable bonus
  (furs or wood). The pioneer is consumed during construction.
- Each turn the outpost gathers yield (base + terrain + bonus). If the
  pioneer had an expert profession (lumberjack, hunter, fur trapper),
  those bonuses apply to the gathering rate.
- At 100 accumulated, the outpost disbands and spawns the original pioneer
  plus a goods cart carrying the harvested yield.
- If another civ's borders expand over the tile, the outpost auto-disbands
  with whatever has been gathered so far.
- Pillaging destroys the outpost; both pioneer and goods are lost.

Build cost: 800 time, 20 gold (same as trapper hut).

Applying the patch
------------------

From the root of the WTP repository (the Mod/ directory):

    git apply outpost-feature.patch

Or to apply as a commit preserving authorship:

    git am outpost-feature.patch

If you prefer to review first:

    git apply --stat outpost-feature.patch   # show file stats
    git apply --check outpost-feature.patch  # dry-run check

Files modified
--------------

XML:
  Assets/XML/Terrain/CIV4BonusInfos.xml       - bScavengeable on 11 bonuses
  Assets/XML/Terrain/CIV4ImprovementInfos.xml - IMPROVEMENT_OUTPOST
  Assets/XML/Terrain/CIV4TerrainSchema.xml    - bScavengeable + bOutpost schema
  Assets/XML/Text/CIV4GameText_WTP_utf8.xml   - 6 text keys
  Assets/XML/Units/CIV4BuildInfos.xml         - BUILD_OUTPOST
  Assets/XML/Units/CIV4UnitInfos.xml          - BUILD_OUTPOST in pioneer builds

DLL:
  Project Files/DLLSources/CvInfos.h          - bScavengeable, bOutpost accessors
  Project Files/DLLSources/CvInfos.cpp        - read/write/XML load
  Project Files/DLLSources/CvPlot.h           - outpost state + methods
  Project Files/DLLSources/CvPlot.cpp         - doOutpostTurn, disbandOutpost, canBuild
  Project Files/DLLSources/CvPlotSavegame.cpp - savegame serialization
  Project Files/DLLSources/CvUnit.cpp         - outpost init on build complete

Branch: experiment/new-feature
Base: origin/develop
