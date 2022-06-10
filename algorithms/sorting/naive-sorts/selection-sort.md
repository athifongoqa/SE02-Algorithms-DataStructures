# Selection Sort

The selection sort algorithm works by first making the first element of this unsorted array, the minimum. Thereafter, it moves through each element. It selects the smallest value in the array, and then swaps it with the first value of the array, placing it in the now sorted portion of the array on the left as the new minimum. In each iteration, we make the first element of the unsorted portion the minimum and compare it to the elements which succeed it and place the minimum value of that round of iterations in the sorted portion.&#x20;

**Goal:**

To sort the array in ascending order.

**Termination:**

The loop stops at the end of the array after the final iteration.

**Explanation of the steps:**

* Set min to location 0 (zero)
* Search for the minimum element in the list
* Swap with the value at location min
* Increment min to point to next element
* Repeat until list is sorted

This algorithm is called selection sort because it repeatedly selects the next-smallest element and swaps it into place.

{% embed url="http://cathyatseneca.github.io/DSAnim/web/selection.html" %}

**Time complexities:**

In all three cases, we will have time complexities of $$O(n^2)$$,$$Θ(n^2)$$& $$Ω(n^2)$$. The reason being that in all cases, we need to run two nested loops where the outer loop will call the inner loop $$n-1$$ times and the inner loop will run $$n - i$$ times where $$i$$ is the current iteration of the outer loop.

**Implementation:**

```
def selectionSort(arr):
    
    index_length = range(0, len(arr)-1)
        
    for i in index_length:
        min = i
            
        for j in range(i+1, len(arr)):
            if arr[j] < arr[min]:
                min = j
                    
        if min != i:
            arr[min], arr[i] = arr[i], arr[min]
                
    return arr    
```
