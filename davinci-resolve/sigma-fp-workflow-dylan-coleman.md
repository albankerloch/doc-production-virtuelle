# Sigma FP Workflow : Dylan Coleman

**Settings / Exposure :**

Camera Raw  (as Clip if note already changed in Project Settings  / Camera RAW  / CinemaDNG) :&#x20;

* Color Space : BlackMagic Design
* Gamma : BlackMagic Design Film
* Check Highligth Recovery

⇒ Raise the exposure (shot underexposed)

⇒ Bring down the hightlights



**Dylan Coleman 6 nodes :**

**Node 1 : CST**&#x20;

* Input Color Space : BlackMagic Design Film Gen 4
* Input Gamma : BlackMagic Design Film
* Output Color Space : ARRI Wide Gamut 3
* Output Gamma : ARRI LogC3

**Node 2 : HDRI Wheels**&#x20;

HDRI Wheels  ⇒ ... (right corner) => Match Color Space & Gamma

**Node 3 : Vignette**

Add Window Circle in the subject face

Add Gamma

Reduce Mid/Detail to soften skin

**Node 4 : Outside Vignette**

Select Outsite of Vignette (Acl + Click or Alt + Drag or Option + O)

Lowering Gain

**Node 5 : Glow Effect**

Select Output = Skiny Regions

Lowering Shine Threshold

Select Output = Glowing Image

Composite Type = SoftLight

Add Gain

Lowering Global Blender

Add Mid/Detail&#x20;

**Node 6 : LUT**

* ARRI ⇒ ARRI Alexa to Rec709



**Dylan Coleman 7 nodes :**

**Node 1 : Primaries**

**Node 2 : White Balance**

Offset Wheel with Vectorscope

&#x20;**Node 3 : Tone**

Custom Curve with Waveform

&#x20;**Node 4 : Glow**

&#x20;**Node 5 : Vignette**

Correct Exposure and L. S. (Low Shadow) if needed

&#x20;**Node 6 : Sharpening**

**Node 7 :**&#x20;

* Input Color Space : BlackMagic Design Film Gen 4
* Input Gamma : BlackMagic Design Film
* Output Color Space : Rec.709
* Output Gamma : Gamma 2.4





