# Merge Sort

Merge Sort falls under the class of Divide and Conquer algorithms. The main idea with Merge Sort is that it splits a large array down recursively as much as possible (until we have arrays of size 1) and builds it back up in a sorted fashion, iteration-by-iteration, until we have an ordered array which is the same size as the original array.&#x20;

**Goal:**

To sort the array in ascending order.

**Termination:**

After splitting the given array into subarrays, once the split subarrays have been merged back together again in order, the algorithm will terminate.&#x20;

**Explanation of the steps:**

* First, we split the original array in half.
* Recursively divide array(s) in half until we are left with arrays of size 1 (contain a single element).
* Compare every second element to the element before it.
* We can now put one element in front of the other in an array twice the size, giving us a relative order of those two elements (meaning the two will be arranged in ascending order).
* We now compare the array of size 2 with the array of size 2 before it.&#x20;
* Because our arrays are longer of size 1, but instead size 2, we use a pointer method with two pointers, each respectively pointing at elements in each array.&#x20;
* We now compare the two smallest items in each array and place the smaller one at the beginning of the new array which is twice the size of the previous array.&#x20;
* We advance the smallest one's pointer to the right and compare the two elements again.&#x20;
* We repeat these steps until our array of size $$n$$ is full and in order. Below is a representation of this process along with the order of steps.&#x20;

![https://media.geeksforgeeks.org/wp-content/cdn-uploads/Merge-Sort-Tutorial.png](<../../../.gitbook/assets/image (100).png>)

{% embed url="http://cathyatseneca.github.io/DSAnim/web/merge.html" %}

**Time complexities:**

The time complexity of Merge Sort is $$O(nlogn)$$ in all 3 cases (worst, average and best) because we must perform $$n$$ comparisons at each iteration and $$logn$$ number of iterations to merge the subarrays together to form the original array in sorted form.

Basically:

$$
O((comparisons)(iterations)) \approx O((n)(logn)) \approx O(nlogn)
$$

**Implementation:**

```
def merge_sort(arr):
    
    # The last array split
    if len(arr) <= 1:
        return arr
    
    mid = len(arr) // 2
    
    # Perform merge_sort recursively on both halves
    left, right = merge_sort(arr[:mid]), merge_sort(arr[mid:])

    # Merge each side together
    return merge(left, right, arr.copy())


def merge(left, right, merged):

    left_pointer, right_pointer = 0, 0
    while left_pointer < len(left) and right_pointer < len(right):
      
        # Sort each one and place into the result
        if left[left_pointer] <= right[right_pointer]:
            merged[left_pointer+right_pointer]=left[left_pointer]
            left_pointer += 1
        else:
            merged[left_pointer + right_pointer] = right[right_pointer]
            right_pointer += 1
            
    for left_pointer in range(left_pointer, len(left)):
        merged[left_pointer + right_pointer] = left[left_pointer]
        
    for right_pointer in range(right_pointer, len(right)):
        merged[left_pointer + right_pointer] = right[right_pointer]

    return merged
```

### &#x20;<a href="#merge-algorithm" id="merge-algorithm"></a>
