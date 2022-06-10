# Hash Tables

A Hash Table is a data structure which stores data in an associative manner. A Hash Table uses an array as a storage medium and uses a hash function (explained on the next page) which will use a given key to generate a unique hash code which will then be converted to a unique index value to determine where the key's associated value is to be inserted or located from within the array. This hash function is required to return the same hash code for equal keys.

![https://guides.codepath.com/compsci/Hash-Tables](<../../../.gitbook/assets/image (61).png>)

**Searching & Accessing:**

The time complexity of accessing/searching data in a Hash Table is $$O(1)$$, assuming there are no collisions because we pass in the respective key into the hash function and retrieve the index of its value by making use of an array's constant lookup time.

**Insertion & Removal:**&#x20;

To insert an element into a Hash Table, we execute a hash function to generate an index and insert the data value into the array at the given index's position. This whole operation happens within a time complexity of $$O(1)$$, assuming there are no collisions. Much like searching for a data value a Hash Table, removing said data value from it requires us to pass its associative key into the hash function which will point us to the correct index for deletion in a time complexity of $$O(1)$$, assuming there are no collisions.

**Caveat:**

We should be mindful of updating a key that is already present in the Hash Table. Once it is updated, its lookup will no longer work for that key. Instead, if a key needs to be updated, we should remove it, update the key, then re-insert the key into the table.&#x20;

It is also important to note that in the worst case scenario, all operations can result in a time complexity of $$O(n)$$. When a hash table distributes the keys poorly, all the keys may hash to the exact same index in the storage array and any operation would require going through all of the previous entries.

**Applications:**

Hash Tables are used to implement database indexes for fast lookup times for database entries.
