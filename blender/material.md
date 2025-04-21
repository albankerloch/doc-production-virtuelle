# Material

**Change color of an object**

* Select the object (on Object Mode or in Scene Collection)
* Material tab (Properties - bellow Scene Collection)
* New
* Base Color (Left Click)

**Add Image Texture (Manually)**

* Download jpeg on the web
* On  Blender :&#x20;
* Select Object
* Properties&#x20;
* Material tab
* New
* Click on the circle near Base Color
* Choose Image Texture

<figure><img src="../.gitbook/assets/image (10).png" alt="" width="375"><figcaption></figcaption></figure>

* Click Open
* Choose the Base Color Jpeg

**Add Rouhgness Texture (Manually) \[Shading Tab]**

* Shift + A (Add Effect) : Image Texture ⇒ Color
* Link to Principled BSDF (Roughness)
* Open ⇒ Choose Roughness Texture
* Color Space : Non-Color

**Add Normal Texture (Manually) \[Shading Tab] = Bump on surface facing up (normal)**

* Shift + A (Add Effect) : Image Texture ⇒ Color
* Link to Principled BSDF (Normal)
* Open ⇒ Choose Normal Texture
* Color Space : Non-Color
* Shift + A (Add Effect)
* Shift + A (Add Effect) : Normal Map
* Link between Image Texture and Principled BSDF (Normal)

**Texture Paint  \[Texture Paint Tab]**

* Create Image Texture on Material Tab (with appropriate color)
* Isolate the view on the object (/)
* Set Mode to Material View (no shades)
* Open texture to paint on left side
* Change Paint to approriate color (and strengh)
* Paint on either side (UV unwrapping or Viewport)
