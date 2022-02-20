# Notes - Day 5

<a href = "https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/big_oh.html">"Big O: Analysis of Algorithm Efficiency, through “Linear Complexity Growth”"</a>

Big O(oh) notation is used to describe the efficiency of an algorithm or function. This efficiency is evaluated based on 2 factors:

- Running Time (also known as time efficiency / complexity): The amount of time a function needs to complete.
- Memory Space (also known as space efficiency / complexity): The amount of memory resources a function uses to store data and instructions.

In order to analyze these limiting factors, we should consider 4 Key Areas for analysis:

1. Input Size: Input Size refers to the size of the parameter values that are read by the algorithm. It doesn't just refer to number of parameters an algorithm reads, but takes into account the size of each parameter value as well.
    - We will use the letter n to refer to the Input Size value. The higher the n number, the more likely there will be an increase to Running Time and Memory Space.

2. Units of Measurement: In order to quantify the Running Time in our analysis, we will consider Three Measurements of time:
    - The time in milliseconds from the start of a function execution until it ends. Big O won’t be considering this measurement since different machines will have different individual run times.
    - The number of operations that are executed. Think of this as the number of lines of code that are executed from start to finish of a function.
    - The number of “Basic Operations” that are executed. Basic Operation refers to operation that is contributing the most to total time. Usually the most time consuming operation within the inner most loop.
    - In order to quantify Memory Space, consider Four Sources of Memory Usage during function run-time:
    - The amount of space needed to hold the code for the algorithm. This is the number of bytes required to store the characters for your function.
    - The amount of space needed to hold the input data. May just refer to this as Additional Memory Space since not all functions have direct input values.
    - The amount of space needed for the output data.
    - The amount of space needed to hold working space during the calculation. Working Space can be thought of as the creation of variables and reference points as our function performs calculations.

Always be aware that Space Complexity and Time Complexity are measured differently and should be analyzed separately.

3. Orders of Growth: We can describe overall efficiency by using the input size n and measuring the overall Units of Space and Time required for the given input size n. As the value of n grows, the Order of Growth represents the increase in Running Time or Memory Space.
    - Constant Complexity means that no matter what inputs are thrown at our algorithm, it always uses the same amount of time or space.
    - Logarithmic Complexity represents a function that sees a decrease in the rate of complexity growth, the greater our value of n. If an algorithm has Linear Complexity, the size of our inputs ‘n’ will directly determine the amount of Memory Space used and Running Time length. Often used for loops or recursive functions.
    - Linearithmic Complexity is used to describe a growth rate of n by lgn. This represents complexity that grows with n, but also by lgn.

4. Best Case, Worst Case, and Average Case

<a href = "https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/big_oh.html">"Source"</a>

<a href = "https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html">"Linked LIsts"</a>

A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link. There are two types of Linked List - Singly and Doubly.

Terminology:

- *Linked List:* A data structure that contains nodes that links/points to the next node in the list.
- *Singly:* Refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.
- *Doubly:* -Refers to there being two references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.
- *Node:* The individual items/links that live in a linked list. Each node contains the data for each link.
- *Next:* Each node contains a property called Next. This property contains the reference to the next node.
- *Head:* A reference of type Node to the first node in a linked list.
- *Current:* - Reference of type Node to the node that is currently being looked at. When traversing, you create a new Current variable at the Head to guarantee you are starting from the beginning of the linked list.

When traversing a linked list, you are not able to use a foreach or for loop. We depend on the Next value in each node to guide us where the next reference is pointing. The best way to approach a traversal is through the use of a while() loop. This allows us to continually check that the Next node in the list is not null. The Current variable will tell us where exactly in the linked list we are.

Adding 0(1)

Order of operations is extremely important when it comes to working with a Linked List.

Here are the required steps to add a new node with an O(1) efficiency.

- We can then instantiate the new node that we are adding. The values passed in as arguments into the Add() method will define what the value of the Node will be.
- newNode.Next by default is set to null. We want to set newNode.Next property to the same location that the Head node is pointing towards. Because Head is just a reference type, we will be assigning it to the same allocation in memory as the node it is pointing too. In this case, it’s Node1.
- At this point in the program we now “technically” have newNode at the beginning of the linked list, but we are not done yet. We now have to re-assign where Head is pointing too. Since Node1 is no longer the first node in the list, we want to re-assign Head to point at newNode.

Adding a Node O(n)

Adding a node to the middle of a linked list is a bit different than adding to the beginning. This is because we are working with more nodes and must re-allocate to make room for the new node.

- Start with a Singly Linked List
- Now let’s create a new node (node6). We will set the value of node6 to be 16. The Next will be null because we haven’t yet attached it into the linked list.
- Now let’s start the adding. We can do an AddBefore method or an AddAfter. For this documentation, we will do an AddBefore. The AddAfter is extremely similar.

AddBefore:

- Current is pointing to node3.
- node3.Next property is equal to node4.
- Since this is the node we want to insert before, we can now set our node6.Next property also to node4. We do this at the time the node is found to prevent setting node6.Next to a node that may not exist.
- now both node3 and node6 are pointing to the same next node. node6 is not quite fully apart of the linked list.
- Next, we have to adjust node3.Next to point to the newly created node, node6. Since we still have Current pointing to node3 this will be a straightforward transaction. We just simply tell Current to change it’s Next to point to the new node (node6).

The time efficiency of this transaction would be O(n) because we could be inserting the new node, worst case scenario, at the end. With n being the number of nodes possible, we would therefore have O(n) time efficiency.

Space efficiency would stay at an O(1) because, like before, no additional space is being used allocated outside of what is given to us on the input.

Print Out Nodes:

Printing out all of the nodes in a Linked List is very similar to what we did in the Includes() method. This is because we are leveraging our Current node and a while loop to traverse through the existing linked list. Much like in Includes, we are creating a while loop to check and make sure we are not at the end of a linked list. Right before the while loop restarts, we move Current to equal the next node in the list. Once we hit the end, we write out the null pointed to by the last node.

When constructing your code, a few things to keep in mind. When making your Node class, consider requiring a value to be passed in to require that each node has a value. <a href = "https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html">"Source"</a>

<a href = "https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d">"What's a Linked List Anyway pt. 1"</a>

One characteristic of linked lists is that they are linear data structures, which means that there is a sequence and an order to how they are constructed and traversed.

One byte could live somewhere, while the next byte could be stored in another place in memory altogether! Linked lists don’t need to take up a single block of memory; instead, the memory that they use can be scattered throughout.

The fundamental difference between arrays and linked lists is that arrays are static data structures, while linked lists are dynamic data structures.

Dynamic data structure can shrink and grow in memory. It doesn’t need a set amount of memory to be allocated in order to exist, and its size and shape can change, and the amount of memory it needs can change as well.

A linked list is made up of a series of nodes, which are the elements of the list.

The starting point of the list is a reference to the first node, which is referred to as the head. The end of the list isn’t a node, but rather a node that points to null, or an empty value.

All a node is concerned with is the data it contains, and which node its pointer references to — the next node in the list.

This is the very reason why a linked list doesn’t need a contiguous block of memory. Because a single node has the “address” or a reference to the next node.

Singly linked lists are the simplest type of linked list, based solely on the fact that they only go in one direction. There is also what we call a doubly linked list, because there are two references contained within each node: a reference to the next node, as well as the previous node.

A circular linked list is a little odd in that it doesn’t end with a node pointing to a null value. Instead, it has a node that acts as the tail of the list (rather than the conventional head node), and the node after the tail node is the beginning of the list.

<a href = "https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d">"Source"</a>

<a href = "https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996">"What's a Linked List Anyway pt. 2"</a>

Big O Notation is a way of evaluating the performance of an algorithm.

There are two major points to consider when thinking about how an algorithm performs: how much time it requires at runtime given how much time and memory it needs.

One way to think about Big O notation is a way to express the amount of time that a function, action, or algorithm takes to run based on how many elements we pass to that function.

If you look, you'll find that there are a ton of different equations used to define the space and time complexity of an algorithm, and most of them involve an O (referred to as just “O” or sometimes as “order”), and a variable n, where n is the size of the input). As far as linked lists go, however, the two types of Big O equations to remember are O(1) and O(n).

An O(1) function takes constant time, it’ll always take the same amount of time and memory to run our algorithm. An O(n) function is linear, which means that as our input grows, the space and time that we need to run that algorithm grows linearly. A O(n²) function, clearly takes exponentially more time and memory the more elements that you have.

To grow all we really need to do is rearrange our pointers. Inserting an element at the beginning of a linked list is particularly nice and efficient because it takes the same amount of time, no matter how long our list is, which is to say it has a space time complexity that is constant, or O(1).

But inserting an element at the end of a linked list is a different story. The interesting thing here is that the steps you take to actually do the inserting are the exact same. However, there’s an added complexity here: we’re not adding something to the beginning of the list, at the head node. We’re adding something after the last node. We’ll need to traverse through the entire linked list to find it.

A good rule of thumb for remember the characteristics of linked lists is this: A linked list is usually efficient when it comes to adding and removing most elements, but can be very slow to search and find a single element. If you ever find yourself having to do something that requires a lot of traversal, iteration, or quick index-level access, a linked list could be your worst enemy. However, if you find yourself wanting to add a bunch of elements to a list and aren’t worried about finding elements again later, or if you know that you won’t need to traverse through the entirety of the list, a linked list could be your new best friend. <a href = "https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996">"Source"</a>

---
<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">**Back**</a>

---
