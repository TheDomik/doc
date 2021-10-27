# **Remove Part**

![[Pasted image 20211007172402.png]] 

This node removes a part from cells.   
	
**Inputs:**

- **In** - cells in that you want to remove a part

**Outputs:**

- **Out** - removing result

**Properties:**

- **Part** field - part that you want to remove from cells

<br />

--------

# Examples
For this example we'll use a simple blank of the house.  
![[Pasted image 20211007172734.png]]
![[Pasted image 20211007172832.png]]  
In this example we'll select random cells on the last floor and remove some walls from them.   
Now let's filter the last floor.  
![[Pasted image 20211007173407.png]]
![[Pasted image 20211007173425.png]]
Next filter random cells.  
![[Pasted image 20211007173541.png]]
![[Pasted image 20211007173608.png]]
And remove a wall from them.  
![[Pasted image 20211007173646.png]]
![[Pasted image 20211007173704.png]]
And the final step - applying changes on the main cells flow by the **Overriding** node.  
![[Pasted image 20211007173818.png]]
![[Pasted image 20211007173837.png]]

!Note Don't use a **Remove Part** node before the **Merge** node!  
It'll cause artifacts because there is no way to merge removing actions properly.  
Instead of that use the **Remove Part Later** and the **Apply Parts Removing** as it shows below.  

Wrong:  

![[dont_use_remove_part_before_merge.png]]
![[dont_use_remove_part_before_merge_result.png]]

Good:  

![[well_using_merge_with_removing.png]]
![[Pasted image 20210920170151.png]]