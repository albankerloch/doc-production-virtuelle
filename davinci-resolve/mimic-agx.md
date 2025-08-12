# Mimic AgX

**AgX**

Try to recreate the reaction of Film to light :

* Desaturate the highlights (Chromaticity Attenuation Rate)
* Keep image vibrant at lower levels

**Fusion : OCIO (Open Color Input Output)**

In Fusion, add a node with the effect OCIOColorSpace

* Select the the OCIO Config file (confi.ocio)
* Source Space: Linear Rec709
* Output Space : AgX Base sRGB

If needed, add a ColorGain node before to change Gain / Lift / Gamme

PB : impossible to access the Color panel

**Color : DCTL**

In Color, add a node with the effect DCTL&#x20;

Download .h and .dctl from Github ([link](https://github.com/sobotka/AgX-Resolve))

Click on LUT and then right-click ⇒ Open File Location

Create a folder and put the .h and .dctl in it















