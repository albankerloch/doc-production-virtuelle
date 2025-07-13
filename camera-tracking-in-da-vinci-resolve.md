# Camera tracking in DVR

**Media Mode**

Add the footage to the Media Pool

Create a timeline with the footage

~~**Cut Mode**~~

~~Cut the footage in the Cut Mode~~

**Fusion Mode : create 3D space**

Position the start and the end of the scene

<figure><img src=".gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

Add Tool ⇒ Tracking ⇒ Camera Tracker

If needed add a mask before

Tick Preview AutoTrack Locations and Bidirectional Tracking

Decrease Detection Threshold, Min Feature Separation to get more AutoTrack Locations

Click on Auto Track

Go to Solve Tab, click Solve

Delete AutoTrack Locations if Average < 1 pixel (Apply Track Selection Filters ⇒ Operations on Selected Tracks ⇒ Delete)

Go to Export tab, click on Unaligned

Select AutoTrack Locations on the floor ⇒ Orientation : Set From Selection

Select AutoTrack Locations at the origin ⇒ Origin : Set From Selection

If needed, set Z Rotation manually to 0

Click on Export

Merge3D ⇒ view on Left ⇒ Right Click ⇒ Camera ⇒ Camera3D

**Fusion Mode : add a shape**

<figure><img src=".gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Drag the 3D shape to the nodes part

Link the shape with the Merge3D

Adjust the type and size of the shape

Adjust the placement of the shape

**Fusion Mode : export in FBX**

Add Tool ⇒ Tracking ⇒ Camera Tracker

Save the file in a folder

Disconnect CameraTracker to MediaOut

Fusion ⇒ Render all savers

If needed restart DVR



