# Simple Resolve grade for DNG 

It's using a fusion composition with AgX and a couple of nodes to serve as a base grade for DNG sequences.
Works with the free DaVinci Resolve version. 

## Usage:

- Timeline should be set at DaVinci WG/Intermediate and Output to Rec 709 Gamma 2.4
- In the Color tab, select those Camera Raw settings: Color Space Rec.709, Gamma Linear, Tick Highlight Recovery if needed.
- In the Fusion tab, import AgX_lin.comp (File->Import->Fusion Composition...) 
- Click on the middle node named AgX and set the OCIO config path to the config.ocio (Browse). Source should be Linear BT.709, Output Space AgX Base and Look None.
- Copy/paste to all your fusion clips.


## Quick notes: 

Save your Fusion composition (File->Export->Fusion Composition...), so you don't have to set the path anymore.
You could also edit AgX_lin.comp, search for OCIOConfig = Input { Value = 

FYI, to copy/paste to all your clips, select your clips with shift then middle click, whether you are in the fusion or the color tab.

It's using https://github.com/sobotka/AgX-Resolve.

