# **Filter Random Input**
 
![[Pasted image 20210922153208.png]]

This node filters random input cells flow. 
	
**Inputs:**

- **In** -  cell inputs to select random flow.

**Outputs:**

- **Out** - result

**Properties:**

- **Mode:**
	- **Single** - return only one cells flow
	- **Multiple** - merge and return several cell flows

<br />

--------

# Examples
Input is a house that has been completed.  

![[default cells.png]]
![[Pasted image 20210918153153.png]]

Now let's filter a house border  

![[Pasted image 20210918155743.png]]
![[Pasted image 20210918160353.png]]
![[Pasted image 20210918155914.png]]

Now we can select a random **Filter By Mask** node output by the **Filter Random Input** node.  

![[Pasted image 20210922154018.png]]
![[Pasted image 20210922154033.png]]

And this is a result of the filtering with a **Multiple** mode on.  
![[Pasted image 20210922154150.png]]
![[Pasted image 20210922154214.png]]