# Binary Search

Now that we've seen Linear Search, it is time to consider its much more efficient alternative. In Linear Search, searching through each and every element will result in a time complexity of $$O(n)$$, we can liken it to opening a phone book (with names ordered in alphabetical order) on the first page and attempt to search for the name Xavier, page-by-page. Whilst this is not necessarily bad, it can still be greatly improved upon.&#x20;

Enter Binary Search. Binary Search is a faster search algorithm alternative with a time complexity of $$Ο(log n)$$. Take the phone book example from above, instead of going through it page-by-page it would be way more efficient to start by opening the phone book halfway and comparing the letters present with X. If we come across a page full of names beginning with M, we know that X will be in the right-hand half, so we rip the phone book in half and only focus on the half to the right of M. We then open this section halfway and repeat the process. We repeat this until we arrive at the page with Xavier on it. At every step, we half the size of the data collection, making it much faster to find our target. Just like in the example, for this algorithm to work properly, the data collection should be in the sorted form and searched according to the metric by which the collection is sorted.

**Goal:**

Our task is to find and return the index of our target element.&#x20;

**Termination:**

Either when the element has been found or when the subsequent subarray's size reduces to zero and the right pointer is less than the left pointer.

**Explanation of the steps:**

* Check if target element falls between first and last element in the array
  * We place pointers on them
  * The initial values of L and R are the first and last indices respectively
* Check the number in the middle of L & R
* Compare target and middle value
* If target = middle value:
  * Return the index of the middle value
* If target > middle value:
  * Move L pointer to (middle value index + 1)
* If target < middle value:
  * Move R pointer to (middle value index - 1)
* Repeat until middle value = target or when the R pointer comes to the left of the L pointer.
  * In the case of the latter, our search region is empty meaning the target element does not exist in the given array

**Time complexities:**

**Worst Case & Average Case:**

In every step of the search, we half the size of the array containing $$n$$ elements until we have an array of size 1, as follows:

$$n$$ $$\Rightarrow$$$$\frac{n}{2}$$$$\Rightarrow$$$$\frac{n}{4}$$$$\Rightarrow$$$$\frac{n}{8}$$$$\Rightarrow$$$$...$$$$\Rightarrow$$$$1$$

Written slightly differently, it will be:

$$n$$ $$\Rightarrow$$$$\frac{n}{2}$$$$\Rightarrow$$$$\frac{n}{2^2}$$$$\Rightarrow$$$$\frac{n}{2^3}$$$$\Rightarrow$$$$...$$$$\Rightarrow$$$$\frac{n}{2^x}$$$$\approx$$$$1$$

If $$n = 2^x$$ , that basically means we need to check $$x$$ elements. To find the number of elements we need to check, we need to find $$x$$ such that $$2^x$$is roughly equal to $$n$$ , as shown below:

&#x20;                                                                 $$2^x$$$$\approx$$$$n$$

If we solve for $$x$$:

&#x20;                                                                 $$x$$$$\approx$$$$log_{2}n$$

This results in a time complexity of:

&#x20;                                                                  $$O(log_{2}n)$$$$\approx$$$$O(logn)$$

**Best Case:**

In the best case, the target we are searching for is the first element we access, which would result in a time complexity of$$Ω(1)$$.

**Implementation:**

```
# Return index of the target or -1 
def binarySearch(arr, target):
    left = 0 
    right = len(arr)-1
    while left <= right:
        mid = round((left+right)/2)        # Round down
        if arr[mid] == target:
            return mid
        else if target < arr[mid]:
            right = mid-1
        else:
            left = mid+1
    return -1
```
