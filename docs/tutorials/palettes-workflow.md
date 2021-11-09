# **Palettes workflow**

**The Palette** - is a tool to randomize a look of house objects.

We'll create two **palettes** for a facade in this tutorial: dark and light, and then we'll use them to create a [palettes random container](palettes-random-container.md).
To create a **palette** you have to right click on some folder -> **Create** -> **Domik** -> **Palette**  

![[create palette.gif]]  

Now we have to change a **layout** of **windows** to make work comfortable.    
We need **two locked inspectors**, one for the **house generator** to regenerate a house without selecting it in the hierarchy, and the second for **palette** to make changes without a risk of closing it accidentally.  

![[change windows layout.gif]]  

Now we have to add this **palette** in top of the **skins list** in the [house generator](house-generator.md)  to see the result of **palette** changes.

![[add this palette to the house.gif]]  


The facade of the house is split to five groups:

- Regular facade walls
- Thin facade walls
- Thick facade walls
- Plinth
- Columns

=== "Regular Walls"
	![[regular facade walls.png]]  
	
=== "Thin Walls"
	![[thin facade walls.png]]  
	
=== "Thick Walls"
	![[thick walls.png]]  
	
=== "Plinth"
	![[plinth.png]]  
	
=== "Columns"
	![[columns.png]]  


Now let's add **skins** for regular walls of the house.  
This is a dark **palette**, so we have to select dark **skins**.  

![[creating of the random group for regular walls.gif]]

Now we'll select **skins** which looks good enough.  
We have to divide a list of **skins** with an empty element, and then group suitable **skins** under it.  

=== "Skins list"
	![[just skins.png]]
	
=== "Skins to check"
	![[skins to check.png]]
	
=== "Divider"
	![[divider.png]]

=== "Suitable skins"
	![[checked skins.png]]  
	
!!! note ""
	Don't forget to set the **Debug** checkbox to **true** to use the first element in the **skins** list, otherwise a random **skin** will be used.

![[filling up regular walls group.gif]]


Now let's check the result.

![[checkout regualr walls.gif]]


Now we have to randomize facade thin walls. 
Create new **skins random group** and fill it with thin facade **skins**.

![[thin walls.gif]]  
 
 Check the result.

![[chechout thin walls.gif]]  

Now let's do thick walls.

![[thick walls.gif]]

And check the result.

![[final checkout dark.gif]]

Next, let's do the same for the light facade group. 

![[palette light creation and setting up FASTER V2.gif]]

Checkout the result.

![[light final checkout.gif]]

Final step - create a [[palettes random container]] to random select one of two palettes.



![[random palette.gif]] 















