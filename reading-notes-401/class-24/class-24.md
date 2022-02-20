# Notes - Day 24

<a href = "https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html">Intro to Hash Tables</a>

**Terminology:**

- *Hash:* - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
- *Buckets:* - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
- *Collisions:* - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

Why do we use them?

  1. Hold unique values
  2. Dictionary
  3. Library

**What is a Hashtable?**

Hashtables are a data structure that utilize key value pairs. This means every `Node` or `Bucket` has both a key, and a value.

The basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value. This is done through what we call a `hash`. A `hash` is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.

Since we are able to `hash` our key and determine the exact location where our value is stored, we can do a lookup in an O(1) time complexity. This is ideal when quick lookups are required.

*Example*

Let’s say we have data of Seattle neighborhood names and their corresponding zip codes.

`["Greenwood:98103", "Downtown:98101", "Alki Beach:98116", "Bainbridge Island:98110", ...]`

Now, we want to be able to search through the data to look up a neighborhood and obtain it’s zip code. We could do this using a for loop that looks through each piece of data one by one until it finds the neighborhood name, then returns the zip code there. This would be an `O(N)` read operation because it requires searching through each piece of data to find the one piece we want.

Arrays actually have fast access. If we know the index of the information we want we can access that information in `O(1)` time. The reason why searching for a piece of data in a collection is `O(N)` isn’t because the array is slow, it’s just that we have to look through all `N` things in the collection.

Hash maps take advantage of an array’s `O(1)` read access. Instead of adding elements to an array from beginning to end, a hash map uses a “hash function” to place each item at a precise index location, based off it’s key.

Basically, the hash function takes a key and returns an integer. We use the integer to determine where the key/value pair should be placed in the array. The hash code is calculated in constant time and writing to an array at one index is `O(1)` so the hash map has `O(1)` access.

The hash code is used again to read something from the hash map. Take the key, run it through the hash code to get a number, use that number to index the array. Calculating the hash code and reading an array at that index is all constant time to the hash map has `O(1)` read access!

## Structure

**Hashing**

Basically, a hash code turns a key into an integer. It’s very important that hash codes are deterministic: their output is determined only by their input. Hash codes should never have randomness to them. The same key should always produce the same hash code.

**Creating a Hash**

A hashtable traditionally is created from an array. I always like the size 1024. this is important for index placement. After you have created your array of the appropriate size, do some sort of logic to turn that “key” into a numeric number value. Here is a possible suggestion:

1. Add or multiply all the ASCII values together.
2. Multiply it by a prime number such as 599.
3. Use modulo to get the remainder of the result, when divided by the total size of the array.
4. Insert into the array at that index.

*Example:*

~~~js
Key = "Cat"
Value = "Josie"

67 + 97 + 116 = 280

280 * 599 = 69648

69648 % 1024 = 16

Key gets placed in index of 16. 
~~~

We now know that our key `Cat` maps to index 16 of the array. We can view into this index and find “Josie”, our value quickly.

Let’s dive a bit deeper into HOW the key/values are stored in the array.

Each index of the array can hold many types of values. The trick is how the values are stored in comparison to efficiency. Each Index of the array contain “buckets”. Each of these “buckets” holds one key/value pair combination. When there is no entry in a specific bucket, the buckets (each index of the array) all start `null`. The hash table starts each bucket empty and overwrites their value once a key generates a hashCode that corresponds with an index.

**Collisions**

A collision occurs when more than one key hashes to the same index in an array. As mentioned earlier, a “perfect hash” will never have any collisions. To put this into perspective, the worst possible hash is one that hashes every single key to the same exact index of an array. The more keys you have hashed to a specific index, the more key/value pair combos you can potentially have.

What would happen if two different keys resolved to be the same index of the array? This is called a collision. The hash map needs to be able to handle two keys resolving to the same index.

If two keys ever ultimately resolved to the same index, then two calls to `.Add(key, val)` with different keys would overwrite each other.

