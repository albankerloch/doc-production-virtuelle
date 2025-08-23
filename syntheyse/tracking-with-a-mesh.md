# Tracking with a Mesh

**Set up in SynthEyes**

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
* Check visually for very bad trackers (points on the sensor)
* Remove manually very bad trackers



**Solve**

* Click on Go! to launch the initial automatic solve (and wait)
* Wait (if too long, stop and remove bad trackers)
* Remove bad trackers (Shift + C)
* Change Automatic to Refine
* Click on Go! again
* Check Calc. Distortion
* If the shot is anamorphic :
  * With the more button, choose std for the two first values
* If the shot is not anamorphic :
  * With the more button, choose 4th radiatic and calculate for the two first values
  * Refine
  * If the solve did not decrease too much, calculate for the two more values
  * Refine
  * If the solve did decrease too much, reset the last values to Automatic
* Click on Lens Worflow ⇒ 2) Distorted



**Link the Mesh to the solved**



