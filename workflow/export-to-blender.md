# Export to Blender

**AutoShot**

* In the "Take Selection" section, select the Day and the intended Take
* With "File" ⇒ "Shots" ⇒ "Add Shot", name a new shot (ex : SHOT001)
* In the "Run Values" section, select :&#x20;
  * Program : Blender
  * Use SceneLoc : used origin location while shooting
  * Generated Blend File : Empty Comp Start
  * Camera Media : Extracted EXRs (used in GeoTracker)
  * Clip in Frame : start frame of the sequence (noted in DVR)
  * Clip out Frame : end frame of the sequence (noted in DVR)
  * AI Roto Model : INSPYRENET (better human extraction but slow)
  * Add Camera Plan : unchecked (or suppress after in Blender)

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>
