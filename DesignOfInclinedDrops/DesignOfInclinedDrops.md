# Design of Inclined Drops
Introduced Dec, 2024.

The design of inclined drops is handles by use of floating nodes, like many other structures in irrigation systems. This include Head and cross regulator structures. The properties and various settings are managed from the floating node, once the node is defined as a structure.

<img src= "./media/Image 1.png" style="width:6in">



<!--TOC-->
  - [Key considerations](#key-considerations)
  - [Usage](#usage)
  - [Exploring Views](#exploring-views)
  - [Explorting Dimension Tables](#explorting-dimension-tables)
  - [Generating Bill of Quantity](#generating-bill-of-quantity)
  - [Hydraulic Design](#hydraulic-design)
  - [Future Work](#future-work)
  - [Technical Notes](#technical-notes)
<!--/TOC-->

## Key considerations
[Back to ToC](#table-of-contents)

The following are the key considerations in the current release.

- The flow at entry MUST maintain upstream hydraulic grade line. This will result in widths smaller than the canal bed width.

- FLow width can not be less than 0.4.

- The chute length is hydraulically short. This means, there is no enough length in the glacis for significant head loss to affect the pre-jump flow depth. If this condition is not met, the designed energy desssipation pool will be conservative.

- The transverse profile of OGL at drop location is horizontal.

- The maximum pool depth allowed is 1.0m.

## Usage
[Back to ToC](#table-of-contents)

To define and analyze an inclined drop structure along a given route, follow below steps.

1. Select the segment of the route where the structure is needed, and start the floating nide insertion command from `Workflow > Floating Nodes > New...` menu command.

    <img src="./media/Image 2.png" style= "width:6in">

1. Interactively select a location for insertion, and click when done.

    <img src="./media/Image 3.png" style= "width:6in">

1. Click on the newly inserted floatin node and edit its properties from `Workflow > Floating Nodes > Edit...`.

    <img src="./media/Image 4.png" style= "width:6in">

    Provide an indentifying tag that suits your need.

1. Provide the fall height in the Node Edit panel.

    <img src="./media/Image 5.png" style= "width:6in">

1. Start the design process from `Workflow > Floating Nodes > Canal Structures...`. Select the *Inclined Drop* Type, and choose design.

    <img src="./media/Image 6.png" style= "width:6in">


    Then provide details that are needed for design.

     <img src="./media/Image 7.png" style= "width:4in">

1. The initial solution is shown on the detail view axis, and a dialo confirms the reulsts.


    <img src="./media/Image 8.png" style= "width:6in">

    Click continue.

The structure is fully defined, and designed now. You can explore the solutions as below.



## Exploring Views
[Back to ToC](#table-of-contents)

Before you can explore the design dimension of the structure, the views must be generated.

1. Click on the Floating node object in profile view.

1. Click on the radio button on the detail view axis panel. This will generate the elevation view.

    <img src="./media/Image 11.png" style= "width:6in">

    Clcik on the radio button again, to create the section view.

     <img src="./media/Image 12.png" style= "width:6in">

1. You cangenerate this drawings to AutoCAD using the `Ctrl`+`p` keyboard combination, as is with any other result.




## Explorting Dimension Tables
[Back to ToC](#table-of-contents)

The outputs of the analysis for a typical inclinded drop structure looks similar to the one shown below.

1. Make sure there is no selection on the profile view axis, and start the `Workflow > Floating Nodes > Canal Structures ...` menu command. The following dialog appears.

    <img src="./media/Image 9.png" style= "width:3in">

    The available strucures are listed. 

1. Click on the desired structures, and the required action by holding the CTRL key, and click `Go`.

    <img src="./media/Image 10.png" style= "width:3in">

1. The data table now contains the design dimensions of the selected drop structures.

    <img src="./media/Image 13.png" style= "width:7in">

    A typical output contains the following details about a given drop.

    <img src="./media/Image 14.png" style= "width:2in">

You can copy the data, and take to other documents for further processing or documentation.

## Generating Bill of Quantity
[Back to ToC](#table-of-contents)

The bill of quantity can be extracted as part of the larger route, or the segment reperesented by the floating node.

> Note: You can not inquire BoQ for a structure alone.

To generate BoQ,

1. Select the floating node, and start the command from `Explore Solutions > Data Tables > Generate BoQ...` menu.

    <img src="./media/Image 16.png" style= "width:6in">

2. Choose the deired format, and click `Apply`.

    <img src="./media/Image 17.png" style= "width:4in">

1. The report is generated, similar to below. A typical listing is included in the figure for inlcined drops.

    <img src="./media/Image 15.png" style= "width:5in">

## Hydraulic Design
[Back to ToC](#table-of-contents)


The hydraulic design of the drop is carried out by first determining the width of the drop structure, with the objective of maintiaing upstream hydraulic gradeline in normal flow conditions. 

Once this is determined, the sizing for the remaining components of the drop structure is carried out based on two factors:

1. Incoming/Outgoing canal section gemetry and hydraulic property.

    This include:
    - flow section dimension (b, m, h, FB)
    - flow section hydraulics (N, s)
    - Structural provisions (Top widths, Approach/exit canal length, desirable apron thickness )

2. Surface flow hydraulics 
   
   This include:
   - Initial and sequent flow depths
   - Anticipated Length of hydraulic jump

3. Sub-surface flow hydraulics
    
    This incllude:
    - subsurface pressure distrubution in full flow and lean flow conditions;
    - provided upstream and downstream cutoff sizes



Detailed notes are included in further below in [Technical Notes](#technical-notes) 



## Future Work
[Back to ToC](#table-of-contents)

The following features will be included in upcoming versions.
- Reporting of hydraulic analysis
- Additional control on input variables
- Type II, III and Type IV energy dessipators
- Intermediate cutoff provisions

## Technical Notes
[Back to ToC](#table-of-contents)

The following are key hydraulic analysis and desired outputs for the design and sizing of an inclined drop structure.

1. Width of Drop

    The width of the verflow section for the inclined drop is determined by using relationships for critical flow conditions.

    1.5Yc= yn

    yc= (q^2/g)^(1/3)

    Combining the two equations gives

    yn= 1.5 ((Q/Wb)^2/g)^(1/3)

    which is solved to give the deired overflow width.


2. Pre-jump Flow depth

    The prejump flow depth is determined from the solutoin of energy conservation equation, between the upstream section and the toe of the glacis.

    <img src="./media/Image 22.png" style= "width:6in">

2. Type I Dessipator: Post Jump Flow Depth


    The post jump flow depth is calcualted by using the below relationship:

    y2=0.5y1(sqrt(1+8F^2)+1);

2. For Type I energy desipator, the length of the stilling pool is detemined as the maximum of the following:

    Lj/y1= 9.75(F1-1)^1.01

    Lj= 5.5*(Eus-Eds)



2. Type D Jump Length

    The length of jump envisaged is estimated from design curves from references below. The charts are presented below (from USBR Manual)

    <img src="./media/Image 18.png" style= "width:5in">

    Lj= Lj/Tw*ht, where Lj/Tw= f(F1) from the chart above.

    or, the minimum recommeneded limit in litrature.

    Lj= 5.5(y2-y1)

    which ever is maximum. 

 


2. Downstream appron length and flow profile.

    This is decided based on the jump type, especially if the jump roller begins not on the toe but some where upstream on the glacis slope. This is true for jump types B, C and D. 
    
     <img src="./media/Image 20.png" style= "width:5in">

    The distance of the jump roller is calcualted from the below chart.


   <img src="./media/Image 19.png" style= "width:5in">

   With this resuts, the downstream appron length is determiend from Lds= Lj-xj.

     <Img src="./media/Image 23.png" style= "width:5in">



2. Thickness of apron

    [To be included soon]
    
    



END.