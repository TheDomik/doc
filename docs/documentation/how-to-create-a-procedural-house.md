# **How to create a procedural house**

There are two ways to create a procedural house.

=== "Drag-and-drop a prefab"

	

	1. Open the **Domik** folder 
	2. Select **House Example prefab** 
	3. Drag-n-Drop it on the scene.
	4. Select it on the scene 
	5. Click **Generate From Random** button in the Inspector.
	
	![[drag-n-drop.gif]]
	
=== "Create as a new gameobject in the scene"

	1. Create new gameobject in the scene.
	2. Add a **House Generator** component to it.
	3. Select a **Regular House** pipeline in the pipeline property in the **House Generator** component.
	4. Set house sizes in the **Base Size** menu.
	5. Add a **Regular Floor** skin to the **House Skins** property.
	6. Add a **Basement** floor, **FLEX Regular Floor** and a **Roof** floors with correct order as it shows below.
	7. Click the **Generate Random** button.

---

You can duplicate it if you want.

1. Select **House Example Prefab** in the **Hierarchy**.
2. Press **Ctrl-D** to duplicate prefab instance in the scene. 
3. Change the position on duplicated house by dragging gizmo handle.
4. Click **Generate Random** button to regenerate it.
5. Repeat.

![[multiple houses.gif]]


---

Click a **Generate Random** button again to randomize look of the house.

![[regen.gif]]