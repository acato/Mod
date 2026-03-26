Enhanced Canals - Chainable Canal Chains
=========================================

This patch allows canals to be built adjacent to existing canals,
enabling multi-tile canal chains that connect water bodies.

Features:
- Canals can chain: build adjacent to water OR an existing canal
- Exponential cost scaling: each additional canal in a chain doubles
  both gold cost and build time (2nd = 2x, 3rd = 4x, 4th = 8x, etc.)
- Coastal ships can traverse the full chain
- Ocean-going ships are still blocked from entering canals
- BFS-based water area resolution for mid-chain canals
- Capped at 20 tiles per chain (20th tile = ~15.7M gold)

Installation (WtP 4.2.1):
1. Back up your existing files first!
2. Copy Assets/CvGameCoreDLL.dll over your mod's Assets/CvGameCoreDLL.dll
3. Copy Assets/XML/Terrain/CIV4ImprovementInfos.xml over your mod's
   Assets/XML/Terrain/CIV4ImprovementInfos.xml
4. Launch the game with the mod

Savegame Compatibility:
- Fully compatible with existing saves (no new variables added)

Files included:
- Assets/CvGameCoreDLL.dll          (Release build)
- Assets/XML/Terrain/CIV4ImprovementInfos.xml  (canal adjacency change)
