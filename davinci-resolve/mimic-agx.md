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



**Color : Install the DCTL**

Download .h and .dctl from Github ([link](https://github.com/sobotka/AgX-Resolve))

Click on LUT and then right-click ⇒ Open File Location

Create a folder and put the .h and .dctl in it

**Color :** Camera-AgX DCTL

Add a node CST node with&#x20;

* Color Space Transform :
  * Input Color Space :  Rec.709
  * Input Gamma : Linear
  * Output Color Space :  ARRI Wide Gamut 3
  * Output Gamma :  Arri LogC3
* Tone Mapping Method : None

In Color, add a node with the effect DCTL  with DCTL List : Camera-AgX

Add Corrected Nodes in between (Gain Lift Gamma)

Add Exposure Nodes beofre CST (Gain) ⇒ Needed if Working Log Encoding = DaVinci Intermediate

Try Canon Log 3



**Color : Jp-AgxDRT DCTL**

Idem ([link](https://github.com/JuanPabloZambrano/DCTL)) with CST parameters :

* Output Color Space : Sony S-Gamut3.Cine
* Output Gamma : Sony S-Log3

DCTL parameters : Flourish / Contrast

Try  JP\_2499\_DRT (vivid colors)



**LUT (Look Up's Table)**

Download the LUTs from [link](https://gumroad.com/d/9eb5bca9bb21e967f4f3c368cd3d4e8a)

Copy Paste cube files in a folder in the LUT Folder

Click Update Lists after

Drag the LUT on a node



















