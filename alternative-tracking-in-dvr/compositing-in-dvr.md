# Compositing in DVR

**Fusion : Import from Blender**

Open the folder of all EXR

Select all

Drag and drop in DVR fusion ⇒ create a node

**Fusion : Add a Gamut node**

&#x20;Right click ⇒ Add Tool ⇒ Color ⇒ Gamut

Select sRGB as Output Space

Check Pre-Divide / Post-Multiply

**Fusion : Add Merge Node**

Apply Mode Normal, Operator Over, Additive 1.0

Link MediaIn1 and MediaIn2 to Merge node

Link Merge node to MediaOut

**Deliver : Export**

Select type (H.24 Master / Youtube, etc)

Change File Name

Click Add to Render Queue

Render All

