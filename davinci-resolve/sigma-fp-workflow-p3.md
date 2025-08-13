# Sigma FP Workflow (P3)

**Settings / Exposure :**

Camera Raw  (as Clip if note already changed in Project Settings  / Camera RAW  / CinemaDNG) :&#x20;

* Color Space : P3 D60
* Gamma : Linear
* Check Highligth Recovery

⇒ Raise the exposure (shot underexposed)

⇒ Bring down the hightlights



**Clever Ghost nodes :**

**Node 1 : CST**&#x20;

* Input Color Space : P3 D60
* Input Gamma : Linear
* Output Color Space : DaVinci Wide Gamut
* Output Gamma : DaVinci Intermediate

**Node 2 : Skin Tone**

With the Vectorscope open :

* Mask the face of the subject
* Set the Color Temp as expected (sunligth, inside, etc)
* Adjust the Tint for the skin to be close to the skin tone line

**Node N - 1 : CST**&#x20;

* Input Color Space : DaVinci Wide Gamut
* Input Gamma :DaVinci Intermediate
* Output Color Space : Rec709
* Output Gamma : Cineon Film Log

**Node N : LUT**

* Film Look ⇒ Rec709 Kodak 2383 D55



**Ole 5 nodes :**

**Node 1 : CST**&#x20;

* Input Color Space : P3 D60
* Input Gamma : Linear
* Output Color Space : Panasonic V-Gamut
* Output Gamma : Panasonic V-Log
* Tone Mapping : None

**Node 2 : LUT**

Sigma ⇒ SIGMA fp Rec.709 (I) ISO 800

**Node 3 : Contrast**

Primaries - Color Wheel

See the hightlight ok at 90 (example with pipette)

Set Pivot to 0.90

Adjust the contrast (to do after all nodes)

**Node 4 : CST**

* Input Color Space : Rec709
* Input Gamma : Rec709
* Output Color Space : Rec709
* Output Gamma : Cineon Film Log
* Tone Mapping : DaVinci

**Node 5 : LUT FPE (Film Emulation)**

Film Looks ⇒ Rec709 Kodak 2383 D60



