# CanalNETWORK 2.5 (Jul-Aug 2024)

**Hello and Welcome Again,**

We are thrilled and excited to bring to you yet another enhanced version of <strong> Version 2.5 of CanalNETWORK and DrainNETOWRK</strong>, including major updates.

In this release we provide updates for better user experience, and bug fixes found while testing previous releases.



Big Thankyou, <strong> EEC  </strong> for your trust, contributions and support.


<p style="color:green"> Happy Designing! </p>

<p style="color:blue">Team Quanomic.</p>


*Skip to read [What's New](#whats-new)*



## Update Resources

Update your version of CanalNETWORK product as follows:
1. Download the update resoruces from [Latest CanalNETWORK update resources](https://drive.google.com/uc?export=download&id=1Ov_tptZDHdrvIf7o1ogrlfpb_iWiBgvD)

    The latest is **Version 2.5.0.4461**

    Accompanied by **Version V4.9.0** of iCAD Bridge Application.


    > **Important Note:** Make sure AutoCAD is closed before you continue. If not, your update may not work, and require time to sort out. This release contains updates to the ***iCAD Bridge*** application.

2. Start your product, go to `Help > Updates...` Then choose `Manual` option. This will ask to close the application and re-start. Choose `Exit` to agree, and continue.

3. Upon restart, the launcher application will ask if you would like to download or manually update. Choose `Manually`. On the file explorer, point to your downloaded resource file. The rest will be handled by the launcher.



## What's New
[Back to ToC](#table-of-contents)

Key improvements are made for the period that cover a range of topics identified by our team, as well as user.

1. Special algorithm included to allow generation of LSec profile drawing for canals of exceptionall short lengths. The algorithm interpolates finer resolution data from existing points to create the drawing.
 
    <img src="./media/Image 088.png" style="width:2in">

1. Resolved issue when attempting to overaly profile data from Windows Clipboard.

    <img src="./media/Image 089.png">

1. Tractive force method of canal section design is included. This major enhancement allows users to investigate canal stability after design, as well as determine stable sections, using the widely accepted method of design.

    <img src="./media/Image 2.png" style="width:6in">

    A detail is included in documentation on the chapter [About Design Criteria]()
  

2. Additional relationship is included for B/D ratio determination for lined canals using B/D= 0.03 Q + 1. This relationship determines better suited canal shapes for lined canals.

     <img src="./media/Image 10.png" style="width:4in">

    The option is automatically enabled for all lining types, except no lining.

2. Similar to above, free board provissions for lined canals are now provided based on FB= 0.4*Q^0.25, regardless of settings for FB values. However, values can not be lower than 0.10m;


2. Improvements to the CanalSection Design interface to use tractive force methods of design, as well as improved display that shows lining material.

    <img src="./media/Image 11.png" style="width:6in">

2. Floating node functions are enhanced better for better user interaction, removing unwanted behavior requesting to remove route. Better visualization is also included in plan view, and verified function to exclude BoQ in case of special segments.

    <img src= "./media/Image 085.png" style="width:7in">
    
2. Additional menu is included for easy creation of side-roads only in cut conditions (As part of the new design criteria).

    <img src= "./media/Image 086.png" style="width:7in">
    
    *Figure showing berms in fill conditions applied always.*

    <img src= "./media/Image 087.png" style="width:7in">

    *Figure showing berms applied only in cut conditions*

2. Better data tip displays maintaining uniformity across plan view, profile view, and detail view axes.

    <img src="./media/Image 083.png" style="width:6in">

2. Included `Refresh Routes` menu for plan view axis. This allows to clear all objects, and recreate only route information in the view. Nodes are now recreated when using the `Show Nodes` context menu.

    <img src="./media/Image 079.png" style="width:6in">


2. The Canal section design interface is updated to ensure designed values from solver are retained on completion. Previously, some solver solutions were volatile (that means were not persistent after closing the interface).

    <img src="./media/Image 080.png" style="width:6in">

1. A new menu tool is included to allow loading and viewing of data hosted on AutoCAD objects eaily. Previously, this task was only possible with iCAD software.

   <img src="./media/Image 0.png" style="width:6in">

The DrainNET product is also improved for the following:
- Corrected display station in cross-section view

    <img src="./media/Image 082.png" style="width:7in">

- Automatic view update upon changes in preference settings.

    <img src="./media/Image 081.png" style="width:6in">



### Bug Fixes
- Cross-section generation following updates for Interceptor ditch provision
- Farm block processing from AutoCAD
- Network resize function 
- Display of invert levels on LSec drawings

END.





