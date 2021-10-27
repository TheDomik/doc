# **Skin**

The **Skin** is a bridge between [[part]]s and theirs in-game representations.   
From the **Domik** perspective, the house is a structured collection of **parts**, so it has to convert these **parts** into real **game objects**.  
And the **Skin** helps the **Domik** to understand how **parts** should look like.  

![[Pasted image 20211027131342.png]]  

**The Skin** is a prefab with a **Skin component** and a bunch of child **game objects** with [Part Builder](part-builder.md) components.  
It also contains a list of bindings between **parts** and **part builders**.  

## **Settings**
![[Pasted image 20211027130643.png]]  

- **Cell Width** - width and length sizes of the cell. Just write a floor mesh width here (in meters).
- **Cell Height** - height of the cell. Just write a wall mesh height here (in meters).

## **Binding**
Binding list is a list of binding between **part** and **part builders**.  
![[Pasted image 20211027130623.png]]  

- **Create Parts for unbound?** - set it true if you want to create new **parts** for unbound **part builders** in the process of binding update. 
- **Path field** - where you want to create new parts?
- **Change Folder button** - click to change a folder for new **parts**.
- **Update Binding button** - click it to update a list of bindings.
- **Binds list** - a list of binding between **parts** and **part builders**.

### **Binds list element**
![[Pasted image 20211027132341.png]]  

- **Part Builder field** - a **part builder** for the **part**.
- **Part Builder** - a **part** that you want to build by this **part builder**.
- **Number field** - a rotation offset after building.

---

**See also:** 
[how to add new stuff](how-to-add-new-stuff.md),
[part](part.md),
[part builder](part-builder.md),
[house generator](house-generator.md).


