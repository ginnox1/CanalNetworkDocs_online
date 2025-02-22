# CanalNETWORK 2.5 (Feb 25 2024)




**Hello and Welcome Again,**

We are thrilled and excited to bring to you yet another enhanced version of <strong> Version 2.5 of CanalNETWORK and DrainNETOWRK</strong>, including major updates.

In this release we provide updates for better user experience, and bug fixes found while testing previous releases. The DrainNET product resources are enhanced in a major way to accommodate key workflow requirements in design process.



Big Thankyou, <strong> EEC  </strong> for your trust, contributions and support.


<p style="color:green"> Happy Designing! </p>

<p style="color:blue">Team Quanomic.</p>


*Skip to read [What's New](#whats-new)*



## Update Resources

Update your version of CanalNETWORK product as follows:
1. Download the update resoruces from [Latest CanalNETWORK update resources](https://drive.google.com/uc?export=download&id=1Ov_tptZDHdrvIf7o1ogrlfpb_iWiBgvD)

    The latest is **Version 2.5.0.4725**

    Accompanied by **Version V4.9.5** of iCAD Bridge Application.


    > **Important Note:** Make sure AutoCAD is closed before you continue. If not, your update may not work, and require time to sort out. This release contains updates to the ***iCAD Bridge*** application.

2. Start CanalNET product, go to `Help > Updates...` Then choose `Manual` option. This will ask to close the application and re-start. Choose `Exit` to agree, and continue.
 

    > **Important Note:** Do not start updates with DrainNET product. The update process may not work, or exhibit unexpected behaviours.

3. Upon restart, the launcher application will ask if you would like to download or manually update. Choose `Manually`. On the file explorer, point to your downloaded resource file. The rest will be handled by the launcher.



## What's New

### CanalNET Updates

[Back to ToC](#table-of-contents)

1. Improved drop type selection, after integration of the new vetical drop structure in project preferences.

    <img src="./media/Image 001.png">



1. Integration of a new type of turnout design, based on guiding drawings and excel templated. The new turnout now generates dimensions tables for the new drawing. It has also features for determining number of pipes and pipe invert levels.

    <img src="./media/Image 002.png">

    Please refer to the documentation for assumptions and details considered when integrating the feature. The section on [Longitudinal Design of Canals Exploring Turnouts]()


1. Multiple routes exception setting capability is now included. Users can select multiple canals and create exception names in one go. 

    Note: All selected canals must branch from the same parent canal.
    Note: The automatically generated names follow a patter of the dynamic character in the input. If alphabet, or number, subsequent names are created sequentially.


    <img src="./media/Image 003.png" style="width:6in">

    
1. Auto change data host shapes on the fly. Helpful tools while saving networks or cloud data. When a new (previously untagged) AutoCAD object is selected to host surface data, or canalnet data, the shape automatically changes.

    <img src="./media/Image 004.png" style="width:4in">

    The feature also allows to provide object tags.

    <img src="./media/Image 005.png" >

 
2. Plan view is icluded on DrainNET application product in this version. Users can visualize and interact with the views, and product to AutoCAD following usual procedures.

    <img src="./media/Image 006.png" >

 1.  DrainNET now displays corrected column headers to LSec data table.

     <img src="./media/Image 007.png" style="width:6in">

 
 
### Bug fix:

The following fixes are made in this update.

- Batch BoQ now handles selections in profile view axis, to avoid applying specific algos (e.g., report by chainage) in batch processes. Previously resulted in long (endless loop difficult to abort)


- LSec plot datum crossing fix. Users must follow the usage note, that canals must be updated for LSec Data once in production view to avoid these issues.

- Exception naming correction for generating to AutoCAD, that resulted in ignoring underscore characters.

- Duplicate label text in AutoCAD when generating cross-section drawings improved.


END.