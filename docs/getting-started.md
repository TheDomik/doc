# **Getting Started**

**This is a Domik** - a tool for houses creation.  

It uses a visual scripting system to determine a logic of generation and designed to work with modular building systems. 
## **Highlights**
- Generation of room **interiors** with **furniture**.
- Powerful visual scripting system - [The Pipeline](pipeline.md).
- [Supports of third party assets.](how-to-replace-models-or-materials.md)
- **Seed** number based generation, feel free to integrate it with your own procedural worlds.
- Supports of **all types of gameobjects**, so you can place something like a spawn-point right in a house. [Just use a furniture system](how-to-add-new-stuff.md).
- **In-Editor** Generation.
- **Runtime** Generation.
- **Multiple floors**.
- **Stairs**.
- **Mesh combine system** is built-in.
- **2D** Assets support (example is not included yet).
- **Mobile**, **Consoles**, **WebGL** and **PC** are supported.
- **HDRP**, **URP** and **Built-in** scriptable pipeline are supported.

---

## Tutorials
- [how to create a procedural house](how-to-create-a-procedural-house.md)
- [how to change a house size](how-to-change-a-house-size.md)
- [how to change house floors](how-to-change-house-floors.md)
- [how the domik builds a house](how-the-domik-builds-a-house.md)
- [how to change room walls](how-to-change-room-walls.md)
- [how to replace models or materials](how-to-replace-models-or-materials.md)
- [how to add new stuff](how-to-add-new-stuff.md)
- [what is a part builder space](what-is-a-part-builder-space.md)
- [how to create and use a placeable object](how-to-create-and-use-a-placeable-object.md)
- [how to create a place](how-to-create-a-place.md)
- [facades workflow](facades-workflow.md)
- [how to create a preview system](how-to-create-a-preview-system.md)
- [how to create and use the pipeline](how-to-create-and-use-the-pipeline.md)
- [deep dive into house building process](deep-dive-into-house-building-process.md)

---

## Main Concepts
- [house generator](house-generator.md)
- [preview system](preview-system.md)
- [[part]]
- [part builder](part-builder.md)
- [[skin]]
- [[palette]]
- [palettes random container](palettes-random-container.md)
- [[place]]
- [[mask]]
- [placeable object](placeable-object.md)
- [placeable objects container](placeable-objects-container.md)
- [[floor]]
- [[interior]]
- [floor tag](floor-tag.md)
- [[pipeline]]

---

## Pipeline Nodes

- Action:
	- [extract positions](extract-positions.md)
	- [find and replace](find-and-replace.md)
	- [[shift]]
- Add:
	- [add part](add-part.md)
- Filter:
	- [filter by mask](filter-by-mask.md)
	- [filter by positions](filter-by-positions.md)
	- [filter by floor tag](filter-by-floor-tag.md)
	- [filter floor](filter-floor.md)
	- [filter internal doors places](filter-internal-doors-places.md)
	- [filter intersections](filter-intersections.md)
	- [filter neighbor cells](filter-neighbor-cells.md)
	- [filter random cells](filter-random-cells.md)
	- [filter random input](filter-random-input.md)
	- [filter with part](filter-with-part.md)
	- [filter with parts](filter-with-parts.md)
	- [filter without part](filter-without-part.md)
- Flow:
	- [[exclude]]
	- [[merge]]
	- [[override]]
	- [[shuffle]]
- Interiors:
	- [calculate room interiors](calculate-room-interiors.md)
	- [place furniture](place-furniture.md)
	- [return interiors](return-interiors.md)
	- [split into rooms](split-into-rooms.md)
- Main:
	- [[end]]
	- [[start]]
- Place:
	- [place part by mask for all rotations](place-part-by-mask-for-all-rotations.md)
	- [place placeable object forced](place-placeable-object-forced.md)
	- [place placeable object](place-placeable-object.md)
	- [place stairs](place-stairs.md)
- Remove:
	- [apply parts removing](apply-parts-removing.md)
	- [remove part](remove-part.md)
	- [remove part later](remove-part-later.md)
- Skins:
	- [create skins layer](create-skins-layer.md)
	- [override skins layer](override-skins-layer.md)
	- [return skins layer](return-skins-layer.md)

