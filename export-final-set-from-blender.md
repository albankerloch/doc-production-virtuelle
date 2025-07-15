# Export final set from Blender

**Blender**

In a new collection : File ⇒ Import FBX

Add a view Camera : click on the upper rigth corner of the main view and drag in the middle of the view

In scene properties, select Camera3D1 as Camera

<figure><img src=".gitbook/assets/image.png" alt="" width="340"><figcaption></figcaption></figure>

Select the camera, in camera properties :

* Set the Focal length with the focal length value found in DVR

<figure><img src=".gitbook/assets/image (1).png" alt="" width="343"><figcaption></figcaption></figure>

* Set the Clip End at 99 m (won't desapear)
* Add a Background Image (Movie Clip ⇒ open the proxy created before)

<figure><img src=".gitbook/assets/image (2).png" alt="" width="326"><figcaption></figcaption></figure>

**Adapt the camera to the environement (trial and error)**

* Ctrl+ A : Add Empty ⇒ Plain Axe
* Select all elements imported + Empty
* Unselect Empty
* Reselect Empty
* Ctrl + P : Parent
* Scale Empty ⇒ S + Ctrl (scale)
* Move Empty⇒ G + Z (set at ground level)

**Export the EXR**

* Set View
* Set the format and folder of the output
* Render ⇒ Render Animation

