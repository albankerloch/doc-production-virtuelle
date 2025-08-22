# Compositing in Nuke

**SynthEyes Export for Nuke**

File ⇒ Export ⇒ Nuke (current)

Choose file destination (default ok)

Timelline setup = Match frames

Starting Frame = 1001

Maya Oversan % 5

Check Export to clipboard ? ⇒ Yes

**Nuke**

Create a new project

Open the Node Graph tab

Paste the nodes exported in the clipboard (setup undistortion and redistortion nodes)

Move the nodes to the left

Save the project (in sequence/.../nuke for ex)

**Run AutoShot Script**

File ⇒ Run Script ⇒ find python script in sequence/.../nuke

New nodes appear

**Check Alignment (with chisels)**

R : add Reader node

Add Blender render (with chisels)

Click on the new node (highlighted)

Click on tab ⇒ search for Shuffle (channel)

Double click on the new node

Change the input layer from rgba to ViewLayder\_Combined

Click tab to add a Grade Node

Add more Gain and multiply to show more light

Click tab to add Reformat Node

Change the output format to Syn83894x2190 (as Cam1Merge1 on the left part of SynthEyes nodes)

**Optionnal Check**

Click M to Add a Merge (over) node

Set A to Cam1Render (chisels) and B to Reformat ⇒ click 1 on the merge node to display the result

Click D to see that the rendered chisels are on the right place :)

**Final Compositing**

Redirect the Reformat Node to the Cam1RePresize Node

Copy and paste the Cam1Reade1 node

Direct the new Cam1Reader1 node to the Cam1Merge (over)

<figure><img src="../../.gitbook/assets/image (27).png" alt="" width="495"><figcaption></figcaption></figure>

Select the Cam1Merge (over)

Render ⇒ FlipBook Selected ⇒ OK

Space to see Full Frame to check if the tracking is correct

**Render**

Redirect the Write1 node (from the script) to the Cam1Merge output

Change the file type to exr

Change the compression to DWWA

(the output directory is already set up)

<figure><img src="../../.gitbook/assets/image (28).png" alt="" width="249"><figcaption></figcaption></figure>

Select the Write1 node

Render ⇒ Render Selected Write Nodes ... ⇒ OK

