# **Filter By Floor Tag**

![[Pasted image 20211029161833.png]]  

This node filter cells by the [floor tag](floor-tag.md).  
Use this node to filter and process a specific floor.  
	
**Inputs:**

- **In** - cells to filter

**Outputs:**

- **Success** - filtered cells
- **Failed** - unfiltered cells

**Properties:**

- **Floor Tag** - a [floor tag](floor-tag.md) that will be used as a filter

<br />

--------

# Examples
Input is a house that has been completed.  

![[default cells.png]]  
![[Pasted image 20210918153153.png]]  

Now lets filter a floor with a **Roof** floor tag.  

=== "Success output"
	![[Pasted image 20210918180235.png]]  
	![[Pasted image 20210918180245.png]]  

=== "Failed output"
	![[Pasted image 20210918180347.png]]  
	![[Pasted image 20210918180406.png]]  
