# **How to create a Preview System**

**The Preview** system provides a rendering of **The Domik** configuration files.   
**Read More:** [preview system](preview-system.md).  
This tutorial will show you how to create an instance of this system, but you can just drag'n'drop a preconfigured prefab into the scene.  

---

You have to create an empty **GameObject** in the scene and add the **Preview** component to it to create an instance of the **Preview** system.  

![[create preview gameobject.gif]]  

Add these **GameObjects** as child:  

- **Placeable Object**
- **Place**
- **Part**
- **Mask**

![[add base childs.gif]]  

Add these **GameObjects** for the **Placeable Object** as child:

- **Env**
- **Add**
- **Remove**
- **Place or Mask**
- **Part**
- **Other**

![[add po childs.gif]]  

Add **Mesh Filter** and **Mesh Renderer** components to all child except the **Other** GameObject.  

![[add mesh filters and renderers.gif]]  

Set links of **Placeable Object** child to the **Preview** component.  

![[set PO links V2.gif]]

Set links to other child to the **Preview **component.  
![[set base links.gif]]  

Set the base size of the **skin**.  
![[set base size.gif]]  

Move objects apart  
![[change positions of previews.gif]]   

Now we have to add materials.  

![[preview mats in folder.png]]  

=== "Accessible"
	![[accessible.png]]
	
=== "Inaccessible"
	![[Inaccessible.png]]
	
=== "Place"
	![[place material.png]]

=== "Add"
	![[Add material.png]]
	
=== "Remove"
	![[remove material.png]]
	
=== "Environment"
	![[Environment material.png]]

![[placing mats.gif]]  

Final step - setting up **skins**.  

![[placing skins.gif]]  

Checkout the result.  

![[checking out the result.gif]]  

