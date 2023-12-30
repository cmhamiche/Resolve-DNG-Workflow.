# Resolve grade for DNG 
It's using a fusion composition with AgX and a simple power grade to serve as a base for a grade.
Works with the free DaVinci Resolve version. 

Installation:
Uncompress the Grades folder in "C:\ProgramData\Blackmagic Design\DaVinci Resolve\"

Usage:
- In the Fusion tab, import the Fusion Composition from "C:\ProgramData\Blackmagic Design\DaVinci Resolve\Grades\AgX.comp" (the OCIO config should point to C:\ProgramData\Blackmagic Design\DaVinci Resolve\Grades\AgX\config.ocio).
.Copy, paste to all your fusion clips (or select your clips with shift then middle click).
- In the Color tab, import the Power Grade from "C:\ProgramData\Blackmagic Design\DaVinci Resolve\Grades\AgX.drx"
Copy, paste to all your clips (or select your clips with shift then middle click) and adjust temperature/exposure values in Camera Raw.


Default is raw interpreted as rec.709/srgb to srgb/AgX Punchy but you can use linear and AgX Base for exemple.
