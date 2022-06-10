# Quick Sort

Quick Sort is another algorithm which falls under the class of Divide and Conquer algorithms. This sort is fast and does not have the extra memory requirements needed for Merge Sort. On average its run time is $$O(n log n)$$ but it does have a worst case run time of $$O(n^2)$$.&#x20;

In the original unsorted array, we pick a pivot and then partition the rest of the array into two distinct groups. We place elements less than the pivot to the left of it and elements greater than it to the right of it. We then repeat this process recursively on each subsequent sub-section (greater than & less than sections) until each has a length of 1. In doing this, we sort the array.&#x20;

**Goal:**

To sort the array in ascending order.

**Termination:**

The base case is met. This will mean only one element is in the array.&#x20;

**Explanation of the steps:**

* Establish a base case which will indicate that there is only one element in the array.&#x20;
* Now we partition. To partition, we pick a pivot.
  * The goal of partitioning is to divide the array into two groups:
    * The first group is less than the pivot and will go to the left of the pivot.
    * The second group is greater than the pivot and will go to the right of the pivot.
    * The pivot will ultimately move to the center, in between the groups.
  * Partitioning will return the new pivot and store it in a variable.
* After partitioning, we sort the two sub-regions.
* We call the quickSort() function on both sections.
* By repeating recursively, we sort the entire array.&#x20;

![](<../../../.gitbook/assets/image (101).png>)

{% embed url="http://cathyatseneca.github.io/DSAnim/web/quick.html" %}

**Time complexities:**

**Worst Case:**&#x20;

The worst case occurs when the partition process always picks greatest or smallest element as pivot. If we consider above partition strategy where last element is always picked as pivot, the worst case would occur when the array is already sorted in increasing or decreasing order, resulting in a time complexity of $$O(n^2)$$ .

**Best Case:**&#x20;

The best case occurs when the partition process always picks the middle element as pivot, resulting in a time complexity of $$Ω(n log(n))$$.

**Average Case:**

On average, we will perform $$n$$ comparisons at each iteration and $$logn$$ iterations resulting in a time complexity of $$Θ(n log(n))$$.

**Implementation:**

```
def quickSort(arr):

    length = len(arr)

    if length <= 1:
        return arr

    else:
        pivot = arr.pop()

    items_gt = []
    items_lt = []

    for item in arr:
        if item > pivot:
            items_gt.append(item)
        else:
            items_lt.append(item)

    return quickSort(items_lt) + [pivot] + quickSort(items_gt)
```

