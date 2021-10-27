# **House Generator**


The **House Generator** component is an entry point to start generation of the house.  

This component provides a setting and construction of the house, and it's designed as a standalone component without any references to editor, so you can just duplicate it, wrap it to a prefab or doing something else.  

![[Pasted image 20210814115724.png]]


**Read More:** [how to create a procedural house](how-to-create-a-procedural-house.md).

---

## **Generate section**

![[b32819f4dfdc71e12ee5da5a8454e483.png]]  

- **Generate Random** - click it to generate a house with a random **seed**.
- **Seed** - a **seed** number which uses to generate a house. [Read More](https://en.wikipedia.org/wiki/Random_seed).
- **Generate** - click it to generate a house from the current **seed** number. Pretty useful to regenerate a house after some changes to see a difference.                    
- **Pipeline** - a reference to the Pipeline Node Graph asset. If you want to change rules of generation you, have to change it.
- **Combining Mode** - defines how meshes of the house should be combined:

	- **Realtime**  - Fast. Vertices welding and normals recalculation are disabled, so expect some artefacts on seams between flat meshes (walls, floor, ceiling etc.). The backed lighting also will be broken. Good choice for rogue-like games or to fast check some changes, btw.                                          
	- **Baked** - very slow but artefacts free. Good choice for final creating of the house. Can be used in realtime too, but it can be too slow for it. 
  
---


## **Base Size section**
This panel defines the target size of the house. 

![[Pasted image 20211026155218.png]]  

- **Width** - target width of the house.
- **Length** - target length of the house.
- **Floors** - target floors count.  

You can select between two size modes: **const** and **rand**.

- **Const** - constant size.
- **Rand** - random size.

??? note "Why the final size may differ than the target size?"
	These values not using directly, but send to the **Pipeline**, so the final size of the house depends on the **Pipeline** algorithm.  

**Read More:** [how to change a house size](how-to-change-a-house-size.md).

---



## **House Skins section**

![[Pasted image 20210105135701.png]]  

This is a list of base house skins.   
You can think about these skins as about skins by default.  

Read More: [facades workflow](facades-workflow.md), [[skin]].

---

## **Floors section**
**Floors** - is a description of floors that you expect to see.

![[Pasted image 20211026160316.png]]

**Read More:** [how to change house floors](how-to-change-house-floors.md).






