# Resolve grade for DNG 
It's using a fusion composition with AgX and a simple power grade to serve as a base for a grade.
Works with the free DaVinci Resolve version. 

Uncompress the Grades folder in C:\ProgramData\Blackmagic Design\DaVinci Resolve\
In the Fusion tab, import the Fusion Composition C:\ProgramData\Blackmagic Design\DaVinci Resolve\Grades\AgX.comp (the OCIO config should point to C:\ProgramData\Blackmagic Design\DaVinci Resolve\Grades).
In the Color tab, import the Power Grade C:\ProgramData\Blackmagic Design\DaVinci Resolve\Grades\AgX.drx and adjust temperature and exposure values in Camera Raw.


Default is raw interpreted as rec.709/srgb to srgb/AgX Punchy but you can use linear and base AgX for exemple.
