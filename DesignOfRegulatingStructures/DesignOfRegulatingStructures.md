# Design of Regulating Structures
[Back to Home](..\index#online-documentation)

Flow regulating strucrures are a key component of a canal network system. They are provided at different points along canal routes to provide adequate control of flow condition during conveyance of irrigation water to different parts of the irrigation area. 

CanalNETWROKcurrently allow the design of Head Regulator Strucures and Cross-Regulator Strucrture. The design of these structures is handled with in the CanalNETWORK environment. Follow below links to navigate this page.

<!--TOC-->
  - [Defining the Structure](#defining-the-structure)
  - [Design Settings for HR/CR structures](#design-settings-for-hrcr-structures)
    - [Design Settings](#design-settings)
    - [Additional Settings](#additional-settings)
  - [Designing the Canal Structure](#designing-the-canal-structure)
    - [Design of Cross Regulator Structures](#design-of-cross-regulator-structures)
    - [Design of Head Regulator Structures](#design-of-head-regulator-structures)
  - [Exploring Solutions](#exploring-solutions)
    - [Dimension Tables](#dimension-tables)
    - [Detailed Drawing Views](#detailed-drawing-views)
    - [Bill-of-Quantity](#bill-of-quantity)
  - [Technical Notes](#technical-notes)
<!--/TOC-->


## Defining the Structure
[Back to ToC](#table-of-contents)

The design of regulating and conveyance structures is carried out using floating nodes. Floating nodes can be used for many purposes. Representing a structure is only one of the uses (Refer the chapter on [Longitudinal Design]() for more details.

   <img src= "./Images/Image 073.png">

---
 **<u>Important Notes</u>**
Before defining and designing structues with in the CanalNETWORK environemnt, it is recommended to understand the following notes:
    
1. Floating node positions can be created ONLY at stations in profile data, and hence are restrained by profile data available, and minSpacing project preference setting. It is important to consider this during profile extraction.

1. CR can be placed on any canal, any segment.
1. HR requires a regular (junction) node - connecting to a parent canal - just upstream of its location that is labeled neither as **Turn Out** nor as **Division Box**.

1. No drop strucrutes are allowed between the upstream node, and the floating node representing the structure.

---
To insert the floating node along a canal route:

1. Select the route in layout view.

2. In profile view select a segment in the route where you would like to locate the structre.

3. Go to `Workflow > Floating Nodes > Insert New`. This will activate an interactive tool to pick a location with in the segment selected. Pick a location.
   
   ![ds](Images/Image%20003.png)
   
   *Insert New menu command.*
   
   You can also edit the location after insertion by using `Workflow > Floating Node > Edit Current`, by first selecting the node.
   
   You can also delete floating nodes from `Workflow > Floating Node > Delete Current`, by first selecting the node.

4. Click on the floating node just inserted to select it, and go to `Workflow > FLoating Node > Canal Structures...` to define the strucrure. The *Edit Variables* dialog box appears for user input. Supply data as below:
   
   ![dsf](Images/Image%20047.png)
   
 
* User Tag or Name: specify the name of the individual structure that can adequately identify the structure properly latter. A standard convention is to use the canal route tag and type of structure, if needed including a serial number. (eg., HR 01 TC_3_12). This input is used to identify the control structure on plan views annotations.

* Type of Structure: The type of structure the floating node represents. Select from the available list (select the proposed structure of interest either cross regulator, head regulator or inclined drop).
  
  <u>Cross Regulators</u>: structures that are located on parent canals at a position some distance downstream of an off-taking branch canal. They are used to regulate head of flow in the parent canal, so that required amount of water flows to the branch canal. Often, their crest level is set the same as the canal bed level), Head regulators.
  
  <u>Head Regulators</u> are structures posited on branch canals. They usually have their crest levels raised in proportion to the expected overflow discharge rate.
  
 <!-- <u>Inclined drops</u> are energy dissipating structures located along canals. These drops can be designed as special structures - in contrast to regular vertical drop structures - with proper consideration for surface and subsurface hydraulic conditions.
  -->

  
  * Next Action: The proposed action to execute upon hitting `Apply` Button. There are two options.

      <u>Save</u> saves the information provided on the floating node objects, and exits.

      <u>Design</u> This choice saves the data, and continues to the design process. Note, if there is an existing design information on the selected node, the option will appear as **Redesign**. 
      
  5. Hit the `Apply` button to continue. 

<!-- Note: For Inclined drops, automatic check applies if drop height is sufficient for an effective energy dissipation upstream energy grade line (US.EGL) is sufficiently greater than the downstream energy grade line (US.EGL) if not, a message is displayed and check the exit drop and try again. Similarly, if the head loos not sufficiently defined the right message displayed for cross and head regulator and feed the value greater than 0.1m.


![[  ]](Images/Image%20004.png) 


*Dialog promoting invalid action for inclined drop design.*
-->

## Design Settings for HR/CR structures
[Back to ToC](#table-of-contents)


Specific parameters and settings for regulator structures design is found as part of the proejct preferences setting. It can be accessed from `Workspace > Edit Preferences...` menu command. The parameters are shown below.

<img src="./Images/Image 048.png">

Each of the variables are used in design, drawing generation and BoQ estimation as needed in different workflows. The following table defines and explains each variable.

Some of the paramters are shown also in the below typical section figure.
<img src="./Images/Image 050.png">

### Design Settings
[Back to ToC](#table-of-contents)



|No|Variable Name, and Unit| Values | Remarks|
|----------------------------------
|1| Discharge Factor| min 0.5<br> max 1.0<br>Default: 0.85| A discharge reduction factor to represent minimum flow conditions. <br> Note: This is applicable in CR structures only.|
|2|Allowable Exit Gradient(m)| min: 0.10<br>max:0.3<br>Default:0.2| Desired safe exit gradient desired at downstream end of the structures. This value is used to determine the depth of the downstream cutoff wall and the overall length of the impervious floor of the structures|
|3| Wing Wall Thickness(m)|min: 0.20m<br> max:0.50<br> Default:0.30m|Desired thickness for all wall components of the structures.|
|4| Min Apron Thickness(m)| min: 0.20m<br> max:0.50<br> Default:0.30m|Apron thickness for upstream and downstream impervious floor. Note, for downstream floor, apron thickness is also calculated based on subsurface flow conditions and resulting unbalanced head. The applied thickness is the maximum of the two.|
|5|Cutoff Wall Thickness(m)|min:0.05m<br>max:0.50m<br>Default:0.30|Thickness values for cutoff walls or piles as needed.|
|6|Gate Provisions|Gate width:<br><ul>min:0.30m<br>max:1.0m</ul>Pier Width:<ul>min:0.15m<br>max:0.50m<br>|Gate provision, specified as a pair of values representing GATE WIDTH, PIER WIDTH.|
|7|Filter Block Size(m)|min:0.20<br>max:0.50<br>Default:0.20|Desired filter block sizes to be used for design. Note, these are applied also considering the number of layers (below)|
|8|Filter Block Layers(-)|min:1<br>max:3<br>Default:3|Specifies how the filter blocks are laid out for quantity estimation. Note: A desired arragnement can be created by manipulating the block size and number of layers.|
|9|Silt Factor|min:0.05<br>max:12.5<br>Default:1.0|Silt factor for use in scour depth estimation and subsequent sizing of upstream and downstream cutoff walls, as well as sizing of the launching appron thickness.|

### Additional Settings
[Back to ToC](#table-of-contents)


|No|Variable Name, and Unit| Values | Remarks|
|----------------------------------
|1| Width of Walkway(m)|min:0.6m<br>max:1.5m<br>Default:1.0|Clear walkway desired on the operating slab or bridge deck of the structure, exluding the curbs on both sides.|
|2|Thickness of Operating Slab(m)|min:0.10m<br>max:0.30m<br>Default:0.20m|Thickness of the concrete slab.|
|3|Width and Height of the Curb(m)|min:0.10<br>max:0.3<br>Default:0.20|Thickness and height of the side curbs on the operating slab.<br><img src="./Images/Image 049.png"  style="width:1.5in">|




## Designing the Canal Structure
[Back to ToC](#table-of-contents)

The design of a structre represented with a floating node can be started or revisited at any time by following these steps.

1. Click on the floating node, and start the menu command `Workflow > Floating Nodes > Canal Structure...`.
1. On the *Next Actions* variable of the edit dialog, choose `Design` or `Redesign` option, and hit `Apply`.

This will proceed to the design process.

> **Important Note:** The design settings on project preferences are used in all design/redesin tasks. It is recommended to set these values once, and retain for the life of the project design.

In below sections, detailed presentation is made regarding the design steps followed for each structure.

### Design of Cross Regulator Structures
[Bacto to ToC](#table-of-contents)

Technical details on theoretical basis implemented in the software is included below in [Technical Notes](#technical-notes).

Cross-regulators are designed with out overflow crest height, or h~c~=0.0. The software searches for an ideal drop height that meets modular flow requirements.

The search begins from the currently provided drop height with increments of 2.5Cms until an acceptable flow condition is found. The detail view axis shows the solution found.

<img src="./Images/Image 056.png"><br>

Note: The solid line represents Normal flow volume, and dotted lines represent the reduced flow volume.

If solution fails, the following message is thrown.

<img src="./Images/Image 055.png" style="width:6in"><br>

> Note: It is recommended to start design with no exit drop provided. However, setting a desired height is also acceptable.


### Design of Head Regulator Structures
[Back to ToC](#table-of-contents)


Detailed theoretical basis for the design of regulating structures is included further below under the section [Technical Notes](#technical-notes).

For succesful design of head regulator structures, the floating node representing the structre must meet the following requirements.

1. The canal alignment mut be a branch canal to a supply canal. HR structures can not be applied on a parent canal for the project.

    <img src="./Images/Image 057.png">

1. The upstream node on the parent canal can not be a division box or a turnout.

    <img src="./Images/Image 059.png">


1. The node must be the first structure in the canal (no drops or other node/controls) before its location.

    <img src="./Images/Image 058.png">


1. The available bottom width must be greater than or equal to the gate width specified in the project preferences.

    <img src="./Images/Image 060.png">

Once these conditions are met the floating node is accepted for design as a head regulator structure. The process is much similar to that explained in [Design of Cross Regulator Structures](#design-of-cross-regulator-structures) above. 

The following workflow is implemented.

> Note: We refer to the supply canal as the **parent canal.** The **Host canal** is the canal on which the head regulator structure is located.

1. Determine the upstream flow condition, based on the hydraulics in the parent canal as well as the host canal alignment. This considers both the normal *Q* and factored *Q**Q~minFac~* flow rates in the parent canal. See [Technical Notes](#technical-notes) below for details.

   
    
    <img src="./Images/Image 065.png">

    This step often requires repositioning of the starting invert level for the host canal, inorder to accomodate the flow within the design full-supply-depth. Confirm to the prompt, and the invert level is adjusted. Click on the route in plan view to see the changes.
    
      <img src="./Images/Image 061.png">

    
2. The design of crest height and fall heigh is then carried out by considering modular flow requirements and broad crested weir flow conditions. A dialog confirms the solution, and graphical presentation shown in the detail view axis.

    <img src="./Images/Image 066.png">
    <img src="./Images/Image 067.png">

Different solutions for the design can be explored as detailed in the following section.


## Exploring Solutions
[Back to ToC](#table-of-contents)

One can explore solutions for Head and Cross-regualator structures as follows.

### Dimension Tables
[Back to ToC](#table-of-contents)

To list the dimension table for structures, follow below steps. The dimension tables are generated in accordance with the symbols and drawing presented below.

   <img src="./Images/Image 068.png">

1. Make sure there is no selection in profile view.
1. Then start the menu command `Workflow > Floating Nodes > Canal Structures...`. This will start the below dialog box.

    <img src="./Images/Image 070.png">
1. To delete or see the summary data related to a single structure skip to next step. To create the dimension tables, select desired structures and hit `OK` button.


    <img src="./Images/Image 069.png">

1.  choose one of the structures, and hit `OK` button. Confirm your desired action.

    <img src="./Images/Image 071.png">



### Detailed Drawing Views
[Back to ToC](#table-of-contents)


For a floating nodes whose design is fully solved and completed, section and elevation views can be generated. To view these, 

1. Select a desired node on the profile view axis.

1. Toggle the *View FUS/FDS* radio button above the detail view axis to generate alternate views. When toogled on an elevation view is generate.

      <img src="./Images/Image 062.png">

1. When toggled off, a longitudinal section is created.
    
    <img src="./Images/Image 063.png">


These drawings can be sent to AutoCAD at a desired scale and annotated for more detailed presentation.

<img src="./Images/Image 064.png">

### Bill-of-Quantity
[Back to ToC](#table-of-contents)


Bill of quantity is included as part of the canal route quantity schedule. To create one:

1. Select the desired canal route containing the structure, and make sure profile data is generated using `Workflow > Data Tables > Lsec Profile Data...`.

1. Use `Workflow > Data Tables > Generate Route BoQ...` menu command to create the BoQ schedule.

    > Tip: You can select the structure node, and create a specific BoQ for the node (and the segment upstream).

    <img src="./Images/Image 072.png">


## Technical Notes
[Back to ToC](#table-of-contents)

The design of cross-regulator and head regulator structures is carried based on the following considerations:

Note: Crest heihgts for overflow section are set automatically as follows.
- For Cross-regulator structures, *hc* is set to 0.0, retaining the CBL (Canal Bed Level) upstrem of the node locaiton.
- For head regulators, *hc* is set to a minimum value of 0.05m.


        Q = C_dBH^{3/2}
        Where:
        C~d~ is the Coeficient of discharge
        B is the available overflow length
        H is the resulting overflow head above crest level

The design of regulating structures is carried out ALWAYS to attain modular flow over broad crestd weir. Hence Cd value 1.70 is used.

<u>Overflow Width Design</u>:
The design process attempts to optimize available canal bottom width and set gate provission specifications to determine a feasible combination of gates and piers for the overflow section. This process also attempts to maintain the overflow head to closely match the existing normal flow depth in the incoming canal.

<img src="./Images/Image 051.png" style="width:5in">

<u>Modular Flow</u> The design iteration is carried out until a modular flow condition is ensured based on the following relation ship (See section figure above).

$$ h~2~/h~1~<=0.75 $$

> Note: Modularity is checked and established for both the normal (Q) and reduced (Q*Q~minFac~)discharge rates passing through the regulating structure.

For head regultors, the overflow condition is matched with upstream hydraulics at the parent canal (both normal and factored flow rates.)

The following schematic shows considerations built in to the software for upstream flow hydraulics on a head regulator structure.
    
   <img src="./Images/Image 065.png">

   > **Note:** the software considers normal flow and minimum flow rates in the parent canal, and the crest height is designed for the minimum flow conditions antiticpated in the parent canal, while attempting to maintain modular flow for both flow conditions in parent canal.


The above two considerations set the allowable headloss for the structure to operate optimally. Pre and post jump depths, y~1~ and y~2~ are then determined from energy conservation equations

Length of stilling pool is determined from 

L~pool~= 5(y~2~-y~1~)

the length of the glacis is determined using glacis slope *m~glacis~*, crest height *h~c~*, depth of pool *d~p~* and the elevation difference between the entry and exit to the structure as follows:

L~glacis~= m~glacis~*(h~c~+HL+d~p~)

The length of the overflow crest is determined to ensure broad crested weir flow using:

L~crest~= 2*h~1~, Lc>=0.50m

<img src="./Images/Image 052.png" style="width:4in">


The overall length of the impervious floor is determined from khoslas set of relations.

<img src="./Images/Image 053.png" style="width:2in"><br>

<img src="./Images/Image 054.png" style="width:5in">

The above relations allow determination of a safe overall length for the impervious floor. This in turn allows sizing of the upstream apron as follows:

Lu= L~total~-(L~glacis~+L~pool~), L~u~>=1.0m


Once the overall sizing of the structue is finished, protection works are sized as follows.

R= 1.35(q^2^/f)^1/3^, if h~1~<4.75q^1/2^, or<br>
R= 0.473*(Q/f)^1/3^, otherwise.

the, upstream and downstream cutoff depths (du, dd) are estimated from:

du= 1.25R-y~1~, and<br>
dd= 1.5R-y~1~, dd>=d~Gexit~




Note: m~galcis~=2.0 for all calcualtions.

[Back to ToC](#table-of-contents)

END.

