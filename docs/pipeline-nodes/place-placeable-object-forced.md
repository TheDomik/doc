# **Place Placeable Object Forced**

![[Pasted image 20211005165423.png]]


This node is an alternative to **Add Part Node**, but, unlike it, it applies changes to the surrounding space.  
	
**Inputs:**

- **All** - the main cells flow
- **Target** - cells in that you want to place a placeable object

**Outputs:**

- **Out** - placing result

**Properties:**

- **Placeable Object** - a placeable object that you want to place
- **Turn** - force turning
	

<br />

--------

# Examples
For this example we'll use a very simple house blank.  
![[Pasted image 20211006131933.png]]  
![[Pasted image 20211006130430.png]]  

Let's imagine that we want to place some stairs in a specific cell. That will happens if you'll use an **Add Part** node? Well... something like that.  
![[Pasted image 20211006130228.png]]
![[Pasted image 20211006130334.png]]
![[Pasted image 20211006130430.png]]

Looks totally wrong, that's because we are not removed internal walls, ceiling and floor on the top floor. We can remove them by the **Remove Part** node, or... we can just apply Placeable Object actions! To do it we have to use a **Place Placeable Object Forced**. We already have a preconfigurated Stairs Placeable Object, so let's use it.  
![[Pasted image 20211006131336.png]]
![[Pasted image 20211006131203.png]]
![[Pasted image 20211006130556.png]]
![[Pasted image 20211006130447.png]]

And we can even rotate it if we want.  
![[Pasted image 20211006131605.png]]
![[Pasted image 20211006131621.png]]