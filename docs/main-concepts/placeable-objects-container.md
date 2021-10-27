# **Placeable Objects Container**
The **Placeable Objects Container** is a container of [placeable object](placeable-object.md)s or other [placeable objects container](placeable-objects-container.md)s.  
It's designed to group up objects which can present some common idea.   
Use it with objects which can or should be represented by different **parts**.  

![[Pasted image 20210104200256.png]]


- **Mode** - a placing mode:
	- **Place All** - try to place all items.   
	Use it to group up objects by some topic to make an [[interior]] list of **placeable objects** a bit cleaner.
	- **Place First Relevant** - iterate over items and stop after the first success of placing.   
	Use it if these items represent an object that trying to adapt to different environments.  
	Example: kitchen stoves for different sizes of the room.   
	- **Place Random Relevant** - place only one item by random.  
	Use it if these items are just variants of one object.   
	Example: a picture on the wall.  
- **Placeable Objects list** - a list of items that you want to try to place.

!!! note ""
	You can even make a container and fill it with other containers, and it'll try to place all child containers. 