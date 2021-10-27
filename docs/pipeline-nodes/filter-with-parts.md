# **Filter With Parts**

![[Pasted image 20210922163351.png]] 

This node filters cells with several parts.   

**Inputs:**

- **In** - cells to filter

**Outputs:**

- **Success** - filtered cells

**Properties:**

- **Part Fields** - targets to filter
- **Filter With:** 
	- **Any** - filter cells, which contain any target part.
	- **All** - filter cells, which contains all target parts.
	
<br />

--------

# Examples
Input is a house that has been completed.  

![[default cells.png]]
![[Pasted image 20210922162630.png]]

#### Filter With Any Mode
This mode is pretty useful for situations when you want to find all variations of some part. In this example we will filter cells with a **Bed Segment** part with all possible rotations.  

![[Pasted image 20210922164331.png]]
![[Pasted image 20210922164026.png]]


#### Filter With All Mode
This mode is good when you want to find cells which should looks special.  
Here we will filter a room corners.  

![[Pasted image 20210922165027.png]]
![[Pasted image 20210922164851.png]]
