---
hide:
  - toc
---

# **Filter Internal Doors Places**

![[Pasted image 20210918181546.png]]

This node filters best places for doors between rooms.  
You have to add parts for all outputs and then merge them together in most situations.
	
**Inputs:**

- **In** - cells to filter
	
**Outputs:**

- **0** - cells for door part with original rotation
- **90** - cells for door part rotated by 90 degrees
- **180** - cells for door part rotated by 180 degrees
- **270** - cells for door part rotated by 270 degrees




<br />

--------

# Examples
Input is a set of barebone rooms without extarnal walls, windows, furniture etc.  
![[Pasted image 20210918182115.png]]  
![[Pasted image 20210918184412.png]]  

Now let's filter best places for doors and look up to the result.    
![[Pasted image 20210918184536.png]]  
![[Pasted image 20210918185105.png]]  
Looks... strange and useless.  
But it's not actually.  
Let's add a **[0] Internal Doorway** part to add a more context.  

![[Pasted image 20210918184920.png]]  
![[Pasted image 20210920165818.png]]  

Much Better! But now we have a parts overlapping.  
To solve it we have to remove **[0] internal wall** parts from filtered cells.   
![[Pasted image 20210918185341.png]]  
![[Pasted image 20210918185404.png]]  

Wonderful!  
Now let's repeat it for other rotations and merge them.  

![[Pasted image 20210920155142.png]]  
![[Pasted image 20210920155417.png]]  

??? warning "Don't use a **Remove Part** node before the merge node! "
	Don't use a **Remove Part** node before the merge node!  
	It'll cause artifacts because there is no way to merge removing actions properly.  
	Instead of that use the **Remove Part Later** and the **Apply Parts Removing** as it shows below.  
	![[dont_use_remove_part_before_merge.png]]  
	![[dont_use_remove_part_before_merge_result.png]]  

Still looks like a mess, but we have all doors!  
Last step - applying changes to the main cells flow.  

![[Pasted image 20210920170100.png]]  
![[Pasted image 20210920170151.png]]  