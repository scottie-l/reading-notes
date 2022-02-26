# Notes - Day 10

### <a href = "https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html">"Stacks and Queues."</a>

1. *Stacks:*

A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.

Common terminology for a stack is:

- <u>*Push:*</u> - Nodes or items that are put into the stack are pushed
- <u>*Pop:*</u> - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
- <u>*Top:*</u> - This is the top of the stack.
- <u>*Peek:*</u> - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.
- <u>*IsEmpty:*</u> - returns true when stack is empty otherwise returns false.

Stacks follow these concepts:

- <u>*FILO:*</u> - (First In Last Out): This means that the first item added in the stack will be the last item popped out of the stack.
- <u>*LIFO:*</u> - (Last In First Out): This means that the last item added to the stack will be the first item popped out of the stack.

STACK: Current and before `push`

|`Push ⇨`|||Pop ⇨|
| --- | --- | --- | --- |
|TOP ⇨|`4`|value: "Blue"||
|||next: `3`|
||`3`|value: "Green"|
|||next: `2`|
||`2`|value: "White"|
|||next: `1`|
||`1`|value: "Red"|
|||next: `null`|

Pushing a Node onto a stack will always be an O(1) operation. Let’s walk through the steps:

- First, you should have the Node that you want to add. Here is an example of a Node that we want to add to the stack. `Push ⇨ "Node 5", value: "Grey", next = "Null"`
- Next, you need to assign the next property of Node 5 to reference the same Node that top is referencing: Node 4 `Push ⇨ "Node 5", value: "Grey", next = 4`
- Technically at this point, your new Node is added to your stack, but there is no indication that it is the first Node in the stack. To make this happen, you have to re-assign our reference top to the newly added Node, Node 5. `TOP⇨ = Node 5, value: "Grey", next = 4`
- Here is the pseudocode to push a value onto a stack:

~~~js
ALOGORITHM push(value)
// INPUT <-- value to add, wrapped in Node internally
// OUTPUT <-- none
    node = new Node(value)
    node.next <-- Top
    top <-- Node
~~~

Our New STACK: Current and before `pop`

|Push ⇨|||`Pop ⇨`|
| --- | --- | --- | --- |
|TOP ⇨|`5`|value: "Grey"|
|||next: `4`|
||`4`|value: "Blue"||
|||next: `3`|
||`3`|value: "Green"|
|||next: `2`|
||`2`|value: "White"|
|||next: `1`|
||`1`|value: "Red"|
|||next: `null`|

When conducting a pop, the top Node will be re-assigned to the Node that lives below and the top Node is returned to the user. Typically, you would check `isEmpty` before conducting a pop. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block. Let’s walk through the steps of pop:

- The first step of removing Node 5 from the stack is to create a reference named temp that points to the same Node that top points to. `Temp = TOP⇨ "Node 5", value: "Grey", next = 4`
- Once you have created the new reference type, you now need to re-assign top to the value that the next property is referencing. In our visual, we can see that the next property is pointing to Node 4. We will re-assign top to be Node 4. `TOP⇨ "Node 4", value: "Blue", next = 3`
- We can now remove Node 5 safely without it affecting the rest of the stack. Before we do that though you may want to make sure that you clear out the next property in your current temp reference. This will ensure that no further references to Node 4 are floating around the heap. This will allow our garbage collector to cleanly and safely dispose of the Nodes correctly. `Temp = "Node 5", value: "Grey", next = 4`
- Finally, we return the value of the temp Node that was just popped off. `Return = Temp`
- Here is the pseudocode to push a value onto a stack:

~~~js
ALGORITHM pop()
// INPUT <-- No input
// OUTPUT <-- value of top Node in stack
// EXCEPTION if stack is empty
   Node temp <-- top
   top <-- top.next
   temp.next <-- null
   return temp.value
~~~

`Peek`: When conducting a peek, you will only be inspecting the top Node of the stack. Typically, you would check `isEmpty` before conducting a peek. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.

Here is the pseudocode for a peek:

~~~js
ALGORITHM peek()
// INPUT <-- none
// OUTPUT <-- value of top Node in stack
// EXCEPTION if stack is empty
   return top.value
~~~

We do not re-assign the next property when we peek because we want to keep the reference to the next Node in the stack. This will allow the top to stay the top until we decide to pop.

IsEmpty: Here is the pseudocode for isEmpty:

~~~js
ALGORITHM isEmpty()
// INPUT <-- none
// OUTPUT <-- boolean
return top = NULL
~~~

----
2. *Queues.*

Common terminology for a queue is"

