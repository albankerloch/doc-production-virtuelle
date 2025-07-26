# Import shots in AutoShot

**Windows**

* With the Lightcraft Jetset app opended on IPhone, click on Sync in Autoshot :

![](<../.gitbook/assets/image (15).png>)

* On the Run Values section, choose Blender and click on Pick Executable and select the exe in :
  * C:\Program Files (x86)\Steam\steamapps\common\Blender (if installed with Steam)
  * or C:\Program Files (x86)\Blender Foundation\Blender 4.1
* Next to Scene Blend file, click on Set and select the blender project on the Assets folder
* Choose the options needed :&#x20;
  * Generated Blend File :&#x20;
    * Empty Comp Start
    * Append Scene (copy orginal project)
    * Linked Scene (if lot of scenes : for production)
  * Camera Media :&#x20;
    * Original File
    * PNG
    * EXR
  * Clip In Frame / Clip Out Frame (open shot in DVR to check frames needed)
  * AI Roto Model (INSPYRENET slow but better to isolate persons)
  * Import Set LiDAR (if a scan was done)
  * Set Depth (plane to camera)
* Click on Save & Run (it'll open Blender)

