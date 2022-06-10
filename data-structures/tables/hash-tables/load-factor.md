# Load Factor

The load factor denoted by the symbol $$\lambda$$ measures the fullness of the hash table. It is calculated by the formula:

$$\lambda =$$ $$number~of~records~in~table\over number~of~locations$$&#x20;

* Its purpose is to give us a sense of how "full" a hash table is.
* It can be used as an indicator for when to rehash. As the load factor approaches 0 (zero), the more empty our hash table is.&#x20;
* The closer our load is to 1, the better it is to rehash & address the collisions (covered on the next page).
* Any table with where $$\lambda > 1$$, is guaranteed to have collisions. A great way of understanding this is through [The Pigeonhole Principle](https://youtu.be/B2A2pGrDG8I).&#x20;



&#x20;
