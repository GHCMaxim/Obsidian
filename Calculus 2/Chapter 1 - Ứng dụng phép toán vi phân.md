### I. Ứng dụng trong hình học mặt phẳng
#### 1.  Vector tiếp tuyến, phương trính tiếp tuyến và pháp tuyến của đường cong tại 1 điểm
##### * Đường cong trong mặt phẳng
- Dạng $y=f(x)$ 
- Dạng tổng quan: $f(x,y)=0$
- Dạng tham số $\begin{cases} x=x(t) \\ y= y(t) \end{cases}$
##### * Vector tiếp tuyến
Cho $M(x,y), M_0(x_0,y_0) \in (L)$ (Đường cong)
$$\begin{align}
\overline{MM_0} &= (x-x_0,y-y_0) = (\Delta{x},\Delta{y})\\\\
\overrightarrow{v} &= \lim_{M \to M_0}{\overline{MM_0}} \; \text{là tiếp tuyến}\\
&=\lim_{(\Delta{x},\Delta{y}) \to (0,0)}{(\Delta{x},\Delta{y})}
\end{align}$$
##### * Điểm chính quy, điểm kì dị
- Cho $f(x,y)=0$ hoặc $\begin{cases} x = x(t) \\ y = y(t) \end{cases}$ với $M \in (C)$  
- Nếu $$\begin{align} [f'_x(M)]^2 + [f'_y(M)]^2 = 0 \\ (\; \text{hay} \; [x'(t_0)]^2 + [y'(t_0)]^2 \neq 0 \;)\end{align}$$   thì M là điểm chính quy. Ngược lại, M là điểm kì dị.
#### 2. Phương trình tiếp tuyến và pháp tuyến
- Cho $(C)$ và $M \in (C)$ 
	- **TH1:** $(C) ; f(x,y)=0$ 
		<=> $f'_x(M)dx + f'_y(M)dy = 0$ (1) 
		Đặt $\overrightarrow{n} = (f'_x(M),f'_y(M))$ *vector tiếp tuyến:* $\overrightarrow{u}=(dx,dy)$ 
		(1) $\Leftrightarrow \overrightarrow{n}.\overrightarrow{u}=0 \Leftrightarrow \overrightarrow{n} \; \bot \; \overrightarrow{u}$    
		- *Phương trình tiếp tuyến tại M:* $f'_x(M)(x-x_0)+f'_y(M)(y-y_0)=0$ 
		- *Phương trình pháp tuyến tại M:* $\frac{x-x_0}{f'x(M)} = \frac{y-y_0}{f'y(M)}$  
	- **TH2:** $(C)\begin{cases}x=x(t) \\ y=y(t)\end{cases};M:\begin{cases}x_0=x(t) \\ y_0=y(t) \end{cases} \Leftrightarrow t=t_0$  
		- *Vector tiếp tuyến:* $\overrightarrow{u}=(dx,dy) = (x'(t)dt, y'(t)dt)$ 
		- *Phương trình tiếp tuyến:* $\frac{x-x_0}{x'(t_0)}=\frac{y-y_0}{y'(t_0)}$ 
		- *Phương trình pháp tuyến:* $x'(t_0)(x-x_0)+y'(t_0)(y-y_0)=0$ 