Collisions are solved by changing the initial state of the buckets. Instead of starting them all as `null` we can initialize a `LinkedList` in each one! Now if two keys resolve to the same index in the array then their key/value pairs can be stored as a node in a linked list. Each index in the array is called a “bucket” because it can store multiple key/value pairs.

Since different keys can lead to the same bucket it’s important to store the entire key/value pair in the bucket, not just the value. The key must be stored with the value! If only values were stored in buckets then it would be impossible to determine which value to return when a key led you to a bucket.

This is similar to the original neighborhood names stored in an array with their zip codes shown earlier.

Here’s an actual example of just one bucket in a real hash map. In this example the two different keys `"Pioneer Square"` and `"Alki Beach"` happen to ultimately resolve to the same bucket. When we look at the bucket we see a representation of the Linked List that exists there. Pioneer Square was added first, so it’s at the front of the list. Then there’s Alki Beach as the second element in the linked list. Notice that both of them store the entire key/value pair.

~~~js
hashMap.Add("Pioneer Square", 98104);
hashMap.Add("Alki Beach", 98116);


Bucket 92: [{Pioneer Square: 98104} --> {Alki Beach: 98116}]
~~~

If we didn’t store the key, the bucket would look like this. Accessing `.get("Pioneer Square")` or `.get("Alki Beach")` would hash the keys and still lead to bucket 92, but it would be impossible to tell which of the zip code values there to return.

~~~js
Bucket 92: [{98104} --> {98116}]
~~~

Hash maps do this to store values:

- accept a key
- calculate the hash of the key
- use modulus to convert the hash into an array index
- store the key with the value by appending both to the end of a linked list

Hash maps do this to read value:

- accept a key
- calculate the hash of the key
- use modulus to convert the hash into an array index
- use the array index to access the short LinkedList representing a bucket
- search through the bucket looking for a node with a key/value pair that matches the key you were given

**Hashmap Example:**

*Hash Code Examples*

Consider these examples running Seattle neighborhood names as Strings through two different hash functions.

Notice that although `"Pioneer Square"` and `"Alki Beach"` have different sum hashes they ultimately resolve to the same bucket index. Their hashes modulo `buckets.length` (to turn them into legitimate array indexes) are equal and they ultimately collide.

Calculating hashes and indexes by summing the ascii values of each character:

~~~js
SUM HASHED: Pioneer Square = 1379
SUM HASHED: Alki Beach = 884
SUM HASHED: U District = 955

BUCKET SIZE=99
SUM INDEX: 1379 % 99 = 92
SUM INDEX:  884 % 99 = 92
SUM INDEX:  995 % 99 = 64
~~~

Calculating hashes and indexes by multiplying the ascii values of each character:

~~~js
MULT HASHED: Pioneer Square = 599126016
MULT HASHED: Alki Beach = 1062823936
MULT HASHED: U District = 578867200

BUCKET SIZE=99
MULT INDEX:  599126016 % 99 = 93
MULT INDEX: 1062823936 % 99 = 31
MULT INDEX:  578867200 % 99 = 43
~~~

**Bucket Sizes**

Hash Maps can have any number of buckets. If a hash map has only a few buckets it will be densely full and have many collisions. If a hash map has more buckets it will be more sparsely populated, there will be less collisions, but there may be a lot of extra empty space.

It’s possible to compute the “load factor” of a hash table. The load factor tells us something about how full the hash table is. A hash table can start with only a few buckets, calculate it’s own load factor, recognize when it gets too full and automatically grow and add more buckets to itself to accommodate more data.

*Recognize:* calculating load factors and choosing the optimal number of buckets, and determining the best hash functions is not within the scope of this class. This class intends to introduce you to what a hash table is, how it’s implemented, what hash codes are, how to handle collisions and how to reason generally about what it means for a hash table to be more empty or more full. This class does not intend to calculate theoretical optimal performance limits for how to best balance a Hash Table.

