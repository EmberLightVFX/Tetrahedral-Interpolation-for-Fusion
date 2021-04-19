# Tetrahedral Interpolation for Blackmagic Design Fusion

Color transformations using tetrahedral interpolation, includes both an implemention for the expression node and blinkscript. I never managed to solve an inverse function for this to round trip back, which is something I came really close to but eventually scrapped. So for now only a simple forward operation.

For folks unfamiliar with Steve Yedlin, ASC: These implementations are supposed to be replications of the one's Yedlin showcasesd. A video where he willingly showed half of the blinkscript code can be found in the end of this page below (0:14:30). Where I only attemped to reconstruct the missing parts with the help of some math from various papers also linked in the end of the page below, which I then later also translated to the expression node for NC Nuke users.

TetraAutomater is only the suggestion of what it could be doing, since it was never mentioned.

I just want to be able to share these for everyone to use. So I don't expect any credit from it!

Video demonstration: https://www.youtube.com/watch?v=8kBkYEiAkIw

### Information

Color transformations using tetrahedral interpolation, includes both an macro (sadly slow) and a DCTL fuse (fast).
Code comes from https://github.com/calvinsilly/Tetrahedral-Interpolation
HSV code comes from https://github.com/TheDIGuy/TetraInterp-DCTL


### To install this fuse for Blackmagic Fusion Studio, copy the file to your UserData Path Map folder:

Linux:
  ~/.fusion/BlackmagicDesign/Fusion/Fuses
  
OSX: 
  ~/Library/Application Support/Blackmagic Design/Fusion

Windows:
  %appdata%\Blackmagic Design\Fusion\Fuses


### For the Fusion page in Resolve Lite or Resolve Studio use these UserData folders:

Linux: 
  ~/.local/share/DaVinciResolve/Fusion/Fuses

OSX:
  ~/Library/Application Support/Blackmagic Design/DaVinci Resolve/Fusion

Windows:
  %appdata%\Blackmagic Design\DaVinci Resolve\Fusion\Fuses
  
  
  
#### If you want to install the macro, place the file in the Macro folder instead of the Fuse folder
