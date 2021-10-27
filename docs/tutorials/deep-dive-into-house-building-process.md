# **Deep dive into house building process**

The process of house generation works in three steps: 

1. Generating of **house cells**
2. Extracting a **house build data** from **cells**
3. Building a house from an extracted **house build data**
	
## **1. Generating house cells**.

![[Pipeline advanced.png]]

This step provides by the **Pipeline** - a visual scripting system. From the **Pipeline** perspective there is no 3D meshes, materials, textures etc. The Pipeline works with an abstract idea of parts of the house. And the name of this abstract thing is... **The Part**! Pretty obvious :D



----------

### **That is the Part?**

![[Pasted image 20210329181311.png]]

The **part** is a **scriptable object** with name and references to 3 other parts with rotations by **90**, **180** and **270** degrees.  
Some **parts** have no rotations (example: floor, ceiling, round table...) so rotated **parts** references will be empty and that's fine.  

??? Abstract "Part without rotations"
	![[Pasted image 20210329181537.png]]

The most important aspect of the **part** is its **name**. The part's name is all that the **Pipeline** should know to start working with it. You can even have two **parts** with different **GUID** but with the same name and the **Pipeline** will think that they are equals.

---------

The Pipeline has only one target - create cells. 

--------

### **That are Cells?**

**Cells** is an abstract representation of house in the code.   
To understand the conception, just image a house as a 3D grid of cells.  

=== "(╮°-°)╮┳━━┳"
	![[Снимок экрана 2021-03-29 182815.jpg]]
	
=== "( ╯°□°)╯ ┻━━┻"
	![[Снимок экрана 2021-03-29 182512.jpg]]

Each cell contains a floor, ceiling, walls and something else. 
Floor, ceiling and walls are **parts**.
So yeah, cells is just a 3D grid of parts lists. 


??? Abstract "Representation in code"

	=== "Cells"
    	![[Pasted image 20210329190104.png]]


	=== "Cell"
    	![[Pasted image 20210329190248.png]]

-------

In the **pipeline** you create cells, modify them, remove, merge and so on.
And in the end you return the result in the [[end]] node. 
Created **cells** comes to the second step of the generation - extracting a house build data from cells.

## **2. Extracting a house build data from cells**.
The **Build Data Extractor** transforms **cells** from an abstract representation of house to the house building instruction.  
It sorts **cells** to floors and rooms and finds **part's builder** for all **cell's parts**.  
**Part Builders** are stored in **skins**, so the **Build Data Extractor** asks them if they have something to build some **part**.  

!!! note ""
	If there is no **Part Builder** for some **part**, this **part** will be ignored during house building.

The priority of **skins** asking from highest to lowest:

1. Skins Layer
2. Interior Skins
3. House Skins

=== "Skins Layer"
	![[Pasted image 20211025182319.png]]

=== "Interior Skins"
	![[Pasted image 20210329185529.png]]	
		
=== "House  Skins"
	![[Pasted image 20210329185651.png]]

!!! note ""
	You can change a look of the room by changing **interior skins** because they have higher priority than **house skins**.  

!!! note ""
	The **Skins Layer** has been created for special cases when you want to change a look of some **cells** filtered by special rules in the **Pipeline**.  

So in the result it returns a structured collection of **Part Builders** - a **House Build Data**. 


??? Abstract "Representation in code"

	=== "Floors"	
		![[Снимок экрана 2021-03-29 195441.jpg]]

	=== "Floor"
    	![[Снимок экрана 2021-03-29 195559.jpg]]
		
	=== "Room"
    	![[Снимок экрана 2021-03-29 195702.jpg]]
		
	=== "Cell"
    	![[Снимок экрана 2021-03-29 195836.jpg]]





## **3. Building of the house by the house build data.**

The **House Builder** takes a house build data and just build it!   
It's more complicated, actually, but there is no reason to dive so deep.  

## **But why so complicated?**
Well, there is only one reason - flexibility.  If you are a programmer, you may know the conception of model-view splitting. The **Part** is a model and the **Part Builder** is a view.  **Part** is an abstract idea of something, and the **Part Builder** builds a look of it. Thanks to this separation, we can redefine how a cell should look right on the fly.   

For example, you created some **pipeline** which generates a simple village house. And you have a regular village where you want to place it. But then you want to add a village which was corrupted by chaos, with lakes of blood, rusted chains and so on. But you have this innocent, vibrant, happy house! That's not that you want. Thanks to this separation, you just need to edit **skins** to change a view of house. You don't need to touch the **Pipeline** at all. And that's wonderful.