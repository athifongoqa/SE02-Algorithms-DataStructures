---
description: First In, Last Out. Last In, First Out.
---

# Stacks

A stack is a type of list where items can only be added to one end and removed from the same end. Thus, a stack is a FILO (First In, Last Out) structure. The most common real-life representations of stacks would be things like a deck of cards, a stack of flapjacks or even a pile of plates. The exact example is unimportant but the idea is the same: Each time a new piece of data is added to the stack (**AKA push**), it is placed on the top. Each time a piece of data is removed it also must be removed from the top (**AKA pop**). Only the top item is directly accessible. The only way we can access the item at the bottom is by removing every item on top of it, one by one, because we cannot remove items from the middle.&#x20;

![https://www.tutorialspoint.com/data\_structures\_algorithms/stack\_algorithm.htm](<../../.gitbook/assets/image (17).png>)

**Accessing & Searching:**

Peeking allows us to access the top element of the stack in a time complexity of $$O(1)$$ without removing it. To be able to access an item (other than the top element) in a stack, we must first remove all the items on top of it, one by one. So in the worst case scenario, accessing said item will result in a time complexity of $$O(n)$$.

**Insertion & Removal:**

To insert an item at the top, we call this process a Push operation. We can only ever push a new item to the top so this operation will run in a time complexity of $$O(1)$$. To remove an item from the top, we call this a Pop operation. Just like the Push operation, the time complexity of this operation will also be $$O(1)$$

**Applications:**

An "undo" mechanism in text editors - this operation is accomplished by keeping all text changes in a stack. A compiler's syntax check for matching braces is implemented by using stack. To reverse a word - you push a given word to stack - letter by letter - and then pop letters from the stack into their new order. Used to implement function calls in recursion programming (aka a call stack). We will see this data structure in action later on in the Depth-First Search algorithm.&#x20;
