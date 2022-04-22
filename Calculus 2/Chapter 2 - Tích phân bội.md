## I. Tích phân kép (Tích phân bội 2)
### 1. Định nghĩa - Tính chất
#### 1.1: Bài toán tính thể tích hình trụ cong (Chia nhỏ - Tập hợp)
#### 1.2 Định nghĩa
- Cho $f=f(x,y)$ xác định trên miền đóng và bị chặn $D$
	- Chia $D$ thành từng miền nhỏ $D_1,D_2,...,D_n$ 
	- $S(D_i)$ là diện tích miền $D$ với $i=\overline{1;n}$ 
	- Lập tổng $I_n=\sum_{i=1}^{n}f(M_i)=SD_i$ 
- Cho $n \to +\infty$  , $max(SD_i) \to 0$ ; nếu $I_n\to I$ không phụ thuộc vào cách chia $D$ , và các cách chọn $D$ thì $I$ là tích phân kép của $f$ trên $D$ :$$I=\iint\limits_{D}f(x;y)dxdy$$
$\Rightarrow$ $f$ khả vi trên $D$.
$\ast$ *Ý nghĩa hình học:*
	- Thể tích hình trụ cong: $V=\iint\limits_{D}f(x;y)dxdy$ 
- ***Định lý:*** Nếu $f(x,y)$ liên tục trên $D$ thì $f(x;y)$ khả tích trên $D$
- ***Tính chất***:
	- $\iint\limits_{D}\alpha f(x,y)dxdy=\alpha\iint\limits_{D}f(x,y)dxdy$  
	- $\iint\limits_{D}[f(x,y)+g(x,y)]dxdy=\iint\limits_{D}f(x,y)dxdy+\iint\limits_{D}g(x,y)dxdy$ 
	- Nếu $D$ được chia làm 2 miền $D_1,D_2$ rời nhau: $$\iint\limits_Df(x,y)dxdy=\iint\limits_{D_1}f(x,y)dxdy+\iint\limits_{D_2}f(x,y)dxdy$$
	- $S_D=\iint\limits_{D}1dxdy=\iint\limits_{D}dxdy$ 
	- $\forall (x,y) \in D, f(x,y) \leq g(x,y) \Rightarrow \iint\limits_{D}f(x,y)dxdy \leq \iint\limits_{D}g(x,y)dxdy$ 
### 2. Cách tính tích phân kép trong toạ độ Decartes
#### a. TH1: D là hình chữ nhật:
- $D=[a,b]\times[c,d]$  
$$\Rightarrow I=\int_{a}^{b}dx\int_{c}^{d}f(x,y)dy=\int_{c}^{d}dy\int_{a}^{b}f(x,y)dx $$
- Chú ý: Khi $D=[a,b]\times[c,d]$ và $f(x,y)=g(x)h(y)$ , ta có:
$$\Rightarrow I=\iint g(x)h(y)dxdy=\left(\int_{a}^{b}g(x)dx\right)\left(\int_{c}^{d}h(y)dy\right)$$
#### b. TH2: $D: \begin{cases}a\leq x\leq b\\f_1(x) \leq y \leq f_2(x)\end{cases}$ 
$$\Rightarrow I=\int_a^b\left[\int_{f_1x}^{f_2x}f(x,y)dy\right]dx=\int_a^bdx\int_{f_1(x)}^{f_2(x)}f(x,y)dy$$
![[Drawing 2022-04-14 16.09.38.excalidraw]] 
#### c. TH3: $D: \begin{cases}c \leq y \leq d\\f_1(y) \leq x \leq f_2(y)\end{cases}$  
$$\Rightarrow I = \int_c^d\left[\int_{f_1(y)}^{f_2(y)}f(x,y)dx\right]dy=\int_c^ddy\int_{f_1(y)}^{f_2(y)}f(x,y)dx$$
![[Drawing 2022-04-14 16.25.29.excalidraw]]
### Các dạng bài toán:
#### 1. Bài toán 1: Bài toán đổi thứ tự tích phân: (Làm tương tự với y)
- Từ biểu thức tích phân lặp, suy ra biểu diễn giải tích của miền lấy tích phân là: $$(D): \begin{cases}a\leq x \leq b\\f_1(x)\leq y \leq f_2(x)\end{cases}$$
- Vẽ phác thảo miền D:
![[Drawing 2022-04-14 16.09.38.excalidraw]]
- Chia D thành các hình thang cong có các cạnh song song với $Ox$. Tìm biểu diễn giải tích các miền con, ví dụ $(D_i):\begin{cases}c_i\leq y \leq d_i\\ f_1(y)\leq x \leq f_2(y) \end{cases}$ 
- Sau đó viết: $$\int_a^bdx\int_{f_1(x)}^{f_2(x)}f(x,y)dy=\sum\limits_{i}\int_{c_i}^{d_i}dy\int_{f_1(y)}^{f_2(y)}f(x,y)dx$$
#### 2. Bài toán 2: Tính các tích phân kép có chứa dấu giá trị tuyệt đối
Giả sử cần tính $\iint\limits_{D}\left|f(x,y)\right|dxdy$ .
Mục đích của chúng ta là phá bỏ được dấu giá trị tuyệt đối. Vì vậy, ta khảo sát dấu của hàm $f(x,y)$ . Do tính liên tục của hàm $f(x,y)$ nên đường cong $f(x,y)=0$ sẽ chia miền $D$ thành 2 miền, $D^+\;,\;D^-$ . Trên miền $D^+$ , $f(x,y)\ge0$ , và trên miền $D^-$ , $f(x,y)\leq0$. 

