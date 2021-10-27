# **Calculate Room Interiors**

![[Pasted image 20211004112605.png]]

This node calculates suitable interiors for rooms.  
You have to return calculated interiors to the **END** node as it shows below.   
	
**Inputs:**

- **In** - cells to analyze

**Outputs:**

- **Room Interiors** - suitable interiors for rooms
		
<br />

--------

# Explain

There is no effect of room's calculating if you don't return it to the END node.  

![[Pasted image 20211004113320.png]]  
![[Pasted image 20211004113350.png]]  

But what will happen if you return the result of calculations to the **END** node  

![[Pasted image 20211004113635.png]]  
![[Pasted image 20211004113646.png]]  

But... There is furniture?   
To add furniture you have to use a **Place Furniture** node.  

![[Pasted image 20211004114033.png]]  
![[Pasted image 20211004114101.png]]  

Wait, wait, are these the same interiors? Why did the walls change color?  
That's because walls materials defined by the skins system, and in this example skins are dynamic. Every room has a bunch of randomly selected skins, and if you used a random engine somewhere before using of the skins, the result of the skins selecting will be different. So yes, these are the same interiors, but with another skins.  

You can also return calculated room interiors by the **Return Interiors** node as it shows below.  

![[Pasted image 20211004115019.png]] 
![[Pasted image 20211004114101.png]]  