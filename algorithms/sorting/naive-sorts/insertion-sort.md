# Insertion Sort

The insertion sort algorithm works by looking at the array as if it is being filled in. The idea is that the array starts off in the first iteration as if it has only one element in it (the first element). The numbers that are inserted thereafter are then inserted into the sorted sub-array at the correct position. This is continued until all values in the entire array have been properly "inserted".&#x20;

{% embed url="http://cathyatseneca.github.io/DSAnim/web/insertion.html" %}

**Goal:**

To sort the array in ascending order.

**Termination:**

When the loop terminates after the last iteration thus producing the desired result.

**Explanation of the steps:**

* Assign a variable to the first element and place it in the sorted sub-list
* Pick next element
* Compare with all elements in the sorted sub-list
* Shift all the elements in the sorted sub-list that is greater than the value to be sorted
* Insert the value
* Repeat until list is sorted

**Time complexities:**

**Worst Case & Average Case:**

In the average and worst case, the time complexity of Insertion Sort will be$$O(n^2)$$. This is because these cases would require walkthroughs of $$O(n)$$comparisons and shifts nested in $$O(n)$$ iterations.

**Best Case:**

Insertion sort will take minimum time when elements are already sorted and will result in a time complexity $$Ω(n)$$.

**Implementation:**

```
def insertionSort(arr):
    length = range(1, len(arr))
    
    for i in length:
        value_to_sort = arr[i]
        
        while arr[i-1] > value_to_sort and i > 0:
            arr[i], arr[i-1] = arr[i-1], arr[i]
            i = i-1
            
    return arr
```
