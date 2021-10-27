# **Merge**

![[Pasted image 20210923145608.png]]

This node merges input cells together.  
	
**Inputs:**

- **In** - cells to merge. Multiple input is accessible (obviously)

**Outputs:**

- **Out** - merge result

??? warning "Don't use a **Remove Part** node before the **merge** node!"

	Don't use a **Remove Part** node before the **merge** node!  
	It'll cause artifacts because there is no way to merge removing actions properly.  
	Instead of that use the **Remove Part Later** and the **Apply Parts Removing** as it shows below.

	**Wrong:** 

	![[dont_use_remove_part_before_merge.png]]
	![[dont_use_remove_part_before_merge_result.png]]

	**Good:**  

	![[well_using_merge_with_removing.png]]
	![[Pasted image 20210920170151.png]]

<br />

--------

# Examples
Input is a house that has been completed.  

![[default cells.png]]
![[Pasted image 20210922162630.png]]

Let's filter house corners by the **Forward Right House Corners** mask.  
![[Pasted image 20210929123232.png]]
![[Pasted image 20210929123329.png]]
![[Pasted image 20210929123402.png]]

That's how result looks if we were select a **90** degree output.  
![[Pasted image 20210929123733.png]]
![[Pasted image 20210929123722.png]]

Now we can merge all mask rotations together to get all corners of the house.  

![[Pasted image 20210929123822.png]]
![[Pasted image 20210929123839.png]]


