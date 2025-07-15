### Notes: 

I am doing the funny because I can, so this guide will follow the general writing rules of the KTaNE manual. This is only a **semi-comprehensive** guide to the topic of DSA. There's too little time and too many topics to cover, hence a lot of the nitty gritty will be removed for the sake of this not being a fucking textbook. I trust that you'll be able to figure that part out when absolutely necessary.
### Introduction
Welcome to the nerd-like and stupid world of DSA.

Study this guide carefully; ***you are the expert***. In this file, you will find mostly everything you need to know to answer most of the medium-hard questions. And remember - ***DON'T FUCK THIS UP***.
(There will be a bonus stage at the end if you manage to get through all this. Hint: I hope you liked the examples.)
### On the Subject of Big-O Notation
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

### On the Subject of Searching Algorithms:
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
### On the Subject of General Data Structure:
Following is the table for general interaction speed. You **don't** need to know this table. However, it's nice to know just in case.
#### Notes:
- Linked list can be doubly lined, which means it has 2 places to starts.
- Hash table is *generally* ALL $O(1)$, unless when it has collisions, then it's $O(n)$.
- Binary Search Tree is *generally* ALL $O(log(n))$, unless the tree is skewed.

| DS                          | Random Access | Search                                  | Insertion                               | Deletion                                | Space Complexity |
| --------------------------- | ------------- | --------------------------------------- | --------------------------------------- | --------------------------------------- | ---------------- |
| Array                       | $O(1)$        | $O(log(n)$(sorted) <br>$O(n)$(unsorted) | $O(1)$ at end<br>$O(n)$ anywhere else   | $O(1)$ at end<br>$O(n)$ anywhere else   | $O(n)$           |
| Linked list                 | $O(n)$        | $O(n)$                                  | $O(1)$ at start<br>$O(n)$ anywhere else | $O(1)$ at start<br>$O(n)$ anywhere else | $O(n)$           |
| Hash Table                  | You don't     | $O(1)$ - $O(n)$                         | $O(1)$ - $O(n)$                         | $O(1)$ - $O(n)$                         | $O(n)$           |
| Binary Search Tree          | You don't     | $O(log(n)$- <br>$O(n)$                  | $O(log(n)$- <br>$O(n)$                  | $O(log(n)$- <br>$O(n)$                  | $O(n)$           |
| Balanced Binary Search Tree | You don't     | $O(log(n)$                              | $O(log(n)$                              | $O(log(n)$                              | $O(n)$           |

### On the Subject of Linked Lists

As simple as in the name itself, this data type is a bunch of values connected to each other to form a big line you can't cut through, therefore to know whether someone is in the line, all you can do is ask the person at the bottom/top of the line, for them to ask up. It's only main use case is when all you *really* care about is Insertion or Deletion.

You only really need to understand that, each member of the list have its value, and a sign pointing to the next value. Think of the 100 Prisoners problem. The optimal solution is converting the boxes into a linked list (Box 10 points to Box 40, Box 40 points to box 11,...), and hope that it's a circular linked list at the size <50.

3 main types of LL:
- Single LL: You can only traverse forwards
- Double LL: You can traverse backwards and forwards
- Circular LL: The final node connects to the first one.

### On the Subject of Stack/Queue

Stack means that it's following First In, Last Out. Think of a stack of plates, you don't can't take the plate at the bottom because it will crash and burn, however, you can take the plate at the top for free.
Queue means that it's following First In, First Out. Think of a line of people waiting to go into a stadium. First guy gets in line gets in first.

Both of them has the general same functions to manipulate things inside: 
	-`push()` or `enqueue()`: Insert into the Stack/Queue
	-`pop()` or `dequeue()`: Remove the final element
	-`top()` or `peek()`: Check the first element without doing anything about it.
	-`isEmpty()` or `isFull()`


### On the Subject of Trees
Here comes the fun and complicated part, there are many types of trees, however, I'll generalize and point out the unique part of most of them so that your head won't burst open. As for how you generally traverse a tree, please refer to the Tree Traversal/Path finding section.

Each tree will generally have:
- A root (the starting/top-most point)
- Nodes (Values inside the tree)
- Branches/Edges (The line connecting nodes)

The depth of a node means how far down from the root it is.
The height of the tree means the length of the deepest node to the root.

Most of the trees will use Binary Tree as it's basic form.

#### Binary Trees:
A Binary tree means that at all times, all nodes will only have at most 2 children.
Because of this, a node of a binary tree will have:
- It's own value
- A value pointing to its left child
- A value pointing to its right child.

Insertion always start with left child.
Deletion means that you are pulling its right child up(if it exists, else left.) as replacement. If it has no child, no need to replace anything.

There are some terms you have to know:
- **Balanced Binary Tree:** The difference between height of left subtree and right subtree is at most **1**.
- Preorder Traversal: Visit the node, go left subtree, then right subtree
- Inorder Traversal: Visit left subtree, to the node, to right subtree
- Postorder Traversal: Visit left subtree, to right subtree, to node.

#### Binary Search Tree(BST)
It's the same as the binary tree, however, all nodes to the left is always less in value than the node, and all nodes to the right is always larger. This model makes it easier to search/insert/delete, as just like Binary Search, it is sorted.

##### Note: 
```
I highly doubt they will go this far into the part below this section of trees. However, it's best to be prepared.
```

#### AVL Tree
This is a self-balancing Binary Tree. It achieves this by rotating some of the nodes and checking the Balance Factor on insertion/deletion until the tree balances itself. 
Every node should have a Balance Factor between -1 and 1 for the whole tree to be balanced.
- Balance Factor: Left subtree height - Right subtree height
- Left-Left rotation: You rotate the left-most node, down left.
- Right-Right rotation: You rotate the right-most node, down right.
- Left-Right rotation: You rotate the left child left, then the node right.
- Right-Left rotation: You rotate the right child right, then the node left.

#### Red-Black Tree
Another self-balancing Binary Tree. It achieves this by coloring nodes red or black...?
A bit confusing isn't it, but here's some guidelines:
- Root is always black
- No red nodes connecting to each other.
- Empty nodes (i.e right = null) are black, and are called NIL nodes.
- All paths from a node to a node to a NIL node should have the same amount of black nodes

It's possible to prove that with those rules, it is impossible for a chain a 3 nodes to not be balanced. Only left and right rotations are available for this tree.

##### Note: 
```
I won't go into B(+) Trees as I absolutely doubt they will ask on it, and Ternary Search Trees, as it's the same as Binary Search Trees, just 3 children.
```

### On the Subject of Tree Traversal / Path Finding

##### Note:
```
No direct examples will be given, as that gets long, fast. Therefore, only the gist of things will be displayed here. You are free ask me to add some, or go deeper into each algo through Mizuki if necessary.
```
#### Breadth First Search(BFS):
The general rule of thumb to understand is that BFS is pouring water into a vertical maze to solve it, you are going through all possible steps, from left to right, before going downwards.

You will generally meet more dead-ends using this route. However, you can map everything, so this is best used to search for things in a tree/maze.

#### Depth First Search (DFS):
If BFS is pouring water into a vertical maze, this is sticking your hand down the hole, at deep as you could until you touch a wall, then moving backwards, going from left to right.

You will generally find the way out/last node faster this way. However, just because there's a hole, doesn't mean you have to stick your d\*ck into it. 

This is where the Post/In/Preorder Traversals come in, as you will be using this search type to find out.

#### Djikstra's Algorithm
This is your go to solution for pathfinding with weights. To make it easier to understand, this is just BFS with a weight calculator to consider options. Best used to find the shortest path from one node to another.
### On the Subject of Recursion

This is generally just the function calling itself while running, either directly inside the function, or indirectly though another function. You are generally trading performance for less code when choosing this option. Unless *specifically* have to, use iterative, or a variation of Dynamic Programming to make the problem go faster.

Common use-cases for Recursions include:
	- Tree/Graph traversal
	- Sorting
	- Divide and Conquer scenarios
	- Backtracking
	- Memoization (or caching)

Example:
```Java
static int fibbo(int n)
{
	if (n= == 0)
		return 0;
	if (n == 1 || n == 2)
		return 1;
	else
		return (fib(n-1) + fib(n-2))
}
```

### On the Subject of Greedy 
This is just choosing the most obvious and immediate solution to the problem at that single moment.Because you are only choosing what's best then, this will generally not be the optimal solution. Therefore, problems where choosing what's best then is the way to use Greedy. I won't give an example on this one, however you can search online to find some decent ones.
### On the Subject of Dynamic Programming
This is just an optimization over just plain recursion. The entire concept rests upon the idea of storing the results of subproblems so that you don't have to recalculating things you've already worked on.

Example:
```Java
static int nthFibbo(int n){
	if (n<=1)
		return n;
	int[] dp = new int[n+1];
	dp[0] = 0;
	dp[1] = 1;
	for (int i = 2; i<=n; i++) {
		dp[i] = dp[i-1] + dp[i-2]
	}
	return dp[n];
}
```

2 general ways of doing DP:
- Bottom-up(Tabulation): You go from the smallest problem possible, and gradually build up to the final problem. You get rid of recursion completely, and write only iteration. (Refer to the nthFibbo example above.)
- Top-down(Memoization): You keep the solution recursive, however you save the values you have calculated inside a table for use later.

Top-down example: nthFibbo:
```Java
static int Util(int n, int[] dp){
	if (n<=1){
		return n;
	}
	if (dp[n] != -1) {
		return dp[n];
	}
	dp[n] = Util(n-1, dp);
}

static int nthFibbo(int n) {
	int[] dp = new int[n+1];
	Arrays.fill(dp, -1);
	return Util(n, dp);
}
```