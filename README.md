# Simple Resolve grade for DNG 

It's using a fusion composition with AgX and a simple power grade to serve as a base for a grade.
Works with the free DaVinci Resolve version. 

## Installation:
Uncompress the "Grades" folder in "C:\ProgramData\Blackmagic Design\DaVinci Resolve\"

## Usage:

- In the Fusion tab, import the Fusion Composition named AgX.comp (File->Import->Fusion Composition...). Copy, paste to all your fusion clips.

- In the Color tab, import the Power Grade named AgX.drx (Right click on the Gallery, Import). Copy, paste to all your clips 

## Quick notes: 

Adjust temperature and exposure values in Camera Raw. Enable Highlight Recovery if needed. There's a red shift since tint is at 10 by default, put that value at 0 for Daylight temperature.

For the people in the back: AgX.comp and AgX.drx are in "C:\ProgramData\Blackmagic Design\DaVinci Resolve\Grades".

The OCIO config of fusion's node named OCIOColorspace1 should point to "C:\ProgramData\Blackmagic Design\DaVinci Resolve\Grades\AgX\config.ocio".

If you uncompress the files elsewhere you'll have to fix the paths and save your composition and power grade.

Default is raw interpreted as rec.709/sRGB to fusion AgX Base/sRGB but you can use rec.709/linear and AgX Punchy/linear for exemple.

For simplicity sake, I have sticked to DaVinci YRGB as color science and rec.709 (scene) for the timeline and output color space. If you want to use DaVinci Wide Gamut/Intermediate, you'll have to adjust your curve accordingly.

FYI, to copy/paste to all your clips, select your clips with shift then middle click, whether you are in the fusion or the color tab.

