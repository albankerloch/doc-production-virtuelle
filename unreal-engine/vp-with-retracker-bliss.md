# VP with REtracker Bliss

**Project Setup :**

* Create a new project with the Virtual Production blank template
* File ⇒ Import into Level ⇒ fbx
* Open folder
* Create a Plugins Folder at the root level
* Add LiveLinkBliss Folder
* Edit ⇒ Plugins ⇒ Check if those are enabled:
  * LiveLinkBliss
  * Timed Data Monitor
  * Camera Calibration
* Edit ⇒ Project Setting ⇒ Engine ⇒ General Settings&#x20;
  * Frame Rate ⇒ Use Fix Frame Rate = 25
  * Timecode ⇒ 25 fps
* Restart



**Virtual Production Compositing :**

* Import the Aruco Tag into the scene
* Create a Media Player (and Media Texture automatically)
* Set the input source as USB Capture
* Crate a new VP composition (0010\_comp)
* Add 2 Layers : Media Plate & CGI
* Select the Media Plate and Composure ⇒ Input ⇒ Media Texture
* Select CGI elements ⇒ Layer window ⇒ Add Layer with Selected elements (Layer 1)
* Select the CGI plate and Composure ⇒ Input ⇒ Capture Actors ⇒ Actor Set ⇒ Layer1
* Select 0010\_comp and:
  * Output ⇒ + ⇒ Output pass = Player Viewport
  * Transform/Compositing Passes ⇒ + ⇒ Material ⇒ Material (New CompositingMaterial created)
* Open the new material CompositingMaterial&#x20;
  * Material ⇒ Material Domain ⇒ Post Process
  * Right click ⇒ TextureSampleParameter2D ⇒ Duplicate
  * Rename media\_plate\_1 and cg\_element\_1
  * Right click ⇒ over
  * Link media\_plate\_1 RGBA to over (A)
  * Link cg\_element\_1 RGBA to over (B)
  * Link over RGBA to Emissive Color
* Chroma keying :&#x20;
  * Select media\_plate\_1
  * Transform/Compositing Passes ⇒ Transform Passes ⇒ Chroma Keying ⇒ Key Colors ⇒ +
  * User Cross to choice the Green Color



**Virtual Subject Setup**

* Content browser ⇒ Right click ⇒ LiveLink ⇒ Blueprint Virtual Subject ⇒ role = LiveLink Camera Role&#x20;
* Name it VirtualFIZ and open it
* In Variables, add 3 float variables (Focus, Iris, Zoom) and click on the eye to be able to modify them
* In Event Graph, Right Click ⇒ Update Virtual Subject Static Data
* Link to Event On Initialize
* Right Click in Static Data ⇒ Split Structure Pin
* Check (and only that) :
  * Static Data is Aperture Supporter
  * Static Data is Focus Distance Supporter
  * Static Data is Focal Length Supporter
* In Event Graph, Right Click ⇒ Update Virtual Subject Frame Data
* Link to Event On Update
* Right Click in Static Data ⇒ Split Structure Pin
* Drag the variables on the Event Graph ⇒ Get {variable}
* Link the variables to the Update Virtual Subject Frame Data :
  * Zoom ⇒ Frame Data Focal Length
  * Iris ⇒ Frame Data Aperture
  * Focus ⇒ Frame Focus Distance
* Press Compile Button
* Set Default values for the variables (click on it ⇒ Details), ex :
  * Zoom = 24 (mm)
  * Iris = 22 (f22)
  * Focus = 1500 (cm = 1,5m)



**Track Camera with LiveLink**

* Launch the Bliss REtracker
* Windows ⇒ Virtual Production ⇒ LiveLink
* \+ Source ⇒ ,LiveLink Bliss Source => IP Address (127.0.0.0) + (Port 50000)
* Click on Bliss ⇒ Buffer - Settings :
  * Buffer Size = 200&#x20;
  * Offset = 0,145 s (to be confirmed)
* \+ Source ⇒ Virtual Subject ⇒ select VirtualFIZ&#x20;
* Presets ⇒ Save As Presets ⇒ Name it LiveLinkBliss Preset
* Gears ⇒ Plugins ⇒ LiveLink ⇒ Default LiveLink Preset ⇒ select it
* Select CineCameraActor ⇒ Details ⇒ Add ⇒ 2 LiveLinkComponentController :
  * LiveLinkComponentControllerFIZ
  * LiveLinkComponentControllerBliss
* Select LiveLinkComponentControllerFIZ ⇒ LiveLink ⇒ Subject Representation ⇒ Virtual
* Select LiveLinkComponentControllerBliss ⇒ LiveLink ⇒ Subject Representation ⇒ Camera1



**Calibration**

* Add objet to the scene ⇒ Virtual Production Production ⇒ Checkerboard
* Select Checkboard and change :
  * Num Corner Rows = 4
  * Num Corner Cols = 6
  * Odd Cube Materal = BlackUnlitMaterial
* Create a Lens file on the content browser ⇒ Right click ⇒ Misilanious ⇒ Lens File
* Select CineCameraActor ⇒ Details ⇒ Add ⇒ Lens
* Select Lens created ⇒ Lens File = Lens File created before
* Change Media Source to Media Texture and Select the Video Texture
* Type the Lens Model Name
* Type the Sensor dimensions (height / with \* 9 / 16)
* Type the same Sensor dimensions on the cine camera actor
* On the Lens File Panel, select Focus and click + twice :
  * input value : 10, Encoder mapping : 10
  * input value : 10000, Encoder mapping : 10000
* On the Lens File Panel, select Iris and click + twice :
  * input value : 3,2, Encoder mapping : 3,2
  * input value : 16, Encoder mapping : 16
* On the Calibration Steps, Lens Distortion panel :&#x20;
  * Calibration Pattern = Checkerboard
  * Calibrator = CameraCalibrationCheckerboard
  * Click in the image several times (15-20) to capture the real checkerboard in different position
  * Set guess focal lenght to your guess (ex : 28mm)
  * Click Calibrate Lens and OK
* Check Calibration on the Nodal Offset panel :&#x20;
  * Nodal Offset Algo = Nodal Offset Checkerboard
  * Checkerboard = CameraCalibrationCheckerboard
  * Click in the image&#x20;
  * Click on Apply to calibrator
* On the Lens File Panel, select Nodal Point and enter the nodal point offset calculated



**Worldpose**

* Copy the Aruco Tag folder in the Content Folder
* Check Calibration on the Nodal Offset panel :
  * Nodal Offset Algo = Nodal Offset Aruco Marker
  * Checkerboard = Aruco\_ID\_8\_15x15cm\_C\_1
  * Click in the image&#x20;
  * Click on Apply to Camera Parent



* Tracking delay



Lancer Live Link Hub :&#x20;

* Windows+R
* CMD
* "C:\Program Files\Epic Games\UE\_5.8\Engine\Binaries\Win64\LiveLinkHub.exe" -EnablePlugins="LiveLinkFreeD"
