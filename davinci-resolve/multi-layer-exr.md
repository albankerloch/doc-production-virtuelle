# Multi-Layer EXR

**Blender**

Light Layer ⇒ one collection per light

Export one Animation per Ligth (long)



**DaVinci Resolve**

Stack the layer in the Edit tab

Change in the Video tab : Composite ⇒ Composite Mode : Add

Add Effect : Adjustement Clip ⇒ Apply Color Grading / CST to all EXR down

Possiblilty : flicker one ligth only, or glow

Possibility : samples count different depending on light (with lot of noise)

Possibility : Super Scale ⇒ 2x or 2x Enhanced

Possibility : Frame step = 2 to speed up Rendering (but need to rename)

⇒ Video Properties ⇒ Redtime and Scaling ⇒

* Retime Process = Optical Flow
* Motion Estimation = Speed Warp Faster



**Denoise per layer**

In Color, add a node with a node layer ⇒ Noise Reduction

* Temporal Threshold ⇒ Luma Threshold & Chroma Threshold = 100
* Spatial NR : Mode = UltraNR

⇒ Analyze ⇒ change Luma & Chroma

Add another Denoiser nodes if needed !

Better than Denoiser in Blender (flickering)

Use Motion Blur to mask Noise



**Performance issue in the viewport**

Select all EXR channels + Adjustment layer

Right Click =>New Compound Clip

Right Click ⇒ Render in Place ... (pre-render)

If need to change Right Click ⇒ Open in Timeline





