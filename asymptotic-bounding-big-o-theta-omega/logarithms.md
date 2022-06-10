---
description: >-
  This was a really great question posted in the Google Classroom. I solved it
  after going through some of the activities and explanations provided by Khan
  Academy.
---

# Big-O of the Logarithm

## &#x20;**Is**$$\log _{2} N = O(\log(N))$$**?**&#x20;

Both $$\log _{2} N$$ _(log base 2 of N)_ and $$\log(N)$$ _(log base 10 of N)_ are functions with logarithmic growth, with their base as the only difference. Here's a graph of the two functions:

![](<../.gitbook/assets/image (29).png>)

_A graph with two curves, one for_ $$\log _{2} N$$ _and the other for_ $$\log(N)$$_. The x axis represents n and goes from 0 to 16, the y axis represents the result and goes from 0 to 8. The curve for_ $$\log _{2} N$$ _is above the curve for_ $$\log(N)$$_, once N > 1._

If we were to say that $$\log _{2} N$$ is $$O(\log(N))$$ , then we would be saying that $$\log _{2} N$$ has an asymptotic upper bound of $$O(\log(N))$$, i.e. that for large enough $$N$$ , the running time is at most $$k ⋅ log(N)$$ for some constant $$k$$ . So, we need to come up with a $$k$$ to multiply $$\log(N)$$ by so that it always bounds $$\log _{2} N$$.

It helps to remember this property of logarithms: $$\log_{a} n =$$$$\log_{b}n\over \log_{b}a$$&#x20;

That property means that $$\log(N)$$ can be rewritten in terms of $$\log _{2} N$$:

$$\log(N) =$$$$\log_{2}N\over \log_{2}10$$&#x20;

Which is also:

$$\log(N) =$$$$1\over \log_{2}10$$$$\log_{2}N$$&#x20;

We can now see that $$\log(N)$$ is just $$\log_{2}N$$ times a constant. When we find two functions differ by a constant multiplier, then we know we can always find a $$k$$ to serve as the upper bound. For example, here's a graph where $$k = 5$$&#x20;

![](<../.gitbook/assets/image (31).png>)

_A graph with two curves, one for_ $$\log_{2}N$$ _and the other for 5 times_ $$\log(N)$$_. The x axis represents N and goes from 0 to 16 the y axis represents the result and goes from 0 to 8. The curve for 5 times_ $$\log(N)$$ _is above the curve for_ $$\log_{2}N$$_, once N > 1._

As mentioned before, we can basically ignore constants in asymptotic notation, and treat the functions as equivalent. (Again, meaning $$log(N) = 5⋅log(N)$$)

All of that just to say that yes,  $$\log_{2}N$$ = $$O(\log(N))$$.
