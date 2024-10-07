# CanalNETWORK 2.5 (Oct 2024)

**Hello and Welcome Again,**

We are thrilled and excited to bring to you yet another enhanced version of <strong> Version 2.5 of CanalNETWORK and DrainNETOWRK</strong>, including major updates.

In this release we provide updates for better user experience, and bug fixes found while testing previous releases. The DrainNET product resources are enhanced in a major way to accomodate key workflow requirements in design process.



Big Thankyou, <strong> EEC  </strong> for your trust, contributions and support.


<p style="color:green"> Happy Designing! </p>

<p style="color:blue">Team Quanomic.</p>


*Skip to read [What's New](#whats-new)*



## Update Resources

Update your version of CanalNETWORK product as follows:
1. Download the update resoruces from [Latest CanalNETWORK update resources](https://drive.google.com/uc?export=download&id=1Ov_tptZDHdrvIf7o1ogrlfpb_iWiBgvD)

    The latest is **Version 2.5.0.4581**

    Accompanied by **Version V4.9.3** of iCAD Bridge Application.


    > **Important Note:** Make sure AutoCAD is closed before you continue. If not, your update may not work, and require time to sort out. This release contains updates to the ***iCAD Bridge*** application.

2. Start your product, go to `Help > Updates...` Then choose `Manual` option. This will ask to close the application and re-start. Choose `Exit` to agree, and continue.

3. Upon restart, the launcher application will ask if you would like to download or manually update. Choose `Manually`. On the file explorer, point to your downloaded resource file. The rest will be handled by the launcher.



## What's New
[Back to ToC](#table-of-contents)

Key improvements are made for the period that cover a range of topics identified by our team, as well as user.

1. Default CBL_designSettings are set to 'first' to represent most common design requirements - i.e., mostly in fill condition - for drainage canal routs.

    <img src="./media/Image 001.png" style="width:7in">

1. A new drain canal algorithm implemented. Now, design can progress from upstream controls to downstream controls as needed, giving the user full control on bedlevel modification, invert level changes, and and canal hydraulics. It also automatically limits user inputs to currently set brach (feeder drain) conditions.

    <img src="./media/Image 002.png" style="width:7in">

1. Outfall height edit box is now a display ONLY box. Previous functionality to set invert levels is removed. In the new algorithm, outfall heights are not a design parameter.

    <img src="./media/Image 003.png" style="width:in">


1. Newly introduced **Invert release** function enhanced to work on different scenarios - multiple routes, single routes, or single control.

     <img src="./media/Image 004.png" style="width:6in">


1. Improved algorithm for identifying top level canal generation.

1. Canal Exception name now checks for duplicate naming, and alerts the user to review input.



## Bug Fixes

- Resolved selection handling when farm blocks are switched off.
- Bug fix on route exception setting

END.





