# Color Grading Workflow

**Color Culture**

**Color Space** : _which_ colors are available (sRGB, Rec709, P3, Davinci, ACES)

**Gamma** : defines how those colors transition in brightness (Linear,  sRGB, Gamma 2.2  for PC / Mobile screen, Gamma 2.4 for cinema)

**Linear Gamma** (Gamma 1.0) : doubling the pixel value would quadruple the brightness (since light intensity is proportional to the square of voltage in CRTs)

**Gamma correction** : ensures that a pixel value of 128 is about halfway between black and white in _perceived_ brightness, not in physical light output

**Contrast** affects the difference between light and dark areas.

**Gamma** affects midtone brightness

⇒ sRGB transform hardly whitout clipping or brown out (⇒ DRT/ Tone Mapping necessary)



**First Node : Color**

Applied on the EXR directly in Rec.790 (so not everything work in DVR, ex : color wheel)

⇒ Only use the Gain wheel in Primary Color



**Second Node : CST for LOG Exposure**

Convert EXR into LOG

CST node in Color tab with&#x20;

* Color Space Transform :
  * Input Color Space : Rec.709
  * Input Gamma : Linear
  * Output Color Space :  DaVinci Wide Gamut (or ARRI Wide Gamut 3)
  * Output Gamma : DaVinci Intermediate (or ARRI LogC3)
* Tone Mapping Method : None



**Color Correction Nodes**

Use the Color Wheels Panel :

* Lift : dark tones
* Gamma : midtones
* Gain : highlight tones
* Offset : all tones (?)

Then change :&#x20;

* Temps
* Tint (Green to Magenda)
* Contrast (alternative to Left / Gamma / Gain)
* Color Boost (prioritize neutral colors)
* Saturation (prioritize already saturated colors)

If necessary :&#x20;

* Node Hue : Hue Vs Hue ⇒ Change Red to Purple
* Node Saturation : Hue Vs Sat ⇒ Change Colors more precisely
* Node Lum : Lum Vs Sat : change saturation of brighter or darker tones only
* Node RGB : Curves Custom ⇒ Affect R G B channels more precisely with a curve (Y : Luminance)



**Last Node : CST**

CST node in Color tab with&#x20;

* Color Space Transform :
  * Input Color Space :  DaVinci Wide Gamut (or ARRI Wide Gamut 3)
  * Input Gamma : DaVinci Intermediate (or ARRI LogC3)
  * Output Color Space :  Rec.709
  * Output Gamma :  Gamma 2.2
* Tone Mapping Method : DaVinci
  * Max Nits = 10000 (secure)
* Gamut Mapping : Saturation Compression (avoid Saturated colors to escape the color space)
* Advanced :
  * Check : Apply Forward OOTF (Opto-Optical Transfer Functions ⇒ to Electronic Device)
