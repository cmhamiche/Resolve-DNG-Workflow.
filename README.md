## Resolve grade for DNG 

It's using a fusion composition with AgX and a simple power grade to serve as a base for a grade.
Works with the free DaVinci Resolve version. 

# Installation:
Uncompress the Grades folder in "C:\ProgramData\Blackmagic Design\DaVinci Resolve\"

# Usage:

- In the Fusion tab, import the Fusion Composition named AgX.comp. Copy, paste to all your fusion clips.

- In the Color tab, import the Power Grade named AgX.drx. Copy, paste to all your clips 

# Quick notes: 

For the people in the back: AgX.comp and AgX.drx are in "C:\ProgramData\Blackmagic Design\DaVinci Resolve\Grades"

Adjust temperature and exposure values in Camera Raw.

The OCIO config should point to C:\ProgramData\Blackmagic Design\DaVinci Resolve\Grades\AgX\config.ocio

Default is raw interpreted as rec.709/sRGB to AgX Punchy/sRGB but you can use rec.709/linear and AgX Base/linear for exemple.

For simplicity sake, I sticked to DaVinci YRGB as color science et rec.709 (scene) for the timeline color space, If you use DaVinci Wide Gamut/Intermediate, adjust your curve accordingly.

To copy/paste to all your clips, select your clips with shift then middle click, whether you are in the fusion or the color tab.

