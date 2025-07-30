# Compositing in DVR

&#x20;**SynthEyes : Export Composition to Fusion**

File  ⇒ Export ⇒ Fusion ⇒ Fusion Composition

Select a path for the export

Start Frame = 1

Project Color Depth = 32 bit float per channel

check HiQ by default

Uncheck Use LensDistort node and Allow solver distortion (because we'll use STMAP)

STMAP file type = OpenEXR Files

check Use Fusion meshes

uncheck Include ambiant (light)

check Export to clipboard

**Fusion : Final Compositing**

Drag and drop the export from blender to create a MediaIn2 node

Add a comment to specify which folder was used

Link the MediaIn2 to a new Gamut node :

* Right click ⇒ Add Tool ⇒ Color ⇒ Gamut
* Select sRGB as Output Space
* Check Pre-Divide / Post-Multiply

Link the Gamut node to the Cam1Redistorter (unlink Cam1Renderer)

Merge the Cam1Redistorter to MediaIn1

Link the Merge to MediaOut1

**Deliver : Export**

Select type (H.24 Master / Youtube, etc)

Change File Name

For Youtube :

* Add a title
* Change the type to : Unlisted

Click Add to Render Queue

Render All

