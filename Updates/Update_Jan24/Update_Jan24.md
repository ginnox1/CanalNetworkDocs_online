# CanalNETWORK 2.0

**Hello and Welcome Again,**

We are thrilled and excited to bring to you enhanced version of CanalNETWORK 2.0 with new and powerful features. These additions are requested by users in the currently completed trainings and proejcts.

This page briefly describes the latest release features and capabilities for the **January 2024** release. As always, so excited to bring to you these features and functionalities to the products.


Read on to learn about the new features, and 



<p style="color:green"> Happy Designing! </p>

<p style="color:blue">Team Quanomic.</p>


Navigate this page using the links below.

<!--TOC-->
  - [Update Resources](#update-resources)
  - [What's New](#whats-new)
    - [iCAD Data Table View](#icad-data-table-view)
    - [Data Table View](#data-table-view)
    - [Improved Data validation](#improved-data-validation)
    - [Production](#production)
    - [Network Configuration](#network-configuration)
    - [Bug Fixes:](#bug-fixes)
<!--/TOC-->


## Update Resources

Update your version of CanalNETWORK product as follows:
1. Download the update resoruces from [Latest CanalNETWORK update resources](https://drive.google.com/uc?export=download&id=1Ov_tptZDHdrvIf7o1ogrlfpb_iWiBgvD)

    The latest is **Version 2.08.3649**

    Accompanied by **Version V4.8.12** of iCAD Bridge Application.

    <img src="./media/Image 16.png">

2. Start your product, go to `Help > Updates...` Then choose `Manual` option. This will ask to close the application and re-start. Choose `Exit` to agree, and continue.

3. Upon restart, the launcher application will ask if you would like to download or manually update. Choose `Manually`. On the file explorer, point to your downloaded resource file. The rest will be handled by the launcher.


Download the update resources to make your installation uptodate from the linke below.


## What's New
Updated capabilities for this release are documented below.

> :warning: **Important Note:** If your current ***iCAD Bridge Application*** is linked to iCAD application folder, and iCAD is not updated, make sure to relink AutoCAD environment to the *iCAD Bridge.dvb* in CanalNETWORK application folder.


### iCAD Data Table View
Data on AutoCAD objects can now be accessed directly, avoiding the need to start iCAD for similar use cases. The title bar shows the details of the host object.

### Data Table View
The `Copy Table` button now throws the selection dialog with most commonly used settings for Include Columne Names, and All columns.

<img src="./media/Image 11.png" style="width:6in">


### Improved Data validation
Handlers for the following variables are improved to enhance data input validation, and reduce malfunctions.

1. Construction Variables - Earth Cut and fill shapes specification now takes strict triplets. Similarly, canal top provisions now strictly monitor data input for allowed number of inputs only, i.e., 1, 2, 4 or 5 only.

1. Exception names are further tested for validity and assist the uset to get them right always.

### Production
The following improvements are made to production drawings.

1. Sorting batch generated drawings in natural order (by name and by station). This include:
    1. Flow Section drawings
    2. LSec drawings for multiple routes

1. Drop ID (name) presentation in **explore tables** and **LSec drawings** is changed for entire route, instead of previous for each segment.

    <img src="./media/Image 12.png" style="width:8in">

1. Lsec  production is now greately enhanced to fit drawings to provided bounding box, reducing inconsistencies across drawings and the need for extensive editing.  Note, depending on the position of the initial bounding box coordinates, the actual bounding box may be slighly adjusted.
1. New tool launched that generates drawing generation templates (bounding boxes) for LSec and Plan views. Currently A3 paper size is available. Future releases will include other commonly used paper sizes.

    <img src="./media/Image 13.png" style="width=6in">

### Network Configuration
The following tools are enhanced for better network definition and processing.

1. Multi select capability
    Users can now selecet multiple routes in AutoCAD to import to CanalNETWORK environment.
    
    <img src="./media/Image 14.png" style="width:7in">

2. Enhanced Reverse Route 
    Reverse route tool now handles multiple tasks. In addition to reversing the parent object in AutoCAD, it does the following:

    <img src="./media/Image 15.png" style="width:5in">

    Refer to documentation on [Layout Plans and Network Resolution]() section for details.

    > Note: Routes reversed using the above tool will require the pipe workflow to be carried out, i.e, Node ID, Naming, Sizing (if needed with Farmblocks), Profile Extraction, and Soft-reloading.


### Bug Fixes:

- Issue of Batch drawing generation for flow sections using multiple routes is fixed.





