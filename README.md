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

To copy/paste settings to all your clips (to quickly set everything to Linear for exemple), select your ungraded clips with shift, then middle click on the clip you want to copy from. Works whether you are in the Fusion or the Color tab.

If your playback isn't realtime you can set you playback resolution to half (Playback->Timeline Proxy Resolution->Half). Works great if you want to start editing/grading while MLVApp is still dumping.

It's using https://github.com/sobotka/AgX-Resolve.

