# A fusion composition to serve as a base grade for DNG sequences. Works with the free DaVinci Resolve version. 

The way Resolve's Camera Raw handles DNG is different than other RAW video formats: it is a simple mapping to a display referred (not scene referred) workspace and it doesn't clip anything regardless of the timeline settings. 
Those are the main issues we're trying to solve here. It is comprised of a curve, a tone mapper and few saturation adjustments.

It's graded according to my taste and might be subject to change. It's using https://github.com/sobotka/AgX-Resolve.

## DEMO

https://github.com/user-attachments/assets/5b308fdc-5dc6-4111-9aad-328613015d19

## Usage:


#### 1. In the "Fusion" tab, import "AgX_lin.comp" (File ->Import->Fusion Composition...)

Select the node named "AgX" and set the "OCIO config path" to the "config.ocio" (Browse). Source should be "Linear BT.709", "Output Space" "AgX Base" and "Look" "None".

Copy/paste (middle click) to all your fusion clips. You can switch to the "Color" tab.
  
![3 Fusion](https://github.com/user-attachments/assets/e2f4a592-3389-4fc5-aad8-2927be312b42)


#### 2. In the "Color" tab, change this "Camera Raw" settings: "Gamma" "Linear".

Copy/paste (middle click) to all your clips, you can start grading as usual.
  
![2  Camera Raw](https://github.com/user-attachments/assets/64492b10-b181-4220-bb86-f8411279d62b)


## Quick notes: 

- **Save your Fusion composition (File->Export->Fusion Composition...), so you don't have to set the path and do your settings anymore.**
Alternatively, you can edit AgX_lin.comp to set the path with a text editor, search for "OCIOConfig = Input", exemple: OCIOConfig = Input { Value = "D:\\Resolve_DNG_Workflow\\Grades\\AgX\\config.ocio", },

- **If your playback isn't realtime you can set you playback resolution to half (Playback->Timeline Proxy Resolution->Half).** Works great if you want to start editing/grading while MLVApp is still dumping.

- If you tick "Highlight Recovery" you might get some bad banding where it's overexposed (low saturation is fine, like recovering details on a white object).

- To copy/paste settings to all your clips (set everything to Linear for exemple), select your ungraded clips with shift and then middle click on the clip you want to copy from. Works whether you are in the Fusion or the Color tab.

- Unfortunatly the black levels of my DNG sequences are not as consistent as I'd like so depending on the clip's exposure you might want to adjust the lift in Camera Raw, -0.5<0.15.

- (Optional) I prefer my "Timeline" to be set to "DaVinci WG/Intermediate" ("Rec 709 Scene" is also fine) "and "Output" to "Rec 709 Gamma 2.4"
  
 ![1  Color Management](https://github.com/user-attachments/assets/59c6d16e-b9ef-4ba2-adf8-7818d9465725)

- (Optional) Since my "Timeline" is set to "DaVinci WG/Intermediate", I set my clip's Color Space and Gamma manually (but "auto" is also fine):
  
 ![349058366-3b5406cf-0b00-4c83-828c-3c5f92e8024e](https://github.com/user-attachments/assets/6a5ffb92-4564-49a6-b6f1-8e4feeb77efe)

 
