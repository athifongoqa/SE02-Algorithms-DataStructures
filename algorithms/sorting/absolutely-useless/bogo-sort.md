# Bogo Sort

Bogo Sort also known as permutation sort, stupid sort, slow sort, shotgun sort or monkey sort is a particularly ineffective algorithm based on generate and test paradigm. The algorithm successively generates permutations of its input until it finds one that is sorted. ([Wiki](https://en.wikipedia.org/wiki/Bogosort))\


For example, if Bogo Sort is used to sort a deck of cards, it would consist of checking if the deck were in order, and if it were not, one would throw the deck into the air, pick the cards up at random, and repeat the process until the deck is sorted.

**Goal:**

To sort the array in ascending order.

**Termination:**

When the helper function which determines if it is sorted returns `True`.

**Explanation of the steps:**

* First, we run a helper function to check if the array is sorted, it returns True if it is and False if it isn't.
* If it returns True, the algorithm terminates.
* If it returns False, we run a shuffle helper function which will generate a random permutation of the array.
* We repeat step 3 as long as step 2 does not apply.

{% embed url="https://bl.ocks.org/alexmacy/770f14e11594623320db1270361331dc" %}

**Time complexities:**

**Worst Case:**&#x20;

Because in every iteration we randomly rearrange the array, this algorithm does not have an upper bound, resulting in a time complexity of $$O(∞)$$(which I did not even know existed before this).

**Best Case:**&#x20;

The best case occurs when array given is already sorted, which case we will be required to check if the array is sorted, resulting in a time complexity of $$Ω(n)$$.

**Average Case:**&#x20;

In the average case the algorithm needs to test all $$n!$$ permutations and for each one of them checking if the list is sorted requires $$O(n)$$ time, resulting in a time complexity of $$Θ(n*n!)$$.

**Implementation:**

```
def bogoSort(arr):
    n = len(arr)
    while (is_sorted(arr)== False):
        shuffle(arr)
  
# To check if array is sorted or not
def is_sorted(arr):
    length = len(arr)-1
    for i in range(0, length):
        if (arr[i] > arr[i+1] ):
            return False
    return True
  
# To generate permuatation (shuffle) of the array
def shuffle(arr):
    length = len(arr)-1
    for i in range (0, length):
        r = random.randint(0,n-1)
        arr[i], arr[r] = arr[r], arr[i]
```
