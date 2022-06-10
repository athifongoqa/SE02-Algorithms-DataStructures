# Factorial Growth Rate – f(n!)

Successively multiplying a variable initialized to 1 by all the integers up to $$n$$ (if any) will compute $$n!$$&#x20;

E.g.:

&#x20;If $$n = 11$$&#x20;

&#x20;$$n!=(1 ×2×3×4×5×6×7×8×9×10×11)$$&#x20;

![](<../.gitbook/assets/image (78).png>)



To put into perspective how bad this can get notice the massive leaps between incrementing $$n$$.

```
factorial(1) # 1
factorial(2) # 2
factorial(5) # 120
factorial(10) # 3628800
factorial(15) # 1307674368000
factorial(20) # 2432902008176640000
factorial(25) # 15511210043330985984000000
```

