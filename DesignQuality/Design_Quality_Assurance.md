# Design Quality Assurance
[Back to Home](..\index#online-documentation)

The latest development in CanalNETWORK product features is the ability to automatically check quality of design. The process uses an agreed design criteria as a benchmark, to compare values from actual design.

The results flag any issue that do not conform to the provisions of the design agreement with in a prescribed tolerance.

> :exclamation: **Important Note**: This tool may not be available on your application depending on the version you are using, and your subscription level. Contact us for any querries.

## Table of Contents
<!--TOC-->
  - [Reference Design Critria](#reference-design-critria)
  - [Starting the Tool](#starting-the-tool)
  - [Check parameters](#check-parameters)
  - [Flag Symbols](#flag-symbols)
  - [Digitize LSec Designs](#digitize-lsec-designs)
    - [Required Data](#required-data)
    - [Prepare the LSec design for Import](#prepare-the-lsec-design-for-import)
    - [Setup the canal network](#setup-the-canal-network)
    - [Import from the LSec draing](#import-from-the-lsec-draing)
<!--/TOC-->

## Reference Design Critria
[Backto ToC](#table-of-contents)

Reference design criteria are the set of criteria that are to be used as a bench mark for evaluating the results of design in the entire network. These can be prepared manually, or loaded from a file. The latter method is always prefered, as it avoids possible data entry errors.

The reference design criteria must be loaded in to the current workspace of CanalNETWORK to use it as a benchmark for quality audit. After ensuring this, proceed to the next step to start the tool.

<img src="./media/Image 3.png" style="width:4in">


Look up the online documentation on [Creating and Managing Design Criteria](../DesignCriteria/#CreatingAndManagingDesignCriteria.md) to learn on how to save, load and edit design criteria in CanalNETWORK environment.




## Starting the Tool
[Backto ToC](#table-of-contents)


The tool can be started from `Workflow > Design & Analyisis > Quality Audit` menu command. 

<img src="./media/Image 1.png" style="width:5in">


Before starting the tool, make sure to select the canal routes that require checking.

> :bulb: **Tip**: Enable multi select to select multiple canals, and get a report for all.

Start the tool, and the report is generated in the format shown below. The presentation of results is discussed below.

<img src="./media/Image 2.png">

## Check parameters
[Back to ToC](#table-of-contents)

[Backto ToC](#table-of-contents)

Design quality is checked for selcted parameters and with reference to the settings in the design criteria. There are seven parameters that are used.

1. **Drop Flag**: checks if the spacing between drop structures any where in the segment does not fall below the minimum spacing requirement in the design 


1. **Slope Flag**: Checks the canal bed slope provided at the segment is with in &plus;1/~50~ or &minus; 1/~50~ of the design creiteria for the canal generation.
1. **Vel. Flag**: evaluates if the velocity of flow in the segment is with in the set limits in the design criteria. These are the minimum non-siliting velocity, and the maximum non-errosive velocities for the canal route. (V~min~ < v < V~max~)
1. **Shear Flag**: Checks if the shear stress computed for the final designed flow section is with in the limits set in the design criteria. (&tau; < &tau;~max~)

1. **Hump Flag**: Checks if there are humps introduced in the route canal, especially at control locations. Segments are flagged not accepted if the hump heights are more than 5cm. (h~hump~<0.05m)

1. **Backflow Flag**: This parameters checks if full supply levels are consistently downgrade. If not possiblity for backflow is eminent, that may cause siliting, overflow or the likes.
1. **FB Flag**: Freeboard provisions are checked against the set value in design criteria. If refenence values are specified, for instance as -1 to use USBR recommended tables, the built in values corresponding to the discharge capacity of the segment is calculated and used as the bench mark. Segments are not accepted if the provided freeboard higher or lower than the benchmark value by more than 0.05m.

## Flag Symbols
[Back to ToC](#table-of-contents)


Integers are used to represent acceptability of design results of a certain segment with respect to the bench mark values.
- +1 indicate the segment is acceptable for the specific parameter
- 0 indicates it was not possible to check that specific parametr for the segment
- -1 indicates the segment is NOT acceptabale for the specific parameter

The chart at the right of the table shows a graphic presentation of the results.

[Backto ToC](#table-of-contents)

## Digitize LSec Designs
[Back to ToC](#table-of-contents)

Digitizing existing designs a new and innovative way developed to allow fast reconstruction of LSec designs from AutoCAD environemnt, in to a fully editable network route in CanalNETWORK environement.

Users can leverage this tool to check designs, generate more details or reformulate existing designs.

### Required Data
[Back to ToC](#table-of-contents)

To effectively use this feature, two types of data are required:
1. the user is expected to have the design criteria used to design the existing LSec profile. The most important aspects are 
    - Hydraulic_Design Parameters, and
    - Construciton_Parameters

    These may or may not be required depending on the objectives of the reconstruciton.

    > :bulb: **Note** Any LSec drawing on (a supported version of) AutoCAD can be digitized. However, LSec profiles generated by CanalNETWORK can be reconstructed quickly with out much manual work, compared to products from other tools.

2. The LSec drawing for digitization
2. The layout alignments of both the parent and branch route is also required, along with the surface data source (usually csv format). This will be used to establish the network with adequate data for reconstruction.


### Prepare the LSec design for Import
[Back to ToC](#table-of-contents)

In the LSec drawing (in AutoCAD), create a reference axis using axis preparation tools, that fit the scaling and size of both the longitudinal distance and the elevation axis.

Then make sure to reference the following objects to the axis just created.

- Canal Bed Level profile
- Full supply level profile
- Canal Top Level Profile
- Canal Controls.



> :bulb: **NOTE**: Canal Controls are strictly vertically drawn at stations where offtaking or branch canals are found. They start at CBL and end at any height. Canal Controls are also drawn/expected at the end of the route.

If drawings generated by CanalNETWORK are used, all the above are already available, and continue to the next step.

<img src="./media/Image 014.png">{br}

### Setup the canal network
[Back to ToC](#table-of-contents)

Start with a clean CanalNETWORK workspace. Then:
1. Import the layout of the route to be reconstructed, and its parent canal. Both must have profile data prepared.

    <img src="./media/Image 001.png" style="width:7in">

    <img src="./media/Image 002.png" style="width:7in">


1. ID nodes for the two routes. This should identify three nodes in the network of two routes.

    <img src="./media/Image 003.png" style="width:7in">


2. Create a naming style for workspace using one that includes the levels for the routes in question. 
2. Then edit the design criteria to fit that used in the design of existing LSec plot. If you are manually reviewing data, select each route, use `Ctrl`+`E` to make sure to edit below variables in particular:
    - **N** Mannings rougness value
    - **m** canal side slope
    - **b/d ratio** used in design
    - **LType** lining type and thickness
    -**Smc, Smf** cut and fill shapes for canal water way.
    
    If a dcf file is available (for CanalNETOWRK designed projects), this can also be used. Simply go to `WorkSpace > Manage Design Criteria...> Import From File...`. 

    <img src="./media/Image 007.png" style="width:4in">

    <img src='./media/.png" style="width:in">

    

    Confirm to R`Replace` when prompted.

    <img src="./media/Image 008.png" style="width:3in">
    
    This will open the file explorer dialog. Find your dcf file, and hit `Open` to continue,

    <img src="./media/Image 009.png" style="width:5in">

    In *Pick Level* dialog, select those generations correpsonding to the routes in question (inthis example SC, and TC) Note this must be the same as used in setting exception below.

    <img src="./media/Image 010.png" style="width:2.5in">

    A dialog will confirm success importing the design criteria.

    <img src="./media/Image 011.png" style="width:4in">

    It helps to review the imported design criteria values for the above variales.
        <img src="./media/Image 3.png" style="width:4in">


2. Then set naming exceptions for the two routes, corresponding to the generation or level used for design.

    <img src="./media/Image 004.png" style="width:5in">

    > This is important, as it will dictate which design criteria will be used to reconstruct the route geometric and hydraulic data.

3. Now force-size the routes. Click on one route in plan view. Click on the segment in profile view. This will invoke the *No Canal* dialog. This is normal, and is because the network is not sized yet for discharge capacity. Choose `Force Canal`. Accept `Yes` to continue.
 
    <img src="./media/Image 005.png" style="width:4in">

    Igonre the *Failed* dialog message, and hit `Ok`. This is because there are no farm blocks found for this route.

      <img src="./media/Image 006.png" style="width:3in">

    Now the segment has a hydraulic and geometric property from the default settings, and clicking on the segment will show the typical section in detail view axis. 
    
    Repeat the same for the other route.

### Import from the LSec draing
[Back to ToC](#table-of-contents)

Now we are ready to import the LSec profile to the branch canal. 

Before starting the import tool make sure:
1. Every element to be imported is instanced. So, for CBL objects, make sure there is only one CBL object for the entire route range. If different objects are found, collect them in to instances.

    Do the same for FSL objects, and CTL objects.

> Note: All objects must be AutoCAD polyline object types, else process will fail.

2. Refernce all objects to be imported, by creating a reference axes around the LSec drawing and using the reference  axes.

> Instancing made just above can be very helpful for referencing multiple objects at once.

Lets invoke the command and proceed.

3. Invoke the command from `Workflow > Routes > Digitize LSec` . This will start a guided process to pick the instance objects. Select in the following order:
    - CBL object (or their instance)
    - FSL Object (or their instance)
    - CTL object (or their instance), and finally
    - Instance of Control objects.

    <img src="./media/Image 015.png" style="width:7in">

    The progress bar will inform progress accordingly, and the canal route is reconstructed. 

It can now be edited, explored or exported as any other route created with in CanalNETWORK environement.

> :bulb: **Tip**: This can be used to check the accuraccy of the design imported in comparison to the reconstruction by CanalNETWORK.

Examples of quality check using this reconstructed route can include, but not limited to:
- Plot FSL and CTL to see variances 
- run Design Quality Assurance tool to investigate performance with respect to design criteria
- Run Cut/Fill annotations to check for quantities


[Back to ToC](#table-of-contents)

END.
