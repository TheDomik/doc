# **Part Builder**

The **Part Builder** is a component which builds a [[part]].  
If you want to change a look of the **part**, you have to change its **Part Builder**.  
**Part Builders** are stored in the [[skin]] - a prefab with the **Skin component** in the root. 
The **skin** binds **parts** and **part builders** together.    
The **skin** will try to bind a **Part Builder** object with four rotated **parts** if you'll add an **[auto]** prefix in the name.  

=== "Part Builder component"
	![[Pasted image 20211027111532.png]]
	
=== "Part Builder object in the Skin"
	![[Pasted image 20211027111514.png]]

=== "Part"
	![[Pasted image 20211027111614.png]]
	
=== "Binding in the skin"
	![[Pasted image 20211027111833.png]]

- **Own Part** - link to an automatically bound part. This is just a debug information.
- **Combine** - do you want to combine meshes after building? 
- **Space** - select the building space:
	- **Room** - build it into the room space.
	- **Floor** - build it into the floor space.
	- **House** - build it to the house space.

---

**See also:** 
[part](part.md), 
[skin](skin.md), 
[how to add new stuff](how-to-add-new-stuff.md), 
[how to replace models or materials](how-to-replace-models-or-materials.md), 
[how to change room walls](how-to-change-room-walls.md).