# Hashing

### Hash Functions <a href="#hash-functions" id="hash-functions"></a>

A hash function's design must be such that given a certain key it will always return the same numeric value in a time complexity of$$O(1)$$. The hash function will ideally distribute all possible keys in the key space uniformly over all possible locations.&#x20;

![https://www.tutorialspoint.com/data\_structures\_algorithms/images/hash\_function.jpg](<../../../.gitbook/assets/image (32).png>)

Consider this example, we want to create a table for storing customer information. A customer's phone number can be used for the key. The table can hold up to 10,000 records and thus valid indexes for an array of that size would be \[0 - 9999] respectively.

* Telephone numbers in this case are 10 digits long => (###) ###-####
* The first 3 of which is the area code of the phone number.
* So, if the hash function was to use the first 4 digits of the phone number (area code and fourth digit), that hash function would not be very good because most (if not all) people in the same area would have the same area code. Most people in Johannesburg have an area code of 011 or 010, so there would be almost no variation in the records. However the last 4 digits of a phone number are more likely to be different between different customers.

Generally speaking a good hash function should adhere these rules:

* be uniformly distributed (all indices are equally likely for the given set of possible keys)
* be random (not predictable)
* be fast to compute
* avoid collisions
