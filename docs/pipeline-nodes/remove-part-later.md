# **Remove Part Later**

![[Pasted image 20211007225920.png]] 

This node collects an information about cells which you want to clear from some part in the future.  

**Inputs:**

- **In** - cells to clear

**Outputs:**

- **Out** - result

**Properties:**

- **Part** - part that you want to remove from cells

<br />

--------

# Examples
For this example we'll use a simple blanket of the house.  
![[Pasted image 20211007230150.png]]  
![[Pasted image 20211007230322.png]]  
Now let's try to place windows.  
![[Pasted image 20211007230446.png]]  
![[Pasted image 20211007230322.png]]  
It seems that nothing happened, but if you look at the house from the other side, it becomes clear that internal walls are blocking windows.  
![[Pasted image 20211007230859.png]]  
So let's fix it!  
The naive way to fix it is just using a **Remove Part** node.   
![[Pasted image 20211007231030.png]]
![[Pasted image 20211007231056.png]]
Looks almost good, but there are walls in the corner, although they shouldn't be there.  
Why?  
Well... we have the corner cell in the both flows at the same time, so, in process of merging we have two intersected cells with the same position, but one still has left internal wall, and second has right internal wall, so they both add these walls to the final cell when merging.  
![[merge removing artifact explain.png]]  
Merging results of removing will always cause artifacts in intersected cells, so don't merge results of removing. 
But... that to do?  
Answer is simple.  
Just remove parts **AFTER** merging!  
And exactly for that there are the **Remove Parts Later** node and the **Apply Removing** node.  
![[Pasted image 20211007234920.png]]
![[Pasted image 20211007234942.png]]
