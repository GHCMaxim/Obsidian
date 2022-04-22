### 3. Ứng dụng của tích phân bội 2
#### 1. Tính diện tích hình phẳng
![[Drawing 2022-04-22 16.06.36.excalidraw]]
$$S_{(D)}=\iint\limits_{D}dxdy$$
- Example: ![[Drawing 2022-04-22 16.08.45.excalidraw]]
	- Cách 1: $$S_{(D)}=\int_{0}^{1}dx\int_{0}^{1}dy=1$$
	- Cách 2: $$\begin{cases}x=rCos\varphi\\y=rSin\varphi\end{cases}$$
		![[Drawing 2022-04-22 16.08.46.excalidraw]]
		$$\begin{align}D_{1}:\begin{cases}0\leq \varphi\leq\frac{\pi}{4}\\0\leq r\leq \frac{1}{cos\varphi}\end{cases}\\D_{2}:\begin{cases} \frac{\pi}{4}\leq\varphi\leq \frac{\pi}{2}\\0\leq r \leq \frac{1}{sin\varphi}\end{cases}\\S=S_{D_{1}}+S_{D_{2}}\\=\int_{0}^\frac{\pi}{4}d\varphi\int_{0}^\frac{\pi}{cos\varphi}xdr+\int...\end{align}$$
	- Example 2: $$\begin{cases}y=x\\y=x^{2}\end{cases}$$
		Cách 1:
		$$I=\int_{0}^{1}dx\int_{x^{2}}^{x}dy=\frac{1}{6}$$
		Cách 2:
		$$I=\int_{0}^{1}dy\int_{y}^{\sqrt{y}}dx=\frac{1}{6}$$
		Cách 3:
		$$\begin{cases}x=rCosy\\y=rSiny\end{cases}\Rightarrow \begin{cases}0\leq \varphi\leq \frac{\pi}{4}\\0\leq r \leq \frac{sin\varphi}{cos^{2}\varphi}\end{cases}$$
		$$S_{(D)}=\int_{0}^{\frac{\pi}{4}}d\varphi\int_{0}^\frac{sin\varphi}{cos^{2}\varphi}rdr$$
	- Example 3: $\begin{cases}y=x\\y=2x\\xy=1\\xy=2\end{cases}$
		- Đổi biến: Đặt $u=xy\;;\;v=\frac{y}{x}$ 
			- $$\begin{align}\begin{cases}1\leq u\leq 2\\1\leq v\leq 2\end{cases} \Rightarrow \begin{cases}x=\sqrt{\frac{u}{v}}\\y=\sqrt{uv}\end{cases}\\\Rightarrow J_{\varphi}=\begin{vmatrix}x'_{u}&x'_{v}\\y'_{u}&y'_{v}\end{vmatrix}=\frac{1}{2v}>0\\S(D)=\int_{1}^{2}du\int_{1}^{2} \frac{1}{2v}dv= \frac{ln2}{2}\end{align}$$ 
	- Example 4: $D$ giới hạn bởi đường Lemniscate $(x^{2}+y^{2})=2a^{2}(x^{2}-y^{2})$ 
		- Đổi sang toạ độ cực: $\begin{cases}x=rCos\varphi\\y=rSin\varphi \end{cases}$ 
		- $$\begin{align}r^{4}=2a^{2}r^{2}Cos(2\varphi) \Rightarrow r=a.\sqrt{2cos(2\varphi)}\\\Rightarrow \begin{cases}-\frac{\pi}{4}\leq\varphi\leq \frac{\pi}{4}\\ \frac{3\pi}{4}\leq\varphi\leq \frac{5\pi}{4}\end{cases}\\S(D)=2\int_{\frac{-\pi}{4}}^\frac{\pi}{4}d\varphi\int_{0}^{a.\sqrt{2cos(2\varphi)}}rdr =2a^{2}\end{align}$$
	- Example 5: $D$ giới hạn bởi lá Decartes: $x^{3}+y^{3}=axy$ 
		- Đổi sang toạ độ cực
		- $$\begin{align}&\begin{cases}0\leq \varphi\leq \frac{\pi}{2}\\0\leq r\leq \frac{aSin\varphi Cos\varphi}{Sin^{3}\varphi+Cos^{3}\varphi}\end{cases}\\&r^{3}(Cos^{3}\varphi+Sin^{3}\varphi)=ar^{2}Sin\varphi Cos\varphi\\&S(D)=\int_{0}^{\frac{\pi}{2}}d\varphi\int_{0}^{\frac{aSin\varphi Cos\varphi}{Sin^{3}\varphi+Cos^{3}\varphi}}rdr=\frac{a^{2}}{2}\int_{0}^{\frac{\pi}{2}}\frac{Sin\varphi Cos\varphi}{(Sin^{3}\varphi+Cos^{3}\varphi)^{2}}d\varphi\\&\text{Đặt}\;t=tan\varphi \Rightarrow \frac{a^{2}}{2} \frac{1}{3}\int_{0}^{+\infty}\left(\frac{d(t^{3}+1)}{(t^3+1)^2}\right)\Biggr|_{0}^{+\infty}=\frac{a^{2}}{6}\end{align}$$
		