#### Section 10.1 
##### Exercise 1:
Skip vì chỉ kẻ mà dài vãi cặc
##### Exercise 3:
- Edges: Undirected
- Parallel edges: No
- Loops: No
$\Rightarrow$ Simple graph
##### Exercise 5:
- Edges: Undirected
- Parallel edges: 2? or 4, I think that's 2, idk
- Loops: 3
$\Rightarrow$ Psuedograph
##### Exercise 7:
- Edges: Directed (There be arrows)
- Parallel edges: None 
- Loops: 2
$\Rightarrow$ Directed graph
##### Exercise 9:
- Edges: Directed
- Parallel edges: 2
- Loops: 2
$\Rightarrow$ Directed multigraph
##### Exercise 10:
- Graph 3: Already simple
- Graph 4: (b;d);(a,b)
- Graph 5: (a,b);(b,d),(c,d)
- Graph 6: (a,c);(b,d)
#### Section 10.2
Pendant: deg = 1
Isolated: deg = 0
##### Exercise 1:
- Edges: 6
- Vertices: 6
- $deg(a)=2;deg(b)=4;deg(c)=1;deg(d)=0;deg(e)=2;deg(f)=3$
$\Rightarrow$ c is a pendant vertex, and d is an isolated vertex
##### Exercise 2:
- Edges: 12
- Vertices: 5
- $\begin{align}deg(a)=5\\deg(b)=6\\deg(c)=5\\deg(d)=5\\deg(e)=3\end{align}$
No pendant/isolated vertices
##### Exercise 3:
- Edges: 12
- Vertices: 9
- $\begin{align}deg(a)=3\\deg(b)=2\\deg(c)=4\\deg(d)=0\\deg(e)=2\\deg(f)=0\\deg(g)=4\\deg(h)=2\\deg(i)=3\end{align}$
$\Rightarrow$ f and d are isolated vertices
##### Exercise 4:
- Graph 1: 2+4+1+0+2+3=12 $\Rightarrow$ Twice edges
- Graph 2: 5+6+5+5+3=24  $\Rightarrow$ Twice edges
- Graph 3: 3+2+4+0+2+0+4+2+3=24 $\Rightarrow$ Twice edges
##### Exercise 4:
- Proving: 
	- Every edge has 2 ends. Therefore, the total number of edge ends must be even (Twice the amount of edges)
	- The degree of a vertex is the number of edges that end at said vertex. However, all edges have a vertex at both ends, the sum of all vertex degrees is Edges * 2. Therefore, it is always even
	- However, the sum of all vertex degrees is the sum of all even vertex degrees + the sum of all odd vertex degrees. While the first one is *obviously* even, the 2nd one also has to be even. But a sum of odd numbers is only even if there is an even number of them.
- Therefore, the number of vertices of odd degree *must* be even. Because of this, there cannot exist a graph with 15 vertices of odd degree 5
Note: Only after kinda solving the theorem, did I realize it was already in the ppt. >:L