- Chúng ta có công thức: $$\iint\limits_{D}\left|f(x,y)\right|dxdy=\iint\limits_{D^+}f(x,y)dxdy+\iint\limits_{D^-}f(x,y)dxdy\qquad (2.1)$$
$\Rightarrow$ *Các bước để làm bài toán:*
	1. Vẽ đường cong $f(x,y)=0$ để tìm đường cong phân chia miền $D$.
	2. Giả sử đường cong tìm được chia miền $D$ thành 2 miền. Để xác định xem miền nào là $D^+$ , miền nào là $D^-$, ta xét 1 điểm $(x_0,y_0)$ bất kì, sau đó tính giá trị $f(x_0,y_0)$ . Nếu $f(x_0,y_0)\gt0$ thì miền chứa $(x_0,y_0)$ là $D^+$ và ngược lại.
	3. Sau khi xác định được các miền $D^+,D^-$ , sử dụng công thức $(2.1)$ để tính tích phân.
#### 3. Bài toán 3: Tính tích phân kép trong trường hợp miền lấy tích phân là miền đối xứng
- ***Định lý 1:*** Nếu miền $D$ là miền đối xứng qua trục $Ox$ (tương ứng trục $Oy$) và là hàm lẻ đối với $y$ (tương ứng đối với $x$ ) thì $$\iint\limits_{D}f(x,y)dxdy=0 $$
- ***Định lý 2***: Nếu miền $D$ là miền đối xứng qua trục $Ox$ (tương ứng $Oy$ và là hàm chẵn đối với $y$ ( tương tự đối với $x$ )thì $$\iint\limits_{D}f(x,y)dxdy=2\iint\limits_{D^+}f(x,y)dxdy$$
trong đó $D^+$ là phần nằm bên trên trục $Ox$ của $D$ (tương ứng phía phải của trục $Oy$ của $D$) 
- ***Định lý 3:*** Nếu miền $D$ là miền đối xứng qua trục gốc tọa độ $O$ và hàm $f(x, y)$ thỏa mãn $f(-x,-y)=-f(x,y)=0$ thì$$\iint\limits_{D}f(x,y)dxdy=0$$
### 3. Phép đổi biến số trong tích phân kép
#### 1. Phép đổi biến số tổng quát
Phép đổi biến số tổng quát thường được sử dụng trong trường hợp miền $D$ là giao của *2 họ đường cong*. Xét tích phân kép $\iint\limits_{D}f(x,y)dxdy$  trong đó $f(x,y)$ liên tục trên $D$. 
- Thực hiện phép đổi biến số$$\begin{cases}x=x(u,v)\\y=y(u,v)\end{cases}\qquad\qquad(2.2)$$
thoả mãn:
	- $x=x(u,v);y=y(u,v)$ là các hàm số liên tục và có đạo hàm riêng liên tục trong miền đóng $D_{uv}$ của mặt phẳng $O'_{uv}$ .
	- Công thức $(2.2)$ xác định song ánh từ $D_{uv}\to D$ .
	- Định thức Jacobi: $J=\frac{D(x,y)}{D(u,v)}=\begin{vmatrix}x'_u&x'_v\\y'_u&y'_v\end{vmatrix}\neq 0 \forall (u,v)\in D_{uv}$
Khi đó, ta có biến số:
$$I=\iint\limits_{D}f(x,y)dxdy=\iint\limits_{D_{uv}}f(x(u,v),y(u,v))\left|J\right|dudv$$
- ***Chú ý***:
	- *Mục đích*: Biến miền $D$ từ hình dáng phức tạp về tính tích phân trên miền $D_{uv}$ đơn giản hơn như là hình thang cong hoặc hình chữ nhật, đồng thời có tác dụng làm đơn giản hoá biểu thức tính tích phân $f(x,y)$.
	- Để xác định được miền $D_{uv}$ , lưu ý rằng phép biến đổi biến số sẽ biến biên của miền $D$ thành biên của miền $D_{uv}$ 
	- Có thể tính $J$ thông qua $J^{-1}=\frac{D(u,v)}{D(x,y)}=\begin{vmatrix}u'_{x} & u'_{y}\\v'_{x} & v'_{y}\end{vmatrix}$
#### 2. Phép đổi biến số trong toạ độ cực
- Trong rất nhiều trường hợp, việc tính toán tích phân kép trong toạ độ cực đơn giản hơn **rất nhiều** so với việc tính tích phân trong toạ độ Decartes, đặc biệt khi miền $D$ có dạng hình tròn, quạt tròn, cardioids,... và hàm dưới dấu tích phân có những biểu thức $(x^2+y^2)$ .
- Toạ độ cực của điểm $M(x,y)$ là bộ $(r,\varphi)$ , trong đó $$\begin{cases}r=\left|\overrightarrow{OM}\right|\\\varphi=\widehat{Ox,\overrightarrow{OM}}\end{cases}$$
![[Drawing 2022-04-16 08.36.57.excalidraw]]
Công thức đổi biến: $\begin{cases}x=rCos\varphi\\y=rSin\varphi\end{cases}$ trong đó miền biến thiên của $r,\varphi$ phụ thuộc vào hình dạng của miền $D$ . Khi đó:$$\begin{align}&J=\frac{D(x,y)}{D(r,\varphi)}=r\\&I=\iint\limits_{D_{r\varphi}}f(rCos\varphi,rSin\varphi)rdrd\varphi\end{align}$$
Đặc biệt, nếu miền lấy tích phân có dạng hình quạt $\begin{cases}\varphi_1\leq\varphi\leq\varphi_2\\r_1(\varphi)\leq r \leq r_2(\varphi)\end{cases}$ :
![[Drawing 2022-04-16 08.57.20.excalidraw]]
thì: $$I=\int_{\varphi_1}^{\varphi_2}d\varphi\int_{r_1(\varphi)}^{r_2(\varphi)}f(rCos\varphi,rSin\varphi)rdr$$