#### 3. Độ cong
- Trên đường cong $(L)$, chọn hướng dương, lấy $M, M_0 \in (L)$ 
- Lấy 2 tiếp tuyến $MT$ và $M_0T$ sao cho hướng của $\overrightarrow{MT},\overrightarrow{M_0T}$ tương thích với hướng dương của $(L)$ 
- Đặt $\alpha=(\overrightarrow{M_0T},\overrightarrow{MT})$ 
- **Định nghĩa:** Độ cong trung bình của $(L)$ tại $M_0$ được xác định bởi:$$C_{TB}(M_0)=\frac{\alpha}{\overline{MM_0}}$$
- **Đường cong** của $(L)$ là giới hạn $$\lim_{M \to M_0}{C_{TB}(M_0)} = \lim_{M \to M_0}{\frac{\alpha}{\overline{MM_0}}}$$ Ký hiệu: $C(M)$
- **Công thức:**
	- TH1: $(L) \; y=f(x) \rightarrow C(M)= \frac{\lvert y''\rvert}{(1+y'^2)^\frac{3}{2}}$ 
	- TH2: $(L)\begin{cases} x=x(t)\\y=y(t)\end{cases} \rightarrow C(M) = \frac{\lvert x'y''-x''y'\rvert}{(x'^2+y'^2)^\frac{3}{2}}$
	- TH3: $(L)\;r=r(\varphi)\rightarrow C(M)=\frac{\lvert r^2+2r'^2-r.r'' \rvert}{(r+r'^2)^\frac{3}{2}}$
#### 4. hình bao
- **Định nghĩa:** Cho họ đường cong $(L_C)$ phụ thuộc vào các tham số. Đường cong $(E)$ gọi là hình bao của họ $(L_C)$ nếu mọi đường cong của $(L_C)$ đều tiếp xúc với $(E)$ và tạo mỗi điểm của $(E)$ có 1 đường cong của $(L_C)$ tiếp xúc với E.
- **Công thức:**
	- *Định lý:* Cho họ đường cong $(L_C): F(x,y,c)=0$  không có điểm kì dị (tức là $F'x^2+F'y^2\neq 0 \; \forall M \in L_C$) 
	   Khi đó, phương trình hình bao của họ $(L_C)$ xác định bằng việc khử c từ hệ $\begin{cases} F(x,y,c)=0 \quad(1) \\F'c(x,y,c)=0\end{cases}$ .
	- *Chú ý:* Nếu $(L_C)$ có điểm kì dị thì (1) xác định hình bao và tập các điểm kỳ dị
### II. Ứng dụng trong không gian
#### 1. Hàm vector
##### a. Định nghĩa
- Hàm vector trên D:
$$\begin{align}&\overrightarrow{r}:D\subset\mathbb{R} \rightarrow \mathbb{R}^3\\&t\mapsto\overrightarrow{r}(t)=(x(t);y(t);z(t))\end{align}$$
- Chú ý:  $\overrightarrow{r}(t)=x(t)\overrightarrow{i}+y(t)\overrightarrow{j}+z(t)\overrightarrow{k}$   
##### b. Tốc độ
- Cho $\overrightarrow{r}(t),t \in D$. Xét M sao cho $\overrightarrow{OM}=\overrightarrow{r}(t)$ . $\{M|OM=\overrightarrow{r}(t),t \in D\}$ là 1 đường cong được gọi là tốc độ.
 ##### c. Giới hạn - Liên tục
 $$\begin{align}&\lim_{t \to t_0}{\overrightarrow{r}(t)}=\overrightarrow{a} \Leftrightarrow \forall \varepsilon > 0, \exists \; \delta(\varepsilon) >0 \;\text{sao cho}\; \forall t : \left| t-t_0 \right| < \delta \\ \Rightarrow &\left| \overrightarrow{r}(\theta-\overrightarrow{a})\right|<\varepsilon \end{align}$$
 ##### d. Đạo hàm
 $$\overrightarrow{r'}(t_0)=\lim_{t \to t_0}{\frac{\overrightarrow{r}(t)-\overrightarrow{r}(t_0)}{t-t_0}}$$
 - $\overrightarrow{r}(t)$ khả vi tại $t=t_0$ 
 - *Nhận xét*: $$\begin{cases}\overrightarrow{r}(t)=(x(t);y(t);z(t))\\x(t);y(t);z(t)\; \text{khả vi tại}\; t=t_0\end{cases}$$
 - $\overrightarrow{r}(t)$ khả vi tại $t=t_0$ và $\overrightarrow{r'}(t_0)=(x'(t_0);y'(t_0);z'(t_0))$ 
 #### 2. Đường cong
 - $(L)$ là tốc độ của hàm $\overrightarrow{r}(t)(x(t);y(t);z(t))$
 $\Rightarrow$ *Phương trình tham số:* $\begin{cases}x=x(t)\\y=y(t)\\z=z(t)\end{cases}$
 
$\ast$ ***Nhận xét***: $\overrightarrow{r'}(t_0)$ là tiếp tuyến của đường cong $(L)$ tại $M(t_0)$ 
$\Rightarrow$ *Phương trình tiếp tuyến* $(L)$ tại $M(t_0)$:
$$\frac{x-x_0}{x'(t_0)}=\frac{y-y_0}{y'(t_0)}=\frac{z-z_0}{z'(t_0)}$$
- Pháp diện của $(L)$ tại $M_0$ là 1 mặt phẳng vuông góc với tiếp tuyến tại $M_0$ 
$\Rightarrow$ *Phương trình pháp diện* tại $M$ là: $$x'(t_0)(x-x_0)+y'(t_0)(y-y_0)+z'(t_0)(z-z_0)=0$$
$\ast$ Độ cong trong $\mathbb{R}^3$ :$$\begin{align}(L):\;&\overrightarrow{r}(t)=(x(t);y(t);z(t))\\&M(x_0;y_0;z_0)\end{align}$$
$\Rightarrow$ *Độ cong của $(L)$ tại $M$ là*: $$C(M)=\frac{\sqrt{\begin{vmatrix}x'&y'\\x''&y''\end{vmatrix}^2+\begin{vmatrix}y'&z'\\y''&z''\end{vmatrix}^2+\begin{vmatrix}z'&x'\\z''&x''\end{vmatrix}^2}}{(x'^2+y'^2+z'^2)^\frac{3}{2}}$$
#### 3. Mặt cong
##### a. Định nghĩa
- Dạng tổng quát: $(S): F(x,y,z)=0$ 
- Dạng tham số: $(S)\begin{cases}x=x(u;v)\\y=y(u;v)\\z=z(u;v)\end{cases}$ 
- Cho mặt cong S, và M là 1 điểm nằm trên mặt cong:
	- Đường $\Delta$ là tiếp tuyến của $(S)$ tại M nếu tồn tại đường cong $(L)$ nằm trên $(S)$ nhận $\Delta$ là tiếp tuyến tại M.
	- Tập hợp các tiếp tuyến của $(S)$ tại M lập thành 1 mặt phẳng được gọi là tiếp diện của $(S)$  tại M.
	- Đường thẳng vuông góc với tiếp diện của $(S)$ tại M được gọi là pháp tuyến của $(S)$ tại M
##### b. Công thức
$$(S):F(x;y;z)=0,M(x_0;y_0;z_0)\in (S)$$
$\Rightarrow$ *Phương trình pháp tuyến tại M:$$\frac{x-x_0}{f'x(M)}=\frac{y-y_0}{f'y(M)}=\frac{z-z_0}{f'z(M)}$$
$\Rightarrow$ Phương trình tiếp diện tại M:*
$$f'x(M)(x-x_0)+f'y(M)(y-y_0)+f'z(M)(z-z_0)=0$$