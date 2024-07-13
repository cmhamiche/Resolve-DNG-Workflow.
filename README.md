# Simple Resolve grade for DNG 

A fusion composition to serve as a base grade for DNG sequences. Works with the free DaVinci Resolve version. 

The way Resolve's Camera Raw color space handles DNG is different than other RAW files: it doesn't clip regardless of the timeline and it's display referred. 
Those are the main issues we're trying to solve here. It is comprised of a curve, a tone mapper and few saturation adjustments.

It's graded according to my taste and might be subject to change.


## Usage:

- "Timeline" should be set at "DaVinci WG/Intermediate" and "Output" to "Rec 709 Gamma 2.4"
![1  Color Management](https://github.com/user-attachments/assets/7ebe9465-b039-4d42-921e-1668ca289af9)

- In the "Color" tab, select those "Camera Raw" settings: "Color Space" "Rec.709", "Gamma" "Linear". You might get some harsh highlights clipping if you tick "Highlight Recovery" so double check.
![2  Camera Raw](https://github.com/user-attachments/assets/64492b10-b181-4220-bb86-f8411279d62b)

- In the "Fusion" tab, import "AgX_lin.comp" (File ->Import->Fusion Composition...) 
- Click on the middle node named "AgX" and set the "OCIO config path" to the "config.ocio" (Browse). Source should be "Linear BT.709", "Output Space" "AgX Base" and "Look" "None".
![3 Fusion](https://github.com/user-attachments/assets/e2f4a592-3389-4fc5-aad8-2927be312b42)

- Copy/paste to all your fusion clips then you can switch back to the "Color" Tab to finish your grade.


## Quick notes: 

Save your Fusion composition (File->Export->Fusion Composition...), so you don't have to set the path anymore.
You could also edit AgX_lin.comp, search for OCIOConfig = Input { Value = 

To copy/paste settings to all your clips (to quickly set everything to Linear for exemple), select your ungraded clips with shift, then middle click on the clip you want to copy from. Works whether you are in the Fusion or the Color tab.

If your playback isn't realtime you can set you playback resolution to half (Playback->Timeline Proxy Resolution->Half). Works great if you want to start editing/grading while MLVApp is still dumping.

It's using https://github.com/sobotka/AgX-Resolve.
