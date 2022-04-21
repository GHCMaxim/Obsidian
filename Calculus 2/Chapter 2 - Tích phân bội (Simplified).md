## Tích phân bội - Simplified
### 1. Xác định hình
- Mục đích: Đưa 1 hình phẳng về 2 biến $x,y$ với quy tắc: Nếu $x$ cận là số thực, thì $y$ phải là một hàm theo biến $x$ $\left(\begin{cases}a\leq x\leq b\\f(x)\leq y\leq g(x)\end{cases}\right)$  (Note: $f(x);g(x)$ cũng có thể là số thực) và ngược lại.
#### a. Dạng hình chữ nhật
![[Drawing 2022-04-21 16.17.13.excalidraw]]
$$\begin{align}C_{1}:\begin{cases}a\leq x \leq b\\c\leq y \leq d\end{cases}\\C_{2}:\begin{cases}c\leq y \leq d\\a\leq x \leq b\end{cases}\end{align}$$
Note: Tuỳ thuộc xét theo đường nào, từ trái sang phải hay từ dưới lên trên.
#### b. Hình cong:
![[Drawing 2022-04-21 16.24.29.excalidraw]]
- Cách xác định: 
	- Xác định cận của $x$ trước: $a\leq x \leq b$
	- Để xác định cận của $y$ ,kẻ một đường thẳng đi từ dưới lên trên. Ta thấy nó cắt qua $g(x)$ trước rồi đến $f(x)$ $\Rightarrow$ $g(x)\leq y \leq f(x)$
	- $\begin{cases}a\leq x\leq b\\g(x) \leq y \leq f(x)\end{cases}$
#### c. Xác định bởi 3 đường
![[Drawing 2022-04-21 16.42.37.excalidraw]]
- Cách xác định $D = D_{1} \cup D_{2}$ 
	- $D_{1}:\begin{cases}a\leq x \leq b\\ f_{3}(x)\leq y\leq f_{1}(x)\end{cases}$
	- $D_{2}: \begin{cases}b\leq x\leq c\\f_{3}(x)\leq y\leq f_{2}(x)\end{cases}$ 
### 2. Tính chất:
#### 1. Tính chất tổng:
- Nếu $D=D_{1}+D_{2}$ và $f(x,y)$ khả tích trên $D$ thì:$$\iint\limits_{D}f(x,y)dxdy=\iint\limits_{D_1}f(x,y)dxdy \;+\;\iint\limits_{D_2}f(x,y)dxdy$$
#### 2. Trị tuyệt đối:
- Nếu $f(x,y)$ và $|f(x,y)|$ là những hàm khả tích trên $D$ thì: $$\left|\iint\limits_{D}f(x,y)dxdy\right|=\iint\limits_{D}|f(x,y)|dxdy$$
- 