# Introduction to CanalNET Software and Its Capabilities

[Back to Home](..\Index#online-documentation)

Well come!
<!--
If Preview window is not working, disable any pulgins. Right click on any .md file, and choose Mark Down Editor, also choose Set to default.
-->

<!--- Work on these as you get time.

[  ] DOC: When updating, start from CanalNET. Proper message if from drainNET
[  ] DOC Resize fcn recalculate discharge, canal section by reapplying design criteria. Hence most node info are reset (CBL, drops, ioInvts(1), ioInvts(2),...)
--->
---
CanalNETWORK is a software product that offers targeted solution to the design, analysis and documentation of a system of gravity canal networks. It is a product of a committed work to understand the practice of irrigation systems design in the local context, as well as governing theory in open channel hydraulics. 

This introcution is intended to give basic knowledge about the key problems that the software solves, and different tools available to solve them. It focuses on key features of the software, and is NOT a comprhensive document containing all the details. 

The following topics are discussed:

## Table of Contents
<!--TOC-->
  - [Uses and applicaiton of CanalNETWORK software](#uses-and-applicaiton-of-canalnetwork-software)
  - [Software Operating Limits](#software-operating-limits)
  - [Important System Related Notes](#important-system-related-notes)
  - [Data and Software required for use with CanalNETWORK](#data-and-software-required-for-use-with-canalnetwork)
  - [Standard workflow](#standard-workflow)
  - [Download and Install The Software](#download-and-install-the-software)
<!--/TOC-->

Refer to other sections of this documentation to learn more about specific usage and application of the software to tackle day to day design tasks.

If you have any comments about this document, we will appreciate if you drop us an email at [info@quanomic.et](info@quanomic.et)

## Uses and applicaiton of CanalNETWORK software
[Back to ToC](#table-of-contents)

CanalNETWORK software is an all-in-one solution, that allows to design, analyse and document the planning and design of canal irrigation systems. It allows to process data from start to end, allowing production of reach graphic and tabular documents to AutoCAD, as well as other text presentation software.

CanalNETWORK software for use in:

* A system of open canal irrigtion network (supply only)

* Canal network connectivity analysis, and automatic generation of labels /tags for entire network

* Complete and detailed Longitudinal design of individual canal routes

* Automated generation of detailed and summary bill of quanity

* Automated generation of different drawing products

* Collaboration between enginners and team leads to tackle large scale projects

* Compact saving and sharing of design data

* ... and more.

## Software Operating Limits
[Back to ToC](#table-of-contents)

CanalNETWORK software has the following operating limits while in use for any network formulation and analysis.

- Manning's equation, and the Critical Tractive Force method of analysis are available for flow analysis and canal sizing
- Maximum of two branches to a node are allowed
- Flattest slope possible 1/10,000
- Steepest slope possible 1/100
- Maximum allowable canal side slope 5H:1V
- Thineest canal lining 0.001M, Thickest Canal Lining allowed 50Cm thick
- Maximum number of Canal Generations 10 Gens
- Minimum length of canal routes acceptable is 25m.
- Minimum acceptable curve radius is 20m.

## Important System Related Notes
[Back to ToC](#table-of-contents)

CanalNETWORK application has the following minimum system requirements.

- Machine: Core i7, 9th Gen, X64 (SSD highly Recommended) 

- RAM: 8GB

- GPU: 4GB

- Screen resolution 1080x1980 (FHD). Two monitors recommended for working with AutoCAD side by side.



Working with different AutoCAD versions is possible.

- iCAD and CanalNETWORK products are fully tested on AutoCAD 2018 version. However, users have applied them using AutoCAD 2020, 2022, 2023 versions. This include Civil3D products, started as AutoCAD apps.

- If there are multiple versions of AutoCAD installed on a machine, CanalNETWORK product links to the current open version, and retains this version through out the session. It will not work with other versions opened after this. To connect with other versions, restart the CanalNETWORK application.


## Data and Software required for use with CanalNETWORK
[Back to ToC](#table-of-contents)

Working with CanalNETWORK software requires the following tools:

* iCAD software (a related product)

* AutoCAD 2018 and latter

In addition, text and spreadsheet applications are also helpful to export and/or import data to and from.

CanalNETWORK software handles detailed design task for an system of irrigation canals, whose layout has been well prepared. It does NOT include solution for creating layout of canals. The following data are required to start using the software:

* A canal layout drawing on AutoCAD: This provides the basis for the design of network of canals as a system.

* Topo cloud data (from surveying or other source): that is used to generate profile data for longitudinal design

* a design criteria for the project: that provides detailed values of reference criteria and other governing factors (e.g., duty, slope, limiting velocity...)

## Standard workflow
[Back to ToC](#table-of-contents)


CanalNETOWORK allows for flexible design approaches and processes. However, due to high dependency of tasks on available data, it is recommended to adopt the below discussed workflow. Adopting this workflow is proven to offer optimal progress towards the final products in the shortest possible time.

![](Images/Workflow%20Oct22.png)

Note in the above figure that:

- The starting input data are AutoCAD layout map, Topo Cloud data, and Design Criteria.
  
  The AutoCAD lauout map is required to have ONLY the polylines representing the canal routes. Contour maps, and other topgraphic features are not required. Unless needed for potential realigning, removing these additional data is recommended for speed.

- Network resolution process ensures the connectivity between each route, through the automatic Node Creation task and available management tools (in `Workflow > Nodes >` ). In the process of resolving connectivity, editing the polyline objects representing individual routes is often unavoidable, hence the two way interaction shown. It is also important to check the profile of individual routes is always downgrade. This also requires adjusting the AutoCAD drawing.
  
  *Important Note: Network resolution task often forces change to AutoCAD objects. The AutoCAD file must be saved to maintain these changes frequently.*
  
  Network resolution also requires naming to be available. Use the maximum generation style available as a tentative source to complete this task.

- Establishing Network is generating, based on the resolved network, the right naming and design criteria to each route in the network. The Design Criteria is required for this stage. 
  
  Here setting exceptions is expected for some routes, using `Edit > Route Exceptions > Set Exception`. 
  
  Also, farm block data is imported (or auto-estimated) to allow automatic sizing of each route as per the designated duty in the design criteria.
  
  Q~i~ = d~i~ * A~i~
  
  *This is a key milestone in the progress towards longitudinal design task. Back up the network data at this stage for latter use.*

- Profile extraction is the final stage before longitudinal design. The AutoCAD polylines representing canal routes are refined in the node resolution process. Hence, one can use iCAD product to generate profiles for all routes. Note this stage must follow succesful node resolution.
  
  V (Vertexing): ensures the each parent canal registers OGL at point of intersection with a branch canal. Else, misleading figures may occur during junction design and hydraulic checks. `Use Workflow > Prep Network > Insert Vertex` . 
  
  I (Instancing): allows fast processing of subsequent tasks - from referncing, and profile extraction, to autodesign of longitudinal profile, to BoQ extraction. Handle this task wisely for efficient processes in subsequent stages. There are two ways for instancing:
  
  - Use AutoCAD addon tools to create instances manually from selection of AutoCAD objects
  
  - Use iCAD's CadExtract utility, and collect objects by layer to create instances quickly. This requires that polyline objects in AutoCAD, representing canal routes, are properly assigned to relevant layers.
  
  - Use CanalNetwork toos for automatic collection and grouping of canals by generation to a single instance, form  `Workflow > Prep Network > Create Instances`
  
  R (Referncing): is the process of georeferncing each canal route object in AutoCAD. This is done from the AutoCAD addon tool.
  
  P (Profile extraction): having completed the above three tasks sequentially, the user is now ready to tackle profile extraction using iCAD's `AlignmentProfileJET `module. There are two steps to extract:
  
  - Host the Topo Cloud data to a host object in AutoCAD
  
  - Collect the routes for extraction to the iCAD workspace. Instances are very helpful here, as they can help import all instanced routes in one click.
  
  - Start the AlignmentProfileJET module, and provide details. The module will extract data per specified inputs and save the data automatically to the accompanying file *drawingname.xsd*  in the same folder as the source autocad file, where drawingname is the name of the source autocad file.
  
  Use the CadExtract utility to check which objects have not succesfully extracted profile data, and run the module again for them until all hosts report completed profile data.
  
  Repeat the process for all instances. 
  
  *This is an important mile stone in the progress towards longitudinal design. Backup the project data from within CanalNETWORK.* Use `Workspace > File Managmenet > Backup Project Data...`

- Here the user brings everything together to sprint to Longitudinal design task. With every work backdup, start clean (that is delete .xsd file). Then:
  
  - Restore sized network data from `Workspace > File Managment > Restore Backup...` and point to the desired backup source file.
  
  - Link the CSV data file as a separate data source to the current project from `Workspace > File Management > Attach Alternate CSV Source..`. and point to the profile data backup file. This allows the software to read profile data for each route from this file.
  
  - Finally, use `Edit > Soft Reload Route` to render profile data for each of the routes in the network. Upon succesful completion, user can now directly interact with each route to procceed with longitudnal design task for each route.

Refer to relevant guide lines on how to proceed with each of the above stages, or final production of construction drawings.

## Download and Install The Software

To download the software, click on the link below.


Once the download is complete, 

1. Double click on the downloaded file, and allow to run.

    Note: Because you are executing a downloaded file directly, your antivirus protection software may alert you to allow the process. Click yes to continue.

2. Follow the instructions on the screen to complete installation.

3. Set up your AutoCAD for use with iCAD, following [the procedure outlined on this link.]()


[Back to ToC](#table-of-contents)

END.
