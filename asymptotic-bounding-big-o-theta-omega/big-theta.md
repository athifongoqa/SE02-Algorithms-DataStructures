# Big-Theta

The notation $$Θ(n)$$ is the formal way of expressing an algorithm runtime's lower bound and upper bound. Big theta can be considered as either the exact performance value of the algorithm, or a range somewhere between the algorithm's upper and lower bounds.

**Formally**:

"$$T(n)$$ is $$Θ(f(n))$$", if $$T(n)$$ is$$O(f(n))$$ **AND** $$T(n)$$ is $$Ω(f(n))$$for all $$n >= n_0$$.

![Khan Academy: https://www.khanacademy.org/computing/computer-science/algorithms/asymptotic-notation/a/big-big-theta-notation](<../.gitbook/assets/image (11).png>)

**Informally**:

"$$T(n)$$ is $$Θ(f(n))$$"$$f(n)$$ describes the exact bound for $$T(n)$$ where $$n >= n_0$$.

**Put simply:**

"$$T(n)$$ is $$Θ(f(n))$$", growth rate of $$T(n) ==$$growth rate of $$f(n)$$ where $$n >= n_0$$.
