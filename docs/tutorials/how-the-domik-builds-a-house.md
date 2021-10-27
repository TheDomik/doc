# **How the Domik builds a house**
=== "(╮°-°)╮┳━━┳"
	![[Снимок экрана 2021-03-29 182815.jpg]]
	
=== "( ╯°□°)╯ ┻━━┻"
	![[Снимок экрана 2021-03-29 182512.jpg]]

House is a builded cells. Cells are a grid collection of parts with positions. Parts are just names of objects that you want to see there. So, to build a house, the House Builder should find visual representations for these parts and place them in relevant positions.  
A visual representation of the part is a game object with a Part Builder component. From now on, we will simply refer to them as Part Builder.

=== "Part"
	![[Pasted image 20211021155519.png]]  
	![[Pasted image 20211021155546.png]]
	
=== "Skin"
	![[Pasted image 20211021155921.png]]  
	![[Pasted image 20211021161822.png]]

=== "Binding of a part"
	![[Pasted image 20211021160138.png]]

=== "Part Builder"
	![[Pasted image 20211021155310.png]]
	
=== "Result of building"
	![[Pasted image 20211021155404.png]]

 So, to build a Part, the house builder should find a Part Builder to it. How does it do it?  
 
The house builder will try to find it in skins. Skin is a collection of Part Builders. Skins are stored in interiors and in the House Generator skins list. 

=== "Interior"
	![[Pasted image 20211021160912.png]]  
	![[Pasted image 20211021160949.png]]
	
=== "House Generator"
	![[Pasted image 20211021161220.png]]

**Interior skins have higher priority than house skins**, so the House Builder will try to find it in them at first.

If the house builder find a Part Builder, it'll just ask it to build this part.

What does it mean for us?  
If we want to change something, we have to find and change its visual representation (a Part Builder) in skins. If it's a part of the room, in most situations it can be found in some interior skin, if it's a part of the facade or something common, it can be in the House Generator skins list.  

So how do you figure out which interior is applied to a room?  
You can do it visually or you can look at the name of the room, this name is the same as the name of the applied interior.  

=== "Rooms"
	![[Pasted image 20211019132827.png]]

=== "Interiors"
	![[Pasted image 20211019132900.png]]
	
??? question "How the room gets an interior?"

	Interior of the room is set in the process of the [[Calculate Room Interiors]] node, basically this node just sets some interior from the [[Floor]] interiors list.   

	
See also: 
[how to change room walls](how-to-change-room-walls.md), 
[how to replace models or materials](how-to-replace-models-or-materials.md).