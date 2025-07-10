# Camera tracking in DVR

**Media Mode**

Add the footage to the Media Pool

Create a timeline with the footage

~~**Cut Mode**~~

~~Cut the footage in the Cut Mode~~

**Fusion Mode**

Position the start and the end of the scene

<figure><img src=".gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

Add Tool ⇒ Tracking ⇒ Camera Tracking

If needed add a mask before

Tick Preview AutoTrack Locations and Bidirectional Tracking

Decrease Detection Threshold, Min Feature Separation to get more AutoTrack Locations

Click on Auto Track

Go to Solve Tab, click Solve

Delete AutoTrack Locations if Average < 1 pixel (Apply Track Selection Filters ⇒ Operations on Selected Tracks ⇒ Delete)

Go to Export tab, click on Unaligned

Select AutoTrack Locations on the floor ⇒ Orientation : Set From Selection

Select AutoTrack Locations at the origin ⇒ Origin : Set From Selection

Click on Export