- <u>*Enqueue:*</u> - Nodes or items that are added to the queue.
- <u>*Dequeue:*</u> - Nodes or items that are removed from the queue. If called when the queue is empty an - - exception will be raised.
- <u>*Front:*</u> - This is the front/first Node of the queue.
- <u>/*Rear*</u> - This is the rear/last Node of the queue.
- <u>*Peek*</u> - When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.
- <u>*IsEmpty:*</u> - returns true when queue is empty otherwise returns false.

Queues follow these concepts:

- <u>*FIFO:*</u> - (First In First Out): This means that the first item in the queue will be the first item out of the queue.
- <u>*LILO:*</u> - (Last In Last Out): This means that the last item in the queue will be the last item out of the queue.

Here is what a Queue looks like:

|`Enqueue ⇩`||||`⇧ Dequeue`|
| --- | --- | --- | --- | --- |
|Node:|`4`|`3`|`2`|`1`|
||value: "Blue"|value: "Green"|value: "White"|value: "Red"|
||next: "Null"|next: `4`|next: `3`|next: `2`|
||Rear⇧|||Front⇧|

`Enqueue` is done with an O(1) operation in time because it does not matter how many other items live in the queue (n); it takes the same amount of time to perform the operation. Let’s walk through the process of adding a Node to a queue:

- First, we should change the next property of Node 4 to point to the Node we are adding. In our case with the visual below, we will be re-assigning Node 4’s .next to Node 5. The only way we have access to Node 4 is through our reference rear. Following the rules of reference types, this means that we must change rear.next to Node 5. `"Node 4", value: "Blue", next = 5`
- After we have set the next property, we can re-assign the rear reference to point to Node 5. By doing this, it allows us to keep a reference of where the rear is, and we can continue to enqueue Nodes into the queue as needed. `Rear⇧ = "Node 5", value: "Grey", next = Null`

Here is Our New Queue:

|`Enqueue ⇩`|||||`⇧ Dequeue`|
| --- | --- | --- | --- | --- | --- |
|Node:|`5`|`4`|`3`|`2`|`1`||
||value: "Grey"|value: "Blue"|value: "Green"|value: "White"|value: "Red"||
||next: "Null"|next: `5`|next: `4`|next: `3`|next: `2`||
||Rear⇧||||Front⇧||

Here is the pseudocode for the `enqueue` method:

~~~js
ALGORITHM `enqueue(value)`
// INPUT <-- value to add to queue (will be wrapped in Node internally)
// OUTPUT <-- none
   node = new Node(value)
   rear.next <-- node
   rear <-- node
~~~

When you remove an item from a queue, you use the dequeue action. Typically, you would check `isEmpty` before conducting a dequeue. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.

Let’s walk through the process of removing a Node from a queue.

- The first thing you want to do is create a temporary reference type named temp and have it point to the same Node that front is pointing too. This means that temp will point to Node 1. `Temp = FRONT⇧ "Node 1", value: "Red", next = 2`
- Next, you want to re-assign front to the next value that the Node front is referencing. In our visual, this would be Node 2. `FRONT⇧ "Node 2", value: "White", next = 3`
- Now that we have moved front to the second Node in line, we can next re-assign the next property on the temp Node to null. We do this because we want to make sure that all the proper Nodes clear any unnecessary references for the garbage collector to come in later and clean up. `Temp = "Node 1", value: "Red", next = "Null"`
- Finally, we return the value of the temp Node that was just removed. `return temp`

Here is the pseudocode for the `dequeue` method:

~~~js
ALGORITHM dequeue()
// INPUT <-- none
// OUTPUT <-- value of the removed Node
// EXCEPTION if queue is empty
   Node temp <-- front
   front <-- front.next
   temp.next <-- null
   return temp.value
~~~

`Peek`: When conducting a peek, you will only be inspecting the front Node of the queue. Typically, you want to check isEmpty before conducting a peek. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.

Here is the pseudocode for a `peek`:

~~~js
ALGORITHM peek()
// INPUT <-- none
// OUTPUT <-- value of the front Node in Queue
// EXCEPTION if Queue is empty
   return front.value
~~~

We do not re-assign the next property when we peek because we want to keep the reference to the next Node in the queue. This will allow the front to stay in the front until we decide to dequeue.

Here is the pseudocode for `isEmpty`:

~~~js
ALGORITHM isEmpty()
// INPUT <-- none
// OUTPUT <-- boolean
return front = NULL
~~~

<a href = "https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html">"Source"</a>

----
<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">**Back**</a>

----
