# **Override**

![[Pasted image 20211015145358.png]]


This node overrides cells **A** with cells **B**.  
Overriding process will replace **A** cells with **B** cells with the same position.    
Most often used in situations where you have filtered cells to a separate flow, changed them, and now want to apply the changes to the main flow.  

**Inputs:**  

- **A** - cells flow which you want to override
- **B** - cells that will override 

**Outputs:**  

- **Out** - overriding result  

<br />

--------


# Examples
Input is a house that has been completed.  

![[default cells.png]]
![[Pasted image 20210922162630.png]]

Let's remove windows from yellow walls by the **Find and Replace** node.  

![[Pasted image 20210929150842.png]]
![[Pasted image 20210929150919.png]]














Now we can apply changes to the main flow by the **Override** node.  
![[Pasted image 20210929150818.png]]
![[Pasted image 20210929150901.png]]



#### Interesting Case

In this example we will see an interesting point of cells overriding. To do this, we must shift the top floor up.  
Let's filter roof cells by the **Flat Roof Places** node.  
![[Pasted image 20210929131224.png]]
![[Pasted image 20210929131644.png]]
![[Pasted image 20210929131715.png]]

Now let's shift it up by the **Shift** node.  
![[Pasted image 20210929131811.png]]
![[Pasted image 20210929131831.png]]

Now let's apply changes by the **overriding** node.  

![[Pasted image 20210929131951.png]]
![[Pasted image 20210929132019.png]]

Very strange result!   
It looks like, instead of moving, we just copied and pasted the top floor. The override node works pretty similar to the **Merge Node** but with one exception - instead of merging overlapped cells it just replace it with new. In this example, there is no overlapped cells, so top floor cells just added to the house as a bunch of new cells.  

How to solve it? Just exclude a filtered floor!  

![[Pasted image 20210929133534.png]]
![[Pasted image 20210929133550.png]]
