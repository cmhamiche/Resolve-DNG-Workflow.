# Simple Resolve grade for DNG 

It's using a fusion composition with AgX and a couple of nodes to serve as a base grade for DNG sequences.
Works with the free DaVinci Resolve version. 

## Usage:

- Timeline should be set at DaVinci WG/Intermediate and Output to Rec 709 Gamma 2.4
- In the Fusion tab, import the Fusion Composition named AgX_EOSM.comp (File->Import->Fusion Composition...). Paste it to all your fusion clips.
- In the Color tab, select those Camera Raw settings: Color Space Rec.709, Gamma Linear, Tick Highlight Recovery if needed.


## Quick notes: 

The OCIO config of fusion's node named OCIOColorspace1 should point to "config.ocio".

FYI, to copy/paste to all your clips, select your clips with shift then middle click, whether you are in the fusion or the color tab.

It's using https://github.com/sobotka/AgX-Resolve.

