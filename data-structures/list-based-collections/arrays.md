# Arrays

An array is a container which can hold a fixed number of elements and these elements should be of the same type. Each element in the array has a position within the array and the position is represented by an index. An index is a number associated with the place/position of an element in an array. It is used to identify the element.

Indices in an array start at 0 (zero) and end at $$n-1$$, with $$n$$ being the number of elements in a given array.

![https://www.tutorialspoint.com/data\_structures\_algorithms/array\_data\_structure.htm](<../../.gitbook/assets/image (14).png>)

**Accessing:**&#x20;

If we use an array, items are stored in memory consecutively and we can have direct access to any particular item through the use of its index which means the time complexity of accessing an array is$$O(1)$$.

**Searching:**

If we are a searching for an element in an unsorted array and we assume that the element we are looking for is at the end of the array (in the worst case scenario) the time complexity of this operation will be $$O(n)$$.

**Inserting:**

Inserting elements into an array is $$O(n)$$, making the list grow can be costly and space can be wasted as large amounts of space may be allocated but never used. Insertion into anywhere other than at the end of the array is a heavy operation because it requires us to shift all values from the point of insertion to the end of the array.&#x20;

**Removing:**

Much like inserting elements into an array, removing elements from an array is $$O(n)$$. Removal of any value anywhere other than the very last item is not great as it also requires us to again re-organize the data by shifting all items from the point of removal to the very end of the list.

**Caveat:**

In order to implement a list using arrays, we have to allocate twice as much space than is necessary. The array is then used until it is full. Once the array is full, it is either that every new insertion into the array will fail until an item is removed or the array must be reallocated. As mentioned above, the reallocation process typically involves creating an array approximately twice the size of the original; copying over the old data; and making this the array. Because this whole process of growing an array typically requires us to copy the entire array, it is not something you want to find yourself doing often. **In summary, you do not grow the array a few elements at a time but in large chunks instead.**&#x20;
