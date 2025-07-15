### Notes: 

I am doing the funny because I can, so this guide will follow the general writing rules of the KTaNE manual. This is only a **semi-comprehensive** guide to the topic of DSA. There's too little time and too many topics to cover, hence a lot of the nitty gritty will be removed for the sake of this not being a fucking textbook. I trust that you'll be able to figure that part out when absolutely necessary.
### Introduction
Welcome to the nerd-like and stupid world of DSA.

Study this guide carefully; ***you are the expert***. In this file, you will find mostly everything you need to know to answer most of the medium-hard questions. And remember - ***DON'T FUCK THIS UP***.
(There will be a bonus stage at the end if you manage to get through all this. Hint: I hope you liked the examples.)
### On the topic of Big-O Notation
Generally speaking, this is *the* tool everyone and their mother uses to describe *how efficient* an algorithm runs.

Usually noted as $O(f(n))$ , where $f(n)$ is the amount of steps that an algorithm needs to perform to solve a problem of size $n$. It also gives the upper limi-. You know what, that's all the nerd stuff.

All you *really* need to understand about the Big-O Notation is that:
- How many loops does the function go through. Each extra loop is one more power added.
- Logarithmic/Exponential/Factorial *probably* means that some janky recursion or DP is applied. 
- Multiple runs are counted as one and the same ($O(2n) = O(n)$)
- $O(n!) < O(c^{n}) < O(n^{c}) < O(nlog(n)) < O(n) < O(log(n))$
- This is additional info, so you don't have to remember them. However it's nice to know *just in case*:
	-  Exponential ($O(c^{n})$) means that there's $c$ extra values to deal with before it's done.
	(Think you have a group of 3 friends, now you have to find out all the ways you can place them in a line, and all 3 doesn't have to be in the line.)
	
	- Logarithmic $(O(log(n)))$ means that the run time is proportional to the input size.
	(Think of Hoshino split-, no wait. Think of constantly chopping an apple in half to find its seed.)
	
	- Factorial ($O(n!)$) means that the input grows factorially. 
	(Think you have 3 group of friends, now find out all the ways you can place them in a line, with all 3 have to be in a line.)


Here's a quick example for you to find out the big-O Notation:
```python
a = [<things>]
b = [<things>]
for item_a in a:
	for item_b in b:
		if item_a == item_b:
			print("same") 
		else:
			print("not same")
```
There are 2 for loops, interconnected. Therefore the notation is $O(n^2)$. The more interconnected loops, the more numbers you add to the power.

### On the topic of Searching Algorithms:
I won't go over Linear Search, as that's literally iterating the array till you find the fucking thing.
However, I will:
#### Binary Search:
This is the way to search for a sorted array of values. It works by splitting the entire array in half, checking the value, and going in the direction of the thing you want to find.

Example: For your convenience, I will pre-sort the array. However, you **MUST** sort it to use this algo for obvious reasons.
```python
value = 6
arr = [1,2,3,4,5,6,7,8,9,10]
```
	Step 1: Split in half, check middle number, if length is even, grab whichever, in this case, left. finds 5. 6 > 5, go right side, remove all on the left.
	Step 2: Split right side in half, check middle number, finds 8. 6 < 8, go left side, remove all on the right.
	Step 3: Split left side in half, check middle number, finds 6. Done. 

Yup, that's the entire thing. Speed is generally $O(log(n))$ because you are dividing it in half every time.
### On the topic of General Data Structure:
Following is the table for general interaction speed. You **don't** need to know this table. However, it's nice to know just in case.
#### Notes:
- Linked list can be doubly lined, which means it has 2 places to starts.
- Hash table is *generally* ALL $O(1)$, unless when it has collisions, then it's $O(n)$.
- Binary Search Tree is *generally* ALL $O(log(n))$, unless the tree is skewed.

| DS                          | Random Access | Search                                  | Insertion                                   | Deletion                                | Space Complexity |
| --------------------------- | ------------- | --------------------------------------- | ------------------------------------------- | --------------------------------------- | ---------------- |
| Array                       | $O(1)$        | $O(log(n)$(sorted) <br>$O(n)$(unsorted) | $O(1)$ at end<br>$O(n)$ anywhere else       | $O(1)$ at end<br>$O(n)$ anywhere else   | $O(n)$           |
| Linked list                 | $O(n)$        | $O(n)$                                  | $O(1)$ at start/end<br>$O(n)$ anywhere else | $O(1)$ at start<br>$O(n)$ anywhere else | $O(n)$           |
| Hash Table                  | You don't     | $O(1)$ - $O(n)$                         | $O(1)$ - $O(n)$                             | $O(1)$ - $O(n)$                         | $O(n)$           |
| Binary Search Tree          | You don't     | $O(log(n)$- <br>$O(n)$                  | $O(log(n)$- <br>$O(n)$                      | $O(log(n)$- <br>$O(n)$                  | $O(n)$           |
| Balanced Binary Search Tree | You don't     | $O(log(n)$                              | $O(log(n)$                                  | $O(log(n)$                              | $O(n)$           |
