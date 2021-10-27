# **Split Into Rooms**

![[Pasted image 20211012134709.png]]

This node splits input cells to rooms.  
Every cell has its own RoomId, by default it's zero. Splitting By Rooms node splits cells by setting new RoomId to them, so, after this process, you can work with borders of cells by filtering them with a Mask.  

**Inputs:**

- **In** - cells to split

**Outputs:**

- **Out** - result of splitting.

**Properties:**

- **Min Size** - minimum side length of rooms
- **Max Size** - maximum side length of rooms

<br />

--------

# Examples
In this example we'll split floors into rooms, find relative interiors to them and place furniture.  


First we have to add floor and ceiling to all cells.  
![[Pasted image 20211012135723.png]]
![[Pasted image 20211012135801.png]]
Now let's try to split it into rooms  
![[Pasted image 20211012135908.png]]
![[Pasted image 20211012135801.png]]  
And... Nothing happened! That's because the **Split Into Rooms** node just sets a RoomID to all cells, to actually split this house into rooms we should add walls in borders of rooms.   
Let's do it.  
![[Pasted image 20211012140132.png]]
![[Pasted image 20211012140314.png]]
![[Pasted image 20211012140144.png]]
Yay! It works!  
But that will happen if we'll try to do it without splitting into rooms?  
![[Pasted image 20211012140436.png]]
![[Pasted image 20211012140500.png]]
Well... One big room, as expected.  

Now let's add doors, interiors and furniture!  
!Note: It's better to add doors and windows before interiors and furniture because interiors calculating and furniture placing are sensitive for doors and windows.  
![[Pasted image 20211012141314.png]]
![[Pasted image 20211012141109.png]]

Next we have to calculate and apply interiors.  

![[Pasted image 20211012141409.png]]
![[Pasted image 20211012141422.png]]

Finish: add furniture.  
![[Pasted image 20211012141534.png]]
![[Pasted image 20211012141545.png]]