# Tracking with a Mesh

**Set up in SynthEyes**

_\[Never work with BRAW ⇒ impossible to export to Blender]_

* Open the Proxy exported from DaVinci Resolve in the scene folder (Footage / Proxy)
* Save the SynthEyes files to the scene folder (Post-Prod / SynthEyes)
* Solver room : click on 24 mm \* 15 mm
* Set the sensor size to 35.9 mm
* If the shot is in anamorphic : set the pixel size to 1.6



**Roto Masking**

* Click on the magic wand
* Click on the area to mask
* Set up a simple form with the few points
* Track this form over the shot
* To see the mask in the Summary room, click Roto on the bar bellow



**Trackers**

* Script ⇒ \*Multi Peel JETSET (import it if needed)

{% file src="../.gitbook/assets/Multi-peel_JETSET_Style.sia" %}

* Check visually for very bad trackers (points on the sensor)
* Remove manually very bad trackers



**Solve**

* Click on Go! to launch the initial automatic solve (and wait)
* Wait (if too long, stop and remove bad trackers)
* Remove very bad trackers (Shift + C ⇒ Bad Frames > 15 hpx Clear ⇒ Fix)
* Change Automatic to Refine
* Click on Go! again
* Check Calc. Distortion
* If the shot is anamorphic :
  * With the more button, choose "Std. Anamorphic" for the first three values
  * Refine
  * If the solve did not decrease too much, calculate for :
    * all values in C's&#x20;
    * first, second, fourth and fifth values in O's
  * Refine
  * If the solve did decrease too much, reset the last values to 0 and set to Manual
* If the shot is not anamorphic :
  * With the more button, choose "4th Radial" and calculate for the first two values
  * Refine
  * If the solve did not decrease too much, calculate for the two more values
  * If the solve did decrease too much, reset the last values to Automatic
  * Refine
  * If the solve did decrease too much, reset the last values to Automatic
* Remove very bad trackers (Shift + C ⇒ Bad Frames = Disable + High Error Trackers < 5 000 ⇒ Fix)
* Change Automatic to Refine
* Click on Go! again



**Link the Mesh to the solved**

* Hit T to open the Texture Menu and Set File with the texture from Polycam
* On the 3D room, choose the Camera & Perpective view
* Select a tracker in the Camera view
* Select "Place" in the Perpective view
* Click on the Mesh where the tracker selected is supposed to be
* Repat that for 4 or 5 trackers
* On the Solve room, Refine the solve
* Place more trackers
* On the Solve room, check the Constrain box
* Refine the solve
* Click on Lens Worflow ⇒ 2) Distorted



**Export to Blender**

File ⇒ Export ⇒ Blender

Select the SynthEyes folder to save the Python file

Run the Export with this options :&#x20;

<figure><img src="../.gitbook/assets/image (30).png" alt="" width="316"><figcaption></figcaption></figure>







