# Refine tracking in SynthEyes

**AutoShot : Generate SynthEyes Script**

Run Values section :

* Program = Others
* Camera Media = Extracted EXRs
* Clip In Frame = \<start frame>
* Clip Out Frame = \<end frame>
* AI Roto Model = INSPYRENET

Click on Save & Run

Click to the path "Syntheyes script exported to" on the console

Copy the path from the explorer

**SynthEyes tracking**

Open SynthEyes

Script ⇒ Run Script ⇒ paste the path ⇒ click on the script

Save as ⇒ save SynthEyes file (.sni)

Click Rotomask (bar bellow)

Shot ⇒ Edit Shot ⇒ set up ending frame (and starting frame if needed)

~~Click Auto (Green button)~~

**Syntheyes Feature Settings**

Click on Feature (tab in the upper part)

Click on Advanced (button on the left part)

Click on Auto Re-blip (to see the points)

Change Small bits size and Max bits size (12 / 24)

Click on Bits all frames (button on the left part)

Click on Peel All (button on the left part)

Get Medium Points :&#x20;

* Change  Small bits size and Max bits size (16 / 32)&#x20;
* repeat (Bits all frames + Peel All) = keeps the best points

Change Large Points :

* Small bits size and Max bits size (20 / 40)
* repeat (Bits all frames + Peel All)

**Creating Survey Data**

On Trackers tab, click on Toolbars / Mesh (up right table)

Click on "Show meshes" on the new Mesh table (up left)

Lasso select severals trackers on the ground (click on blank area and drag the lasso)

Click Track ⇒ Drop onto mesh (on ground area where there is mesh)

**Solve the tracking**

On Solve tab, click Go (Green button)

Disable bad trackers :&#x20;

* Maj + C
* Click on Bad Frames ⇒ Disable

Change Automatic to Refine (bellow Go button)

Click on Go again

Repeat with Maj + C ⇒ High-error Trackers (15.000)

Error must be < 1 HPIX

**Focal Length**

Check if the focal is ok between AutoShot and SynthEyes

<figure><img src="../.gitbook/assets/image (4).png" alt="" width="375"><figcaption></figcaption></figure>

If not, click on 24.900 x 14.006 mm to change manually the sensor size (depending on the camera)

**Lense Distortion**

Click Calc. Distortion

Click on more

In the pop-in, select Radial 4rth-order

Click on C2 and V2 to be set to Calculate

Close the pop-in and click on Go (Green Button) to refine

If the error is not raising, click on C4 and V4 to be set to Calculate and Go again

**Add Chisels**

Click on 8/10 stable trackers on the ground

Click on Script ⇒ Mesh ⇒ Duplicate Mesh onto Trackers

Put 5 as chisel size

**Render Preview (optionnal : to visualize check alignement)**

On the 3D tab, select the mesh

Click on Hide

Shot ⇒ Savec Sequence

Select a folder

Mesh included

Compression setting => 20 000

**Lens Worflow**

On solver tab, click on the Lense Worklow Button

Select Redistyorted (2)

Margin = 5

Maximum Rounding error = 1

**Export for Blender**

File ⇒ Export ⇒ Blender (Python)

Timeline setup = Entire Shot

Starting Frame = 1

Set Track to 5

Change the Blender executable with the Pick Executable in AutoShot

Blender will automatically open

