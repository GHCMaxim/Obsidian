### 1. Tích phân ở trên hình hộp
- $A=[a,b]\times[c,d]\times[e,f]$
- %% insert hình hộp chữ nhật %%
- $$\begin{align}
&T_{1}=a=x_{0}<x_{1}<...<x_{n}=b\\
  &T_{2}=c=y_{0}<y_{1}<...<y_{n}=d\\
  &T_{3}=e=z_{0}<z_{1}...<z_{n}=f\\
  &T=(T_{1},T_{2},T_{3})\\
  &A=\bigcup_{y=0}^{n}A_{j} \qquad A_{j}\;\text{là hình hộp con}\\
  &\iiint\limits_{A}f(x,y,z)dxdydz=I\qquad f\;\text{khả tích trên}\;A
  \end{align}$$
- *Chú ý:* Khả tích $\Leftarrow$ Liên tục $\Leftarrow$ Khả vi. Nhưng **KHÔNG** có ngược lại.
### 2. Cách tính tích phân bộ ba trong hệ toạ độ Decartes
Cách tính: Đưa về 3 tích phân xác định theo từng biến (tích phân lặp)
### 3. Tính chất
- $\iiint(f+g)dxdydz=\iiint f\;dxdydz+\iiint g\;dxdydz$
- $\iiint\limits_{D_{1}\cup D_{2}}fdv=\iiint\limits_{D_{1}}fdv+\iiint\limits_{D_{2}}fdv$ 
- Công thức Fubini: $$\iiint\limits_{[a,b]\times[c,d]\times[e,f]}f\;dxdydz=\int_a^bdx\int_c^ddy\int_e^ff(x,y,z)dz$$
	- Example: $\iiint\limits_{[0,1]^{3}}xyz\;dxdydz$
		- $$=\int_{0}^{1}xdx\int_{0}^{1}ydy\int_{0}^{1}zdz=\frac{1}{6}$$  
	- Example 2: 
		- ![[IMG_20220422_172113.jpg]]
### 3.1 Phép đổi biến tổng quát
- Xét tích phân $I=\iiint\limits_{\Omega}f(x,y,z)dxdydz$
- Đặt: $\begin{cases}x=x(u,v,w)\\y=y(u,v,w)\\z=z(u,v,w)\end{cases}$
- $$J=\frac{D(x,y,z)}{D(u,v,w)}=
\begin{vmatrix}x'_{u}&x'_{v}&x'_{w}\\y'_{u}&y'_{v}&y'_{w}\\z'_{u}&z'_{v}&z'_{w}\end{vmatrix}$$
- $\Omega \leftrightarrow \Omega_{I}$ 
- Khi đó:$$I=\iiint\limits_{\Omega_{I}}j$$