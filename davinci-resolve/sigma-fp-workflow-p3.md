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

**Node 4 : CST**&#x20;

* Input Color Space : DaVinci Wide Gamut
* Input Gamma :DaVinci Intermediate
* Output Color Space : Rec709
* Output Gamma : Gamma 2.4





