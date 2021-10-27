# **Place Stairs**

![[Pasted image 20211007134646.png]]

This node provides a placing of stairs.  

**Inputs:**

- **All** - the main cells flow
- **Target** - cells where you want to place stairs
- **Forbidden** - cells that are forbidden to change

**Outputs:**

- **Out** - floor cells that are now connected by stairs
- **Failed** - floor cells that have not been connected 

**Properties:**

- **Stairs** - a placeable object of stairs
- **Min Stairwell Length** - a minimal length of the stairwell, low number makes this stairs less realistic but more universal.
	

<br />

--------

# Examples
For this example we'll use a house without interiors, furniture and facades, because the **Place Stairs** Node designed to be used before calculating and applying interiors.  
![[Pasted image 20211007123525.png]]
![[Pasted image 20211007123324.png]]

Now we'll try to place a **Stairs 6x6** by the **Place Stairs** node.  
![[Pasted image 20211006131203.png]]  
Here we'll use the same cells flow for the **All** input and for the **Target** input because we want to try to place a **Stairs 6x5** in whole house.  
![[Pasted image 20211007134615.png]]
![[Pasted image 20211007132208.png]]
![[Pasted image 20211007132302.png]]
Here windows and doors intersect with the stairs and this is not fine. To solve it we have to add cells with them to the **Forbidden** input.  

![[Pasted image 20211007134506.png]]

=== "Top"
	![[Pasted image 20211007132739.png]]
	
=== "First Person"
	![[Pasted image 20211007132802.png]]
	
Now this is fine.   
But sometimes the house structure too complicated to be able to use only one stairs, so you have to add more stairs to connect other floors.  
In the next example we'll generate a house with another SEED.  
![[Pasted image 20211007134807.png]]  
Last 2 floors are not connected no, so we have to fix it.  
If you want to see not connected floors use a **Failed** output.  
![[Pasted image 20211007135107.png]]
![[Pasted image 20211007135153.png]]
To fix it let's try to place less demanding stairs.  
![[Pasted image 20211007150708.png]]
All cells that were processed by the placing of stairs now has a **Busy** part, so we can (and should) ignore them by adding them to **forbidden** cells.    
We also use a **failed** output as a **target** input because we want to place this stairs in not connected floors.  
![[Pasted image 20211007155517.png]]  
![[Pasted image 20211007160407.png]]  
A staircase appeared on the back of the house, between the last two floors.  
Now all floors are connected.  