Here’s what the same information looks like in two different hash tables. The first hash table only has 7 buckets. The second has 100 buckets. Notice that even though the second hash table has 100 buckets there are still some collisions. Collisions are ok! We just don’t want every key to hash to the exact same index. That would be literally the worst!

7 buckets:

~~~js
Bucket 0: [{Renton: 98055} --> {Capital Hill: 98102} --> {Greenwood: 98103} --> {Greenlake: 98103} --> {Pioneer Square: 98104} --> {University District: 98105} --> {Columbia City: 98118}]
Bucket 1: [{Bellevue: 98005} --> {Seattle: 98101}]
Bucket 2: [{Mercer Island: 98040} --> {Alki Beach: 98116} --> {Northgate: 98125}]
Bucket 3: [{Downtown: 98101} --> {Laurelhurst: 98105} --> {Bainbridge Island: 98110} --> {Magnolia: 98199}]
Bucket 4: [{Kirkland: 98033} --> {Lynnwood: 98037} --> {Ballard: 98107} --> {Queen Anne: 98109} --> {West Seattle: 98116}]
Bucket 5: [{International District: 98104} --> {Mount Baker:98144}]
Bucket 6: [{Redmond: 98052} --> {Freemont: 98103} --> {South Lake Union: 98109} --> {Madrona: 98110} --> {Belltown: 98121}]
~~~

100 buckets:

~~~js
Bucket 0: []
Bucket 11: []
Bucket 12: [{South Lake Union: 98109}]
Bucket 13: [{Madrona: 98110}]
Bucket 14: []
Bucket 15: []
Bucket 16: [{Magnolia:98199}]
Bucket 17: []
Bucket 18: []
Bucket 19: [{Greenlake:98103}]
Bucket 20: [{Redmond:98052}]
Bucket 21: []
Bucket 23: []
Bucket 24: [{Kirkland:98033}]
Bucket 25: []
Bucket 27: []
Bucket 28: [{Bellevue:98005}]
Bucket 29: [{Seattle:98101}]
Bucket 30: []
Bucket 35: []
Bucket 36: [{Renton:98055}]
Bucket 37: [{Queen Anne:98109}]
Bucket 38: [{Capital Hill:98102}]
Bucket 39: []
Bucket 40: [{Freemont:98103}]
Bucket 41: []
Bucket 46: []
Bucket 47: [{Greenwood:98103}  --> {Belltown:98121}]
Bucket 48: []
Bucket 49: [{Northgate:98125}]
Bucket 50: [{Bainbridge Island:98110}]
Bucket 51: []
Bucket 52: []
Bucket 53: [{Mercer Island:98040}]
Bucket 54: []
Bucket 57: []
Bucket 58: [{Mount Baker:98144}]
Bucket 59: []
Bucket 60: [{International District:98104}]
Bucket 61: []
Bucket 64: []
Bucket 65: [{Columbia City:98118}]
Bucket 66: [{Lynnwood:98037}]
Bucket 67: []
Bucket 71: []
Bucket 72: [{Downtown:98101}]
Bucket 73: []
Bucket 78: []
Bucket 79: [{University District:98105}]
Bucket 80: []
Bucket 83: []
Bucket 84: [{West Seattle:98116}]
Bucket 85: []
Bucket 89: []
Bucket 90: [{Laurelhurst:98105}]
Bucket 91: []
Bucket 92: [{Pioneer Square: 98104} --> {Alki Beach:98116}]
Bucket 93: []
Bucket 95: []
Bucket 96: [{Ballard:98107}]
Bucket 97: []
Bucket 98: []
~~~

**Internal Methods**

*Add()*

When adding a new key/value pair to a hashtable:

1. send the key to the GetHash method.
2. Once you determine the index of where it should be placed, go to that index
3. Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
4. If something does exist, add the new key/value pair to the data structure within that bucket.

