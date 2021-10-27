# **Place Part By Mask For All Rotations**

![[Pasted image 20211004220511.png]]


This node allows you to find places by the mask and place a Part there. It'll process placing for all four rotations, so it's pretty useful if you want to place something somewhere and you don't care about specific rotations.     
And yeah, it'll place this part for every found suitable place.  
	
**Inputs:**

- **In** - cells there you want to place a part

**Outputs:**

- **Out** - placing result

**Properties:**

- **Part** - Part that you want to place
 - **Mask** - Mask that represents a place there you want to place a **Part**.

<br />

--------

# **Examples**
For this example we will generate a house basic cells, split it by rooms, add floor parts and calculate interiors.  

![[Pasted image 20211004223119.png]]
![[Pasted image 20211004223106.png]]

Now let's add some walls here!  
To do it we'll use a **Place Part By Mask For All Rotations** node with a **Forward Rooms Borders** mask.  

![[Pasted image 20211004223302.png]]
![[Pasted image 20211004223355.png]]
![[Pasted image 20211004223328.png]]

This is an alternative way to do the same thing:  

![[Pasted image 20211004223828.png]]