# **Filter Neighbor** 

![[Pasted image 20210921175542.png]]

This node filters target neighbor cells.  

**Inputs:**

- **All** - the main cells flow
- **Target** - cells for which you want to find neighbors

**Outputs:**

- **Top** - top neighbor cells
- **Bottom** - bottom neighbor cells
- **Forward** - forward neighbor cells
- **Backward** - backward neighbor cells
- **Right** - right neighbor cells
- **Left** - left neighbor cells

<br />

--------

# Examples
Input is a house that has been completed.  

![[default cells.png]]
![[Pasted image 20210918153153.png]]

Let's filter the right side of the house.  

![[Pasted image 20210918155823.png]]
![[Pasted image 20210918160028.png]]

Now we can slice this house like a pie by using the **Filter Neighbor Cells** node.  
![[Pasted image 20210921185229.png]]
![[Pasted image 20210921185258.png]]

Or we can make something mad...  

![[house_side_moving.gif]]

Another example: let's select some random cell:  
![[Pasted image 20210921205522.png]]
![[Pasted image 20210921205536.png]]

Now we can add some cells around:  
![[Pasted image 20210921205655.png]]
![[Pasted image 20210921205727.png]]

This node is pretty useful for situations when you want to filter some floor.  
Let's filter the **Basement** floor by the **Filter by Tag** node.  
![[Pasted image 20210921205931.png]]
![[Pasted image 20210921210002.png]]

Now we can filter the top floor by the **Filter Neighbor Cells** node.  
![[Pasted image 20210921210245.png]]
![[Pasted image 20210921210256.png]]

Well, now, we can, for example, change the facade look.  

![[Pasted image 20210921210826.png]]
![[Pasted image 20210921210850.png]]