*Find()*

The `Find` takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.

*Contains()*

The `Contains` method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the `GetHash` and check the hashtable if the key exists in the table given the index returned.

*GetHash()*

The `GetHash` will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed. <a href = "https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html">"Source"</a>

<a href = "https://www.youtube.com/watch?v=MfhjkfocRR0">What is a Hash table? - video</a>

<a href = "https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/">Basics of Hash Tables</a>

Hashing is a technique that is used to uniquely identify a specific object from a group of similar objects. Some examples of how hashing is used in our lives include:

- In universities, each student is assigned a unique roll number that can be used to retrieve information about them.
- In libraries, each book is assigned a unique number that can be used to determine information about the book, such as its exact position in the library or the users it has been issued to etc.
In both these examples the students and books were hashed to a unique number.

Hashing is implemented in two steps:

1. An element is converted into an integer by using a hash function. This element can be used as an index to store the original element, which falls into the hash table.
2. The element is stored in the hash table where it can be quickly retrieved using hashed key.

hash = hashfunc(key)
index = hash % array_size

Hash function

A hash function is any function that can be used to map a data set of an arbitrary size to a data set of a fixed size, which falls into the hash table. The values returned by a hash function are called hash values, hash codes, hash sums, or simply hashes.

Hash table

A hash table is a data structure that is used to store keys/value pairs. It uses a hash function to compute an index into an array in which an element will be inserted or searched. By using a good hash function, hashing can work well. Under reasonable assumptions, the average time required to search for an element in a hash table is O(1).

Collision resolution techniques

Separate chaining (open hashing)

Separate chaining is one of the most commonly used collision resolution techniques. It is usually implemented using linked lists. In separate chaining, each element of the hash table is a linked list. To store an element in the hash table you must insert it into a specific linked list. If there is any collision (i.e. two different elements have same hash value) then store both the elements in the same linked list.

Linear probing (open addressing or closed hashing)

In open addressing, instead of in linked lists, all entry records are stored in the array itself. When a new entry has to be inserted, the hash index of the hashed value is computed and then the array is examined (starting with the hashed index). If the slot at the hashed index is unoccupied, then the entry record is inserted in slot at the hashed index else it proceeds in some probe sequence until it finds an unoccupied slot.

Quadratic Probing

Quadratic probing is similar to linear probing and the only difference is the interval between successive probes or entry slots. Here, when the slot at a hashed index for an entry record is already occupied, you must start traversing until you find an unoccupied slot. The interval between slots is computed by adding the successive value of an arbitrary polynomial in the original hashed index.

Double hashing

Double hashing is similar to linear probing and the only difference is the interval between successive probes. Here, the interval between probes is computed by using two hash functions.

<a href = "https://en.wikipedia.org/wiki/Hash_table">Hash Table Wiki</a>

In computing, a hash table (hash map) is a data structure that implements an associative array abstract data type, a structure that can map keys to values. A hash table uses a hash function to compute an index, also called a hash code, into an array of buckets or slots, from which the desired value can be found. During lookup, the key is hashed and the resulting hash indicates where the corresponding value is stored.

Ideally, the hash function will assign each key to a unique bucket, but most hash table designs employ an imperfect hash function, which might cause hash collisions where the hash function generates the same index for more than one key. Such collisions are typically accommodated in some way.

In a well-dimensioned hash table, the average cost (number of instructions) for each lookup is independent of the number of elements stored in the table. Many hash table designs also allow arbitrary insertions and deletions of key–value pairs, at constant average cost per operation.

In many situations, hash tables turn out to be on average more efficient than search trees or any other table lookup structure. For this reason, they are widely used in many kinds of computer software, particularly for associative arrays, database indexing, caches, and sets. <a href = "https://en.wikipedia.org/wiki/Hash_table">"Source"</a>

---
<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">Back</a>

---
