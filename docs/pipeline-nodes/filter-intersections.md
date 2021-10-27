# **Filter Intersections**

![[Pasted image 20210921144425.png]]

This node filters intersected cells between A and B inputs.
	
**Inputs:**

- **A** - first pool of cells to check intersection
- **B** - second pool of cells to check intersection 

**Outputs:**

- **Out** - result

<br />

--------

# Examples
Input is a house that has been completed.  

![[default cells.png]]
![[Pasted image 20210918153153.png]]

Now let's filter these cells by **Forward House Borders** mask.  
![[Pasted image 20210921145215.png]]
![[Pasted image 20210921145301.png]]
![[Pasted image 20210921145230.png]]
 
 Now look at the result of mask rotation by 90 degrees. Perfect candidate for finding of cells intersection.  
 
 ![[Pasted image 20210921145511.png]]
 ![[Pasted image 20210921145534.png]]
 
 Let's find an intersection between cells filtered by 0° and by 90° rotations of the mask!  
 
 ![[Pasted image 20210921145833.png]]
 ![[Pasted image 20210921145859.png]]
 
 You can even invert the result by the **Exclude** node.  
 
 ![[Pasted image 20210921150125.png]]
 ![[Pasted image 20210921150204.png]]