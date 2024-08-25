# DrainNET Docs

Well Come to the DrainNET product documentation. The product operates mostly on learnings and skills from using the CanalNET product. This page and its linked contents provide specific guidance on use cases and skills that are specific for use and application and drainage canal networks.

Use the below links to navigate the page and its contents.



## General Assumptions and Conventions

Drainage canal alignments are drawn away from parent canals. For drainage networks, this would mean that alignments are drawn FUS direction.

Once network is resolved and sized, the design of individual routes shall be executed from the most downstream to upstream. This would be incotrast to the design of routes in supply canal network, where task progresses from upstream parent canal to downstream branch canals.

## User Interface for DrainNET product

Profile view axis

Node editor panel changes

CanalSection Designer (Perfoemance button) suppressed








## Design Criteria for DrainNETWORK

Reduced number of criteria parameters compared to that in CanalNET. The valid parameters are shown below. Their definition and expanation is included.

No FSL-OGL criteria in design criteria, hence no annotators and related features.


## Routes

Namin styles MD, SD, TD, FD 

Default design criteria for drain canals

dashed line style if invert diff between end and bed is le o, contrast to supply network

## Node Invert:

Nodes represent segments downstream

always attempted to locate nodes meet CTL==OGL. (to avoid unnecessary cut)

minFSL-OGL set to -99

stBranchRaise='Free'

mFSD=-99 Full supply depth

DHD= -1*DHD*

DBL Design

- drop adjust funcitons

- DBL create, and draw

- fitForNoDrop

reverse geometry analysis in comparison to supply canal drop positioning.

Node inverts for branch inlets are positioned to a maximum of:

- OGL-CTL of Branch at control

- CBL at collector canal.

## Profile Views
Mode 0

Mode 1

Mode 2


## Understanding OutFall Heights at Nodes
Note: only one outfall height can be set, and is applied to both branched. 

Single feeder

Two feeders: Outfall height is set for both left and right feeders, representing the differnce of water surface levels with the recieving drain canal. Hence, the invert levels of each feeder is set by subtracting the FDD (Full Drain Depth) from respectice water surface levels, and hence may vary.



## DBL Design and recomended practice

Review tentative designs from feeder to collector drains. For instance QD to TD to SD and to MD. This will ensure invert values for controls / nodes are set accordingly.

D->SD...

Invert changes at controls in recieving canals impact hydraulics at juction with feeder canals, particularly the inlet invert. DBL drawing for branch drains may show oddly positioned bed levels, because existing data relects previous invert locations. 

![fig1](Images/Image%201.png)

This can be easily corrected by clicking on the node, and using `Ctrl+R` or redraw. To reduce/avoid this step deesign/explore from downstream to upstream.

![fig2](Images/Image%202.png)

, especially near segments close to the recieving canal. Accordingly prev

## Using Dummy Routes


## Typical Outfall Structure

