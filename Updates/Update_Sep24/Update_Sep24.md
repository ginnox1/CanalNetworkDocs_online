# CanalNETWORK 2.5 (Sep 2024)

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

    The latest is **Version 2.5.0.4514**

    Accompanied by **Version V4.9.3** of iCAD Bridge Application.


    > **Important Note:** Make sure AutoCAD is closed before you continue. If not, your update may not work, and require time to sort out. This release contains updates to the ***iCAD Bridge*** application.

2. Start your product, go to `Help > Updates...` Then choose `Manual` option. This will ask to close the application and re-start. Choose `Exit` to agree, and continue.

3. Upon restart, the launcher application will ask if you would like to download or manually update. Choose `Manually`. On the file explorer, point to your downloaded resource file. The rest will be handled by the launcher.



## What's New
[Back to ToC](#table-of-contents)

Key improvements are made for the period that cover a range of topics identified by our team, as well as user.

1. The context menu command available for editing drops is made available to designed bedlevels, allowing even more flexibility and contorl on vertical design of canals.

    <img src="./media/Image 001.png">

1. Improved handling of invlaid routes on import, this time for L<25unit routes. In previous versions, these routes were reported, but not effectively removed from the import collection.


1. Included B/D ratio specifically for lined canals, using recommended equation. The canal sections of lined segments are now designed accordingly. This feature automatically detects the lining settings (in Construciton Variables) and applies the ratio as needed. Users can still override design criteria settings manually, to apply or remove lining on a given canal generation.

    <img src="./media/Image 002.png">

1. Improved route coloring algorithm. This function now works for sub routes, as well as respects dummy routes if found. The assigned colors are also consistent between sessions.

    <img src="./media/Image 003.png">

1. Typical drawing can now be built in to deployed applications. Currently, drops, division boxes and turnouts are included. In the future, outfall structures will be included for drainage works. This meanse, the users can import these drawings to their autocad environment, ensuring consistency in production. A new menu command is introduced for this action.

    <img src="./media/Image 004.png" style="width:6in">

1. In addition, documentation is continually enhanced and updated to reflect the changes in software algorithms and functioanlities.

## What's New in DrainNET
[Back to ToC](#table-of-contents)

The product is under development to meet user expectations in design workflow. In this release the following funcitons are included:

1. The lognitufinal design algorithm is improved further to better account for CTL-OGL=0 condition at the begining of feeder canals in the network, as well as setting invert levels at the begining of canals.

    <img src="./media/Image 005.png">


1. Abiilty to reset Outfall heights at junction nodes. The values set to this variable at any node used to be persistent, requiting back and forth to adjust. Now the user can input an empty character to reset it. This value is set automatically based on prevailing terrain condition and hydraulics.

    <img src="./media/Image 006.png">


1. The Resize tool is enbanced to now reet control invert levels to project preferences (Node Invt Level=-0.5 by default, or setting provided by the user and removes outfall height settings. We notice this can accelerate design processes.



## Bug Fixes

- Fixed 404 error message on online documentation home page


END.





