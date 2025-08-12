# Color Management for Blender

**DaVinci Resolve : Settings**

Project Setting ⇒ Image scaling : bilinear or bicubic (for EXR)

Color Science = Davinci YRGB (⇒ managed by CST nodes)

Timeline Color Space = Rec.709 Gamma 2.4

**CST Node to mimic Filmic**

CST node in Color tab with&#x20;

* Color Space Transform :
  * Input Color Space : Rec.709
  * Input Gamma : Linear
  * Output Color Space :  Rec.709
  * Output Gamma : sRGB
* Tone Mapping Method : DaVinci
  * Max Nits = 10000 (secure)
* Advanced :
  * Uncheck Apply Forward OOTF and Apply inverse OOTF

**CST Node to mimic Agx**

CST node in Color tab with&#x20;

* Color Space Transform :
  * Input Color Space : Rec.709
  * Input Gamma : Linear
  * Output Color Space :  Rec.709
  * Output Gamma : Gamma 2.4
* Tone Mapping Method : DaVinci
  * Max Nits = 10000 (secure)
* Gammut Mapping : None (or Saturation Compression if a lot of Saturation)
* Advanced :
  * Check Apply Forward OOTF
