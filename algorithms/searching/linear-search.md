# Linear Search

Linear search is a very simple search algorithm. In this type of search, a sequential search is made over all items in an array one by one. Every item is checked and if a match is found then that item's index is returned, otherwise the search continues until the end of the data collection. If it found that the element is not in the array, the algorithm returns $$-1$$.

**Goal:**

Our task is to find and return the index of our target element.&#x20;

**Termination:**

Either when the target element has been found and the algorithm returns its index or when our algorithm returns $$-1$$ , in which case we know that the target element is not present in the array.

**Explanation of the steps:**

* First, we pass in a target element to be searched for
* Next, we compare the target to the first element in the array
  * If they're equal, we return the index of the first element
  * If they're not equal, we repeat our comparisons with the following elements
* If the target element is not in the array, we return $$-1$$ which indicates that the target is not present

**Time complexities:**

**Worst Case:**

In the worst case, the target element could be the last element in the array, in which case we would have to go through every element in the array, resulting in a time complexity of $$O(n)$$.

**Average Case:**

In the average case, the target element would be exactly in the middle of the array, resulting in a time complexity of $$Θ(\frac{n}{2})$$$$\approx$$ $$Θ(n)$$.

**Best Case:**

In the best case, the target we are searching for is the first element we access, which would result in a time complexity of$$Ω(1)$$.

**Implementation:**

```
def linearSearch(arr, target):
    length = len(arr)-1
    
    for i in range(0, length):
        if arr[i] == target:
            return i
    return -1
```
