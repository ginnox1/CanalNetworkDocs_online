# CanalNETWORK 2.2 (May 2024)

**Hello and Welcome Again,**

We are thrilled and excited to bring to you yet another enhanced version of <strong> Version 2.2 of CanalNETWORK and DrainNETOWRK</strong>, including major updates.

In this **May 2024** update, we have included the design of **Head and Cross Regulator structures**. We have also included important enhancements to the software including DrainNET product.

   
<img src="./media/Image 073.png" style="width:7in"><br>


Big Thankyou, <strong> EEC  </strong> for your trust, contributions and support.


<p style="color:green"> Happy Designing! </p>

<p style="color:blue">Team Quanomic.</p>


*Skip to read [What's New](#whats-new)*



## Update Resources

Update your version of CanalNETWORK product as follows:
1. Download the update resoruces from [Latest CanalNETWORK update resources](https://drive.google.com/uc?export=download&id=1Ov_tptZDHdrvIf7o1ogrlfpb_iWiBgvD)

    The latest is **Version 2.2.1.4037**

    Accompanied by **Version V4.8.12** of iCAD Bridge Application.


    > **Important Note:** Make sure AutoCAD is closed before you continue. If not, your update may not work, and require time to sort out. This release contains updates to the ***iCAD Bridge*** application.

2. Start your product, go to `Help > Updates...` Then choose `Manual` option. This will ask to close the application and re-start. Choose `Exit` to agree, and continue.

3. Upon restart, the launcher application will ask if you would like to download or manually update. Choose `Manually`. On the file explorer, point to your downloaded resource file. The rest will be handled by the launcher.


## Table of Contents

<!--TOC-->
  - [What's New](#whats-new)
    - [CanalNETWORK Enhancements](#canalnetwork-enhancements)
    - [Drain Network Enhancements](#drain-network-enhancements)
<!--/TOC-->


## What's New
Updated capabilities for this release are documented below.

### CanalNETWORK Enhancements
[Back to ToC](#table-of-contents)

The CanalNETWORK product is updated to include the following reviews and modifications. Some of these are environemnt related settings, that are also applicatble while working on drainage network projects.

1. Improved guidance on import of canal routes. Intersecting alignment routes will now guide precise issue resolution, indicating at least one vertex/segment where the issue is encounterd.

    <img src="./media/Image 075.png" style="width:5in">



1. Toolbar button added for quick access to network preferences and other project settings.

    <img src="./media/Image 1.png" style="width:5in">

2. Default settings to network preferences are reviewed to reflect common design needs.

    <img src="./media/Image 6.png" style="width:4in">


1. Farmblocks can now be created and processed for a selected canal. The process attempts to identify connected routes to the selected canal, and create farm blocks. The farmblock data table also reports focused area statistics for the selected route (and its dependants).

    <img src="./media/Image 3.png" style="width:6in">

1. Farm blocks are now better managed, thanks to streamlined data structure. Users can simply toggle on/off farm blocks.

fig fig

1. Farm blocks enhanced vertex editing - add/remove, trim to canal


1. Variable Earth cut and shape fill is now acceptable for canal routes.

    <img src="./media/Image 013.png" style="width:4in">

1. Modified and improved subroute filtering and selection algorithm implemented. The new algorithm works better leveraging connectivity relations from node hirarchy.

1. Intercepto Drain

1. Farm blocks




BugFixes:
1. Node inverts at canal begining of routes (connected to a DummyRoute) now responds to arthimatic input at node invert edit.

    <img src="./media/Image 5.png" style="width:6in">


1. Floating node edit tool for tag and station corrected.

    <img src="./media/Image 074.png">



### Drain Network Enhancements
[Back to ToC](#table-of-contents)

New updates and enhancements to the DrainNET product include the following:

1. Default profile view is set to *Drain USControl*, allowing design mostly in cut conditions as a starting conditions. This is a most desired function in drainage canals design.

1. Naming issues resolved for drain, including sorted presentation for corresponding farmblock areas.

    <img src="./media/Image 7.png" style="width:6in">

1. Improved BoQ listing for controls (Outfalls), and drops to show corrected stations (in accorance with *Profile View* settings).

    <img src="./media/Image 8.png" style="width:7in">

1. New algorithm for subroute selection in drain networks, more effective and accurate.

    <img src="./media/Image 9.png" style="width:7in">

1. Reviewed `Explore Outputs > Batch Process > Explore Subroutes...` in line with improved subroute filtering algorithm.

1. Improved plan view generation for drain networks, now showing corrected stations for control and drop structures.



Bugfixes:
1. Node inverts at canal begining of routes (connected to a DummyRoute) now responds to arthimatic input at node invert edit.
 
 2. Profile view variable (in project preferences) now displays correct settings. Previously, it was static.

[Back to ToC](#table-of-contents)

END.







