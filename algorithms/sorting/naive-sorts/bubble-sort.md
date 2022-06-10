# Bubble Sort

A bubble sort is a naïve approach. It works by going through elements in the array, side-by-side, and switches them when the element on the left is greater than the element on the right and leaves them if they are in order. Eventually, the highest value makes it to the end of the list. We repeat this process and each round, the biggest bubbles to the end of the unsorted subarray/beginning of the sorted subarray.&#x20;

**Goal:**

To sort the array in ascending order.

**Termination:**

When `sorted` is returned as `True`.

**Explanation of the steps:**

* Compare consecutive items. If the left item is larger than the right item, swap them. If not, move on such that the previous right item becomes the new left item. Repeat this process.&#x20;
* The highest number bubbles all the way to the end of the unsorted subarray/beginning of the sorted subarray after each iteration.

{% embed url="http://cathyatseneca.github.io/DSAnim/web/bubble.html" %}

**Time complexities:**

**Worst & Average Case:**

In the average and worst case, the time complexity of Bubble Sort will be$$Θ=O(n^2)$$. This is because these cases would require walkthroughs of $$Θ=O(n)$$comparisons and swaps nested in $$Θ=O(n)$$ iterations.&#x20;

**Best Case:**

In the best case, we will get a time complexity of$$Ω(n)$$. In this case, we have an array that is already sorted in ascending order and will only require us to perform an iteration of comparisons once.&#x20;

**Implementation:**

```
def bubble(arr):

    length = len(arr)-1
    sorted = False

    while not sorted:
        sorted = True
        for i in range(0, length):
            if arr[i] > arr[i+1]:
                sorted = False
                arr[i], arr[i+1] = arr[i+1], arr[i]

    return arr
```
