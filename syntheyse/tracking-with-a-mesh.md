# Tracking with a Mesh

**Set up in SynthEyes**

_\[ALWAYS work with BRAW ⇒ compression or Noise reduction affect the data for tracking]_

* Open the Footage from the scene folder (Footage/Video Assist)
* Save the SynthEyes files to the scene folder (Post-Prod/SynthEyes)
* Solver room : click on 24 mm \* 15 mm
* Set the sensor factor to 1.5
* Set the sensor size to 35.9 mm ⇒ automatically 23.99
* If the shot is in anamorphic : set the pixel size to 1.6



**Roto Masking**

* To be masked : subject in movement or spot on the sensor :
  * Click on the magic wand
  * Click on the area to mask
  * Set up a simple form with the few points
  * Track this form over the shot
* To see the masks in the Summary room, click Roto on the bar bellow



**Trackers**

* Script ⇒ Multi-peel\_JETSET\_Style\_V8 (import it if needed)

{% file src="../.gitbook/assets/Multi-peel_JETSET_Style_V8.sia" %}

* Check visually for very bad trackers (spots on the sensor)
* Remove manually very bad trackers



**Solve**

* Click on Go! to launch the initial automatic solve (and wait)
* Wait (if too long, stop and remove bad trackers or modify the script to have less trackers)
* Remove very bad trackers (Shift + C ⇒ Bad Frames > 15 hpx Clear ⇒ Fix)
* Change Automatic to Refine
* Click on Go! again
* Check Calc. Distortion
* If the shot is anamorphic :
  * With the more button, choose "Std. Anamorphic Merged" for the first three values
  * Refine
  * If the solve did not decrease too much, calculate for :
    * all values in C's&#x20;
    * first, second, fourth and fifth values in O's
  * Refine
  * With the more button, choose "Std. Anamorphic"
  * Refine
  * If the solve decreased too much, reset the last values to 0 and set to Manual
* If the shot is not anamorphic :
  * With the more button, choose "4th Radial" and calculate for the first two values
  * Refine
  * If the solve did not decrease too much, calculate for the two more values
  * Refine
  * If the solve decreased too much, reset the last values to Manual
* Remove very bad trackers (Shift + C)
  * Bad Frames < 2 % = Disable
  * High Error Trackers < 5 000&#x20;
  * ⇒ Fix
* Refine



**Link the Mesh to the solved**

* File ⇒ Import ⇒ Mesh ⇒ select the KIRI .obj in the Asset/Blender/Structure folder
* On the 3D room, choose the Camera & Perpective view
* Select a tracker in the Camera view
* Select "Place" in the Perpective view
* Click on the Mesh where the tracker selected is supposed to be
* Repat that for 4 or 5 trackers
* On the Solve room, check the Constrain box and Refine the solve
* If needed, place more trackers & Refine&#x20;



**Refine the link with the Mesh**

*



**Export to Blender**

* Click on Lens Worflow ⇒ 2) Distorted
* File ⇒ Export ⇒ Blender
* Select the SynthEyes folder to save the Python file
* Run the Export with this options :&#x20;

<figure><img src="../.gitbook/assets/image (30).png" alt="" width="316"><figcaption></figcaption></figure>







