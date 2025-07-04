### 📘 [Linked List Conceptual Q&A](https://docs.google.com/document/d/1mBmbTd2A0r2GYV50GkweULyN-TqKZSmx7UVM4-NX5cs/edit?tab=t.0)

This file contains basic conceptual questions and answers comparing arrays and linked lists in data structure.

---

#### ❓ 1. Why do you think linked-list requires more memory than an array when storing the same number of elements?

**Answer:**  
Let's break down why a linked list requires more memory than an array.  
First of all, a linked list needs a node, which is an object that contains both the value and a reference (or pointer) to the next node. This means it requires two pieces of data: one for the actual value and another to store the memory address of the next node.  
On the other hand, an array only needs one data type to store each value, and the memory locations are managed internally and sequentially.  
So, since a linked list uses more types of data (value + pointer), it ends up using more memory.

-----

#### ❓ 2. Write down Three Limitations of the array which can be solved by the use of Linked List

**Answer:**  
Here listed some limitations of the array which can be solved by the use of linked list:

- **Array Limitation:** Once an array is created, its size is fixed and cannot be changed during runtime.
- **Array Limitation:** An array requires a block of contiguous (sequential) memory, which can be difficult to allocate especially when memory is fragmented.
- **Limited Flexibility:** Arrays have limited flexibility in terms of dynamic operations like inserting, deleting, or resizing. Also, inserting elements in sorted order or in specific positions is complex.

-----

#### ❓ 3. What is the value of Head?

**Answer:**  
Head is the first index (or starting pointer) of a linked list. It stores the memory address of the first node.

-----

#### ❓ 4. What is the value of `?` marked address location?

**Answer:**  
The `?` marked address location refers to the **memory address of the next node** in the linked list.  
If a node has `Next = ?`, then `?` is actually the address of the node that comes immediately after the current one.

For example:  
If a node contains `Value = 10`, `Next = ?`, and the next node is at address `1040`, then `? = 1040`.

-----

#### ❓ 5. What will be the value of `Head->Next->Next->Value`?

**Answer:**  
`Head->Next->Next->Value` means:  
Start from `Head`, move to the next node, then again move to the next node, and finally access the `value` stored there.  
So it returns the **value of the third node** in the linked list.

-----

#### ❓ 6. What will be the value of `Sum` following the pseudocode snippets?

```c
Sum = 0
Temp = Head
While ( Temp -> Next != 1020 ){
    Sum += Temp -> value
    Temp = Temp -> Next
}
Sum -= Temp -> value;
```

**Answer:**
This will cause an **infinite loop** or an **error**, because the condition is checking for a specific memory address 1020.
If none of the **Temp->Next** pointers match **1020**, the loop will never end.
Also, hardcoding memory addresses (like **1020**) is bad practice in real implementations.
Instead, it should check something like **Temp->Next != NULL**.