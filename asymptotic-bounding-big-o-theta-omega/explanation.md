# Further Explanation

**What all this means:**

Let us take a closer look the formal definition for big-O analysis:

"$$T(n)$$ is$$O(f(n))$$", if for some constants $$k$$ and $$n_0$$, $$T(n) <= k ⋅ f(n)$$ for all$$n >= n_0$$&#x20;

The way to read the above statement is as follows:

* $$n$$ is the size of the data set.
* $$f(n)$$ is a function that is calculated using $$n$$ as the parameter.
* $$O(f(n))$$ means that the curve described by $$f(n)$$ is an upper bound for the resource needs of function $$T(n)$$.
* $$n_0$$indicates the minimum value where $$T(n)$$ will **always** be less than $$f(n)$$ without exception.&#x20;

This means that if we were to draw a graph of the resource needs of a particular algorithm, it would fall under the curve described by $$f(n)$$ . Also, it does not need to be under the exact curve described by $$f(n)$$. It could be under a constant scaled curve for $$f(n)$$, so instead of having to be under the $$n^2$$ curve, it can be under the $$10n^2$$ curve or the $$200n^2$$ curve. In fact, it can be any constant, as long as it is a constant. A constant is simply a number that does not change with $$n$$. So as$$n$$ gets bigger, you cannot change what the constant is. The actual value of the constant does not matter though. We are only concerned with the fastest growing term in a statement. Meaning,$$O(n)=O(3n)=O(12n+3)$$ and $$O(n^2) = O(24n^2 +34) = O(3n^2 +2)$$&#x20;

The other portion of the statement $$n >= n_0$$ means that $$T(n) <= k ⋅ f(n)$$ does not need to be true for all values of $$n$$. It means that as long as you can find a value $$n_0$$ for which $$T(n) <= k ⋅ f(n)$$ is true, and it never becomes untrue for all $$n$$ larger than $$n_0$$ , then you have met the criteria for the statement: $$T(n)$$ is$$O(f(n))$$

In summary, when we are looking at big-O, we are in essence looking for a description of the growth rate of the fastest growing term. The exact numbers (whether they be constants or coefficients) do not actually matter in the end.



