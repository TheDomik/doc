# **Add Part Node**
The Add Part node adds a selected part to all input cells.  

![[Pasted image 20210828133934.png]]  
![[Pasted image 20210828134740.png]]  
![[Pasted image 20210828134225.png]]  
![[Pasted image 20210828134652.png]]  

---

## Varieties 
### Add Part 2 Node
This node uses in situations where you want to reduce the number of **Add Part** nodes. Basically this node is equivalent to a chain of *two* **Add Part** nodes.  
![[Pasted image 20210829124313.png]]  
![[Pasted image 20210828134652.png]]  


### Add Part 3 Node
An equivalent to a chain of *three* **Add Part** nodes.  
![[Pasted image 20210829125353.png]]  
![[Pasted image 20210829125421.png]]  

### Add Part 4 Node
An equivalent to a chain of *four* **Add Part** nodes.  
![[Pasted image 20210829132602.png]]  
![[Pasted image 20210829132621.png]]  

### Add Part To Part Node
The Add Part to Part node uses in situations where you want to filter all input cells with specific part and add some part to them. 
- **Target** - part what you want to use as a filter
- **Part** - part what you want to add to filtered cells
- **Mode** - Part adding mode: 
	- **No Rotation** - just add a part to filtered cells
	- **Rotate Only Target** - include all possible rotations of the target part to the filter
	- **Rotate Target And Part** - filter all possible rotations of the target and add relevant rotation offset to the part. 