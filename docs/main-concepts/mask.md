# **Mask**

The **Mask** -  is a mask of adjacency of **cells**.   
This is a description of some place, but in terms of accessibility from the target **cell**.   
Mostly useful in situations when you want to find borders of rooms or whole house.  

??? question "How to create a mask?"
	To create new floor select some folder in the **Project** window -> Right Mouse Click -> Create -> **Domik** -> **Mask**
	![[create mask.gif]]

![[Pasted image 20210402143556.png]]


- **Space** - what type of accessibility do you want to check?
	- **House** - you want to check that the neighbouring cells belong to the house (you want to find borders of house).
	- **Rooms** - you want to check that the neighbouring cells belong to target cell's room (you want to find borders of room).
- **Floor** - a floor where you want to edit cells to check.

---
 
To start working with **cells** select some **cell** in the grid.

![[Pasted image 20210330183433.png]]

- **State** - select what you expect from this cell:
	- **Not Important** - you don't want to check this cell.
	- **Accessible** - This cell should be belonged to the same room as a target cell if you selected the **Rooms space** or this cell should be belonged to the house if you selected the **House space**.
	- **Inaccessible** - this cell should be belonged to another room or doesn't exist at all if you selected the **Room space** or this cell shouldn't exist in this house if you selected the **House space**. 

---

You can see changes of the **mask** by the [preview system](preview-system.md).
![[mask preview.gif]].