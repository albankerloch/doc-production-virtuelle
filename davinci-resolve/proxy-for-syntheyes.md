# Proxy for SynthEyes

**Edit**

With the scene timeline, cut the scene (remove uncessesary begining and ending)

Set Source Frame at the top right of the footage instead of the Source Timecode :

<figure><img src="../.gitbook/assets/image (26).png" alt="" width="279"><figcaption></figcaption></figure>

Just in case note the start frame and the end frame&#x20;



**Color**

In the Camera Raw tab, choose :

* Decode Using : Clip
* Color Space : Blackmagic Design
* Gamma : Blackmagic Design Film

Set the Expore (check with the Waveform)

Add 2 Nodes :

* Noise Reduction :
  * Temporal Threshold : 15 (Luma & Chroma)
  * Spatial Threshold : 15 (Luma & Chroma)
* CST :
  * Input Color Space : BlackMagic Design Film Gen 1
  * Input Gamma : BlackMagic Design Film
  * Output Color Space : Rec.709
  * Output Gamma : Rec.709
  * Tone Mapping : DaVinci



**Deliver**

Set the name as the Timeline name

Chose the H.265 Export

Change the location to the scene folder (Footage/Proxy)

Add to Render Queue

Render All
