# **How to replace models or materials**

If you want to change some part of the house, you have to change its **Part Builder** in the **Skin**.   
**Skin** is a container of objects with **Part Builder** components, which are visual representations of parts of the house.  
**Read more:** [[skin]], [part builder](part-builder.md).  

Usually the house generator uses two groups of skins:

- **House skins** - contains part builders for **facades**, **roof** and so on.
- **Interior skins** - contains part builders for rooms objects: **internal walls**, **furniture**, **ceiling**, **floor**, etc.

!!! note ""
	**House skins** contain default look of objects too.   
	If there is no **interior** for the room, but this room contains a chair, the chair will be constructed by the **Part Builder** from some **House skin**.  
	The same if no one **interior skin** contains a **Part Builder** for this **Part**.  
	If **house skins** and **interior skins** don't contain a **Part Builder** for this **Part**, it'll not be builded at all.

To change a look of the room, you have to change **skins** of an **Interior** that has been applied to this room.    
If there is no **Interior** for this room, you can find this skin in the **House skins list**.  
To change some basic part of the house like a facade or roof, you can do it by changing some of **House skins**.

=== "Interior skins list"
	![[Pasted image 20211021160912.png]]  
	![[Pasted image 20211021160949.png]]
	
=== "House Generator skins list"
	![[Pasted image 20211021161220.png]]

**Read more:** [how the domik builds a house](how-the-domik-builds-a-house.md)

<br />

---

## **Example of changing of sofa by replacing its model**  
It this example, we'll change a sofa of the **Living Room**.   
To do it we have to find and change a skin which contains a **Part Builder** of the sofa.  

!!! note
	You can change a view of an object just for one **Interior**, and all rooms with this **Interior** will have this new look, but other rooms will not.   
	To change a look of some object for all rooms, you should change it in all **skins** with this **part** of the house.




1. Open a **Furniture Origin** Skin
2. Select **[auto] Chilling Section Small**
3. Remove sofa models.
4. Add new model as a child of the **[auto] Chilling Section Small** game object.
5. Fix the position.
6. Close a prefab workspace.
7. Re-generate the house .

![[change_sofa.gif]]

## **Example of changing of sofa by overriding its skin**

Another interesting way to replace something is skins overriding. 

To find out that does it mean, let's select some interior.
![[Pasted image 20210709114829.png]]

Take a closer look at the **Skins section**. It's a list of **skins** for this **interior**.  
Order of **skins** is important, top **skins** have higher priority than down, so you can create a new **skin**, add sofa to it and place it in the top of skins list. In the result, this sofa will be overridden by new.

1. Create a prefab.
2. Add a **Skin** component to this prefab.
3. Open this prefab.
4. Create an empty **GameObject**.
5. Name it exactly as object that you want to replace.
6. Add a **Part Builder** component to this object.
7. Reset it's position.
8. Place new model as a child of this **GameObject**.
9. Fix the position
10. Click an **Update Binding** button in the **Skin** component in the prefab root.
11. Close a prefab workspace and select an **interior**.
12. Add this **skin** in the top of the skins list.
13. Regenerate the house.

![[change sofa by overriding.gif]]