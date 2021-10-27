# **Shift**

![[Pasted image 20211009215700.png]]

This node shifts input cells 

**Inputs:**

- **In** - cells to shift

**Outputs:**

- **Out** - result of shifting

**Properties:**

- **X** - X axis offset
- **Y** - Y axis offset
- **Floor** - floor offset

<br />

--------

# Examples
In this example we'll shift a right side of the house.  
![[default cells.png]]
![[Pasted image 20211009220556.png]]
At first we have to filter a right side of the house.  

![[Pasted image 20211009220748.png]]
![[Pasted image 20211009220729.png]]

Now we can shift it.  
![[Pasted image 20211009220849.png]]
![[Pasted image 20211009220827.png]]

Let'd apply changes by the **Override** node.  
![[Pasted image 20211009220952.png]]
![[Pasted image 20211009221253.png]]

A very strange result, isn't it? That's because the process of overriding works with positions, not with cell id, so, from the perspective of the overriding node, we created some bunch of cells somewhere outside of the house and now trying to add them to the house. So, it just doing it.   
To solve this problem we have to just exclude cells which we want to shift.  
![[Pasted image 20211009221823.png]]
![[Pasted image 20211009221839.png]]

