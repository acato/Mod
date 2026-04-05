Ice Hut & Outpost Improvements - Test Package
===============================================

This package includes the Ice Hut improvement and the Outpost feature
for frontier resource scavenging on unowned tiles.

INSTALLATION:
1. Back up your existing files first!
2. Copy these files into your WTP mod folder, preserving paths:
   - CvGameCoreDLL.dll          -> Assets/CvGameCoreDLL.dll
   - CIV4ImprovementInfos.xml   -> Assets/XML/Terrain/CIV4ImprovementInfos.xml
   - CIV4BonusInfos.xml         -> Assets/XML/Terrain/CIV4BonusInfos.xml
   - CIV4BuildInfos.xml         -> Assets/XML/Units/CIV4BuildInfos.xml
   - CIV4UnitInfos.xml          -> Assets/XML/Units/CIV4UnitInfos.xml
   - XML_AUTO_UTF8_BuildInfo.xml -> Assets/XML/Text/XML_AUTO_UTF8_BuildInfo.xml
   - XML_AUTO_UTF8_ImprovementInfo.xml -> Assets/XML/Text/XML_AUTO_UTF8_ImprovementInfo.xml

OUTPOST TESTING:
- Send a Pioneer to an unowned tile with a scavengeable resource
  (deer, bison, caribou, moose, fox, fur, timber, hardwood, etc.)
- The "Build Outpost" action should appear
- After building (~8 turns), the pioneer is consumed
- The outpost gathers yield each turn until 100 units accumulated
- On completion: pioneer respawns (with tools) + goods cart with resources

Built from branch: integration/play-build (Assert/debug build)
