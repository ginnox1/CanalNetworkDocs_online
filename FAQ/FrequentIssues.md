# Frequently Encountered Issues and their Resolution

1. Missing Design Data

	Canal Profile view misses CBL, FSL, CTL details at the end segment
	1. 

1. Shor canal lengths and large incremental distance for profile extraction. Create profile using smaller increments to get at least 5 to 10 data points.

1. Duplicate alignment routes


1. Non-responsive or bad routes can be caused at times. Specific issues noted incude
	- Routes with NaN at end (Gindira LSC_3)
	- Routes consistently failing to position their nodes after reload
	
When the canal alignemnt is too meandering with many coordinates, data sampling in CanalNET (done at 5m by default) may not import all details. This may cause
- NaN for OGL at end, qualifying for invalid route, and deleted every few minutes.
- for soft-reload tasks to fail to reposition previously or newly identified nodes.

Workaround:
- delete if the route exists in CanalNET data. Then reimport the route.
- The route may still contain profile data, remove both csv and ogl data from Workflow > Routes > PRofile.
- set Refine Profile values (in project preferences) set to a value between 0.5 and 5 (start small at 1.0 and progress from there).
- Now soft reload. This will reimport with raw coordinates but refined. If the process fails, increase the refine size, and try again.
- Then redo nodeId, naming (link with parent if detached), resize,  profile, and soft reload.
- Note, resize function may not capture branch areas.
- Note, The parent canal may need modification.


From accepted references in geotechnical references (AI generated)

| **Soil Type**   | **Mean Grain Size**        | **Angle of Repose (Dry)** | **Specific Gravity**  |
|-----------------|----------------------------|---------------------------|-----------------------|
| **Clay**        | < 0.002 mm                 | 15° to 25°                | 2.70 - 2.80           |
| **Silt**        | 0.002 mm to 0.05 mm        | 25° to 35°                | 2.65 - 2.70           |
| **Fine Sand**   | 0.05 mm to 0.25 mm         | 30° to 35°                | 2.65                  |
| **Coarse Sand** | 0.25 mm to 2 mm            | 34° to 40°                | 2.65                  |
| **Fine Gravel** | 2 mm to 20 mm              | 34° to 40°                | 2.65 - 2.70           |
| **Coarse Gravel**| 20 mm to 75 mm            | 40° to 45°                | 2.65 - 2.70           |


These refined values should be more accurate and reliable for typical soil types.





