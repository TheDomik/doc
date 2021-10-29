# **Interior**
The **Interior** is a description of the room.  
It answers three questions:

- How should it look like?
- Where should it be?
- That furniture should be there?

![[Pasted image 20210330190849.png]]  

??? question "How to create an interior?"
	To create an **interior** select some folder in the **Project** window -> **Right Mouse Click** -> **Create** -> **Domik** -> **Interior**  
	![[create interior.gif]]  

---

## **Furniture**



This is a list of **placeable objects** that you want to place in the room.  
You can use a [placeable object](placeable-object.md) or a [placeable objects container](placeable-objects-container.md) here.  

![[Pasted image 20211029132258.png]]  

---

## **Skins**

This is a list of **skins** which defines how a room should look like.  
Top items of the list have higher priority than bottom, so you can override bottom **skins** with top **skins**.   
**Interior** **skins** have higher priority than [house generator](house-generator.md) **skins**.

![[Pasted image 20211029132615.png]]  

You can use a [[skin]], [[palette]] or a [palettes random container](palettes-random-container.md) here.  

---

## **Placing Rules**

This panel describes a room that can be used with this **interior**.

![[Pasted image 20211029133359.png]]

- **Max Count Per Floor** - a limit of using this **interior** per floor. **Example:** bathroom. Zero number means that you don't want to use a limit for this **interior**.
- **Prefer Room** - a preferred size for a room:
	- **Small** - small rooms better.
	- **Middle** - middle size rooms better.
	- **Big** - big rooms better.
	- **Random** - you don't care.
- **Parts Limit list** - a list of **parts** which should or shouldn't be it the room.

---

### **Parts Limit list item**
![[Pasted image 20211029142105.png]]



- **Part field** - a **part** that you want to limit.
- **Mode** - a type of limit.
	- **Fixed** - limit a count of this **part** in the room by the concrete number.
	- **Range** - limit a count of this **part** in the room by the range.
	- **At Least One** - this **part** should be at least in one exemplar in the room.
	- **Unacceptable** - This **part** shouldn't be in the room.
	
---

**See Also:** 
[[part]],
[how-to change room walls](how-to-change-room-walls.md),
[house generator](house-generator.md).
