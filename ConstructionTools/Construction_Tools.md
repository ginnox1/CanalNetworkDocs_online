# Construction Tools
[Back to Home](..\index.md#online-documentation)

Begining Jun 2023, we have introduced solutions that can assist during supervision works. CanalNETWORK product has significant potential to contribute to construction processes and drive efficiency. Its data models and computational algorithms offer a strong platform to deal with routine bottlenecks encountered during construction supervision. The following are currently available.

> :exclamation: **Important Note**: This tool may not be available on your application depending on the version you are using, and your subscription level. Contact us for any querries.


## Table of Contents
<!--TOC-->
  - [Generating Shop drawings](#generating-shop-drawings)
  - [Changing Profile data for Canal Routes](#changing-profile-data-for-canal-routes)
  - [Alternate canal routes](#alternate-canal-routes)
  - [Estimating progress](#estimating-progress)
<!--/TOC-->

## Generating Shop drawings
[Back to ToC](#table-of-contents)

Use the guides in the Design Prodduction document of this guide, to generate the following working drawings to construction teams:

1. Canal cross-sections at increments

2. Extended cross-sections at desired stations

3. LSec Details for a specific range of station

4. Exagerated plans between stations

5. Extended Plans between stations

6. Canal Junctions and structures

## Changing Profile data for Canal Routes
[Back to ToC](#table-of-contents)

Often times, topographic data on the ground is different from that used during design. In such instances, revising design of canal routes can be done easily. To succesfully make the review, the data of the new topography for the canal route in question must be available in below format. 

![fig](Images/Image%20018.png)



Note: This action will replace all ground reference information for the canal, and the shape of the route can change in the plan view as well. 

Make sure:

- data contains all necessary columns for longitudinal referenceing (chainage), 

- Only one Ofst=0.0 is available to show centerline OGL

- X_Center, Y_Center and Teta_East columns, are available and contain valid data. X_Center and Y_Center represent Northing and Easting along the centerline of the profile data. Teta_East represents the bearing of the front leg at the given station (along the centerline)  with respect to the East. 

- At non straight routes, all the vertices of the alignment route must be captured for best results.

- The Teta_East values are averaged at each station to smooth out drawing generation.

![fig5](Images/Image%20020.png)



To replace the design data with such data collected from the field follow the below steps.

1. In CanalNETOWRK, make sure there is no surface data on the workspace - i.e., if the `Load Hosted Data...` menu item is not checked. If it checked, click on it, and choose `Clear`. 
   
   ![img](Images/Image%20022.png)
   
   
   
   ![img](Images/Image%20023.png)

2. Ensure that you are using the right source. If the project uses Alternative File as a source, link that file from `Workspace > File Utilities >  Alternate Csv Data Source... `. If not, i.e., if using the same source file as the buddy file, leave as is.

3. Finally, Check the final station on the profile data matches (closely) with the length of the route measured on AutoCAD. If this is an issue, the process will not compelte.
   
   Now, Copy the data in the table to the windows clipboard (Ctrl+C), being careful not to include empty cells or unwanted colmns or rows.
   
   ![fig2](Images/Image%20019.png)

4. slect the route object you want to apply the new data, and start the menu command `Work Flow > Routes > Route Profile`.
   
   ![fig2](Images/Image%20021.png)
   
   

5. A dialog will apear confirming there is no surface data on workspace. Choose `Paste CSV`.
   
   Note: It may help to copy the table data, just before choosing `Paste CSV`.

6. Choose `Next` and `Finish` on the import wizard to complete data import.
   
   ![fig](Images/Image%20024.png)
   
    
   
   ![fig](Images/Image%20025.png)
   
   If there is an issue, a dialog such as below will appear. 
   
   ![fig](Images/Image%20026.png)Otherwise a confirmation dialog appears. Hit `Apply` and you are done.
   
   ![fig](Images/Image%20027.png).

7. 

To see the the newly applied profile data, use `Workflow > Routes > Soft Reload Route` menu command. 

New drawings and volume calculations and design reviews are now possible with the new data.

## Alternate canal routes
[Back to ToC](#table-of-contents)

[To be included soon]

## Estimating progress
[Back to ToC](#table-of-contents)

This tool can estimate the volume of earth works executed under cut and fill conditions for a desired reach in a canal route. Surveying data collected along the canal centerline (representing modified Bed Level or MBedL) and along the canal top level (representing modified Top Level or MTopL) are required. The calculation of volumes are made up on the following assumptions:

- Elevation values on surveying data represent a flat surface to the left and right of the station they represent

- Executed fill work at a given station is calculated up to MTopL level on both left and right side banks. The assumption is the center - i.e., the water way is finished to design level as well. MBedL has no effect at stations fully in fill.

- Missing data at begining or ends are set to ground levels (OGL) in design data.

- Missing survering  MTopL= in a given range, the methods assumes the following:

Two sources for survey data can be used.

Method1: AutoCAD drawings

Use Profile drawings on AutoCAD created to scale. These must be referenced (using iCAD Addon tools) to the corresponding axes, or it will not work. For best results, draw survey data on existing profile drawing for a given route, before using it.

![ds](Images/Image%20017.png)

Method 2: Table data

Use table data presented in a spreadsheet (such as MS Excel). The table data can be three column data containing  STA, MBedL, MTopL. It can also be four columns containing STA, MBedL, STA, MTopL.

![fig2](Images/Image%20015.png)

![fig3](Images/Image%20016.png)

To analyze work progress, surveyed progress data must be avilable in the current workspace of CanalNETWORK. To begin, click on the canal route to meausre to make the profile view available. Then:

1. Start Routes > AutoCAD MBL, MTL menu command. AutoCAD will be on select mode and will prompt you to pick both MTopL and MBedL profile objects sequentially. 

2. To bring data from a table (e.g., excel), select the data and copy to clipboard (use Ctrl+C). Then start Routes > Table MBL, MTL menu command. This will continue the import process. If the data is correctly formated, it will be accepted.
   
   The import dialog appears. Click Next, and then Click Finish.

![fig4](Images/Image%2020.png)

![fig5](Images/Image%2021.png)

Note: If data does not meet requirements, process will abort.

This will include the data to the workspace, and also show the newly inlcluded data on the profile view.

![fig6](Images/Image%20003.png)

 Cross-section at different stations can now be explored to show how executed work is captured and presented in BoQ documents.

Cross-section near 0+635

![fig6](Images/Image%20014.png)

Cross-Section near 0+690

![fig7](Images/Image%20013.png)

Cross-section near 0+725

![fig8](Images/Image%20012.png)

Cross Section near 0+760

![fig9](Images/Image%20011.png)

Cross-section near 0+805

![fig10](Images/Image%20010.png)

Cross-section near 0+845

![fig11](Images/Image%20009.png)

BoQ containing executed work volumes can not be generated, using the usual tool from Workflow > Table Data > Generate Route BoQ. Make sure to select any canal segment in the route, and insert the stations of interest. 

![fig1](Images/Image%2023.png)

This will generate a listing similar to the figure below. It automatically includes earth work and fill information, and estimate percentage as a function of the design quantity available in the design information.

![fig24](Images/Image%2024.png)

[Back to ToC](#table-of-contents)



END.