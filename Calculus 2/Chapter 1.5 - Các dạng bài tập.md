### Các dạng bài tập có thể gặp - Chap 1:
#### 1. Dạng 1: Tính độ cong
##### 1. Công thức 1:
Cho $\begin{cases} x=x(t)\\y=y(t) \end{cases}$ và điểm M.
$$\Rightarrow C(M) = \frac{\begin{vmatrix}x'(M) & y'(M) \\ x''(M) & y''(M)\end{vmatrix}}{[(x'(M)^2+y'(M)^2)]^\frac{3}{2}}$$  
- EX1: $\begin{cases}x=t^2-1\\y=t^3\end{cases}$ tại $M(0,1)$
	$M(0,1) \in (L) \Rightarrow \begin{cases}t^2-1=0\\t^3=1\end{cases} \Leftrightarrow t_0=1$ 
	Có  $\begin{cases}x'=2t\\y'=3t^2\end{cases}\Rightarrow \begin{cases} x'(t_0)=2\\y'(t_0)=3\end{cases}$
	$\begin{cases}x''=2\\y''=6t\end{cases}\Rightarrow \begin{cases}x''(t_0)=2\\y''(t_0)=6\end{cases}$
	$\Rightarrow C(M)=\frac{\left|\begin{vmatrix}2&3\\2&6\end{vmatrix}\right|}{(2^2+3^2)^\frac{3}{2}}=\frac{6}{13^\frac{3}{2}}$           
- EX2: $y=-x^3$ tại $x=\frac{1}{2}$ 
	Đặt $x=t$
	$\Rightarrow\begin{cases}x=t\\y=-t^3\end{cases}$ tại $t=\frac{1}{2}$ 
	Có $\begin{cases} x'=1\\y'=-3t^2\end{cases}\Rightarrow \begin{cases}x'(t)=1\\y'(t)=\frac{-3}{4}\end{cases}$  
	$\begin{cases}x''=0\\y''=-6t\end{cases}\Rightarrow \begin{cases}x''(t)=0\\y''(t)=-3\end{cases}$ 
	$\Rightarrow C(M)=\frac{\left|\begin{vmatrix}1&\frac{-3}{4}\\0&-3\end{vmatrix}\right|}{(1^2+\frac{-3}{4}^2)^\frac{3}{2}}=\frac{-3}{\frac{25}{16}^\frac{3}{2}}$    
##### 2. Công thức 2:
Cho $r=r(\varphi)$ và điểm $M$ ứng với $\varphi_0$ 
$$\Rightarrow C(M) = \frac{\left|r^2+2r'^2-r.r''\right|}{(r^2+r'^2)^\frac{3}{2}}$$
- EX1: $r=a.e^{b\varphi}(a,b>0)$  
	$r'=a.b.e^{b\varphi}$
	$r''=a.b^2.e^{b\varphi}$ 
	$$\Rightarrow C(M)=\frac{\left|a^2.e^{2b\varphi}+2a^2b^2e^{2b\varphi}-a^2be^{2b\varphi}\right|}{(a^2e^{2b\varphi}+a^2b^2e^{2b\varphi})^\frac{3}{2}}=\frac{1}{\sqrt{1+b^2}\;a.e^{b\varphi}}$$
##### 3. Công thức 3: Độ cong trong không gian
Cho $\begin{cases}x=x(t)\\y=y(t)\\z=z(t)\end{cases}$ tại $M(t_0)$ hay $r(t)=x(t)\overrightarrow{i}+y(t)\overrightarrow{j}+z(t)\overrightarrow{k}$  
$\Rightarrow C(M) = \frac{\left|r'(t)\wedge r''(t)\right|}{\left| r'(t)\right|^3}$   
- EX1: $\begin{cases}x=Cos(t)\\y=Sin(t)\\z=t\end{cases}$ tại $t_0= \frac{\pi}{2}$ 
	$\overrightarrow{r}(t)=Cost.\overrightarrow{i}+Sint.\overrightarrow{j}+t.\overrightarrow{k}$
	$\overrightarrow{r'}(t)=-Sint.\overrightarrow{i}+Cost.\overrightarrow{j}+1.\overrightarrow{k}$   
	$\overrightarrow{r''}(t)=-Cost.\overrightarrow{i}-Sint.\overrightarrow{j}+0.\overrightarrow{k}$ 
	$\Rightarrow \begin{cases}\overrightarrow{r}(t_{0)=}-1.\overrightarrow{i}+0+1.\overrightarrow{k}=(-1;0;1)\\ \overrightarrow{r''}(t_0)=0.\overrightarrow{i}-1\overrightarrow{j}+0.\overrightarrow{k}=(0;1;0)\end{cases}$  
	$\Rightarrow C(M)=\frac{1}{2}$ 
#### 2. Dạng 2: Các phương trình tiếp tuyến, pháp tuyến (Tangent, Normal(?) equations)
##### 0.5. Cách nhớ công thức:
- Đối với các phương trình dạng f ($f(x,y);f(x,y,z)$), thì "tiếp" là nhân và ngược lại. 
- Để nhớ các công thức, chỉ cần nhớ 1 để có thể suy ra công thức còn lại. Nếu nhớ công thức dạng phân số, thì để tìm ra công thức còn lại, ta đặt mẫu số biến thành thừa số và ngược lại.
##### 1. Dạng 2.1:
Cho $\begin{cases}x=x(t)\\y=y(t) \end{cases}$ tại $t=t_0$ ; $A(a,b)$ 
- *Phương trình tiếp tuyến*: $\frac{x-a}{x'(t_0)}=\frac{y-b}{y'(t_0)}$
- *Phương trình pháp tuyến*: $x'(t_0)(x-a)+y'(t_0)(y-b)=0$
-***Cách làm***: Tính A, $x'(t),y'(t)$, thay giá trị $t_0$ , rồi tính các phương trình.
- EX1: $\begin{cases}x=2t-Cos\pi t\\y=2t+Sin\pi t\end{cases}$ tại $t=\frac{1}{2}$ 
	Thay $t=\frac{1}{2}$ vào hệ pt $\Rightarrow A(1,2)$  
	$\begin{cases}x'_t=2+\pi Sin(\pi t)\\y'_t=2+\pi Cos(\pi t)\end{cases}\Rightarrow \begin{cases}x'(\frac{1}{2})=2+\pi\\y'(\frac{1}{2})=2\end{cases}$
	$\Rightarrow$ Tiếp tuyến:  $\frac{x-1}{2+\pi}=\frac{y-2}{2}$ 
	$\Rightarrow$ Pháp tuyến: $(2+\pi)(x-1)+2(y-2)=0 \Leftrightarrow (2+\pi)x+2y -6 -\pi =0$ 
 ##### 2. Dạng 2.2:
Cho $f(x,y)=0$ tại $A(a,b)$
- *Phương trình tiếp tuyến*: $f'_x(A)(x-a)+f'_y(A)(y-b)=0$
- *Phương trình pháp tuyến*: $\frac{x-a}{f'_x(A)}=\frac{y-b}{f_y'(A)}$ 
- ***Cách làm***: Tính $f'_x(A);f'_y(A)$ rồi thay vào công thức. 
- EX1: $y=e^{1-x^2}$ giao với đường $y=1$
	Phương trình hoành độ giao điểm: $$\begin{align}&e^{1-x^2}=1 \\\Leftrightarrow\; &1-x^{2} = 0 \\\Leftrightarrow\; &x = \pm 1\end{align}$$ $\Rightarrow A(1,1),B(-1,1)$
	Đặt $f(x,y)=y-e^{1-x^2}=0$ 
	$\Leftrightarrow \begin{cases}f'_x=2x.e^{1-x^2}\\f'_y=1\end{cases}$
	- TH1: Xét theo $A(1,1)$
		$\Leftrightarrow\begin{cases}f'_x(A)=2\\f'_y(A)=1\end{cases}$ 
		Phương trình tiếp tuyến: $2(x-1)+1(y-1)=0$
		Phương trình pháp tuyến: $\frac{x-1}{2}=\frac{y-1}{1}$
	- TH2: Xét theo $B(-1,1)$
		$\Leftrightarrow \begin{cases}f'_x(B)=-2\\f'_y(B)=1\end{cases}$
		Phương trình tiếp tuyến: $-2(x-1)+1(y-1)=0$
		Phương trình pháp tuyến:	$\frac{x-1}{-2}=\frac{y-1}{1}$ 
##### 3. Dạng 2.3:
Cho $\begin{cases}x=x(t)\\y=y(t)\\z=z(t)\end{cases}$ tại $t=t_0$ ; $M(a,b,c)$
- *Phương trình tiếp tuyến*: $\frac{x-a}{x'(t_{0})}=\frac{y-b}{y'(t_{0})}=\frac{z-c}{z'(t_{0})}$ 
- *Phương trình pháp diện*:  $x'(t_0)(x-a)+y'(t_0)(y-b)+z'(t_0)(z-c)=0$ 
- ***Cách làm***: Tính $x',y',z'$ theo $t$, đông thời thay trực tiếp $t_0$ vào, rồi thay vào công thức
EX1: $\begin{cases}x=a.Sin^2(t)\\y=b.Sin(t).Cos(t)\\z=c.Cos^2(t)\end{cases}$ với $t=\frac{\pi}{4}$ 
	$\Leftrightarrow \begin{cases}x'_t=a.2.Sin(t).Cos(t)=a.Sin2t\\y'_t=b.Cos(2t)\\z'_t=c.2.-Sin(t).Cos(t)=-c.Sin2t\end{cases}$
	$\Leftrightarrow \begin{cases}x'(\frac{\pi}{4})=a\\y'(\frac{\pi}{4})=0\\z'(\frac{\pi}{4})=-c\end{cases}$ 
	Tại $t=\frac{\pi}{4}\Leftrightarrow A(\frac{a}{2},\frac{b}{2},\frac{c}{2})$ 
	Phương trình tiếp diện: $\frac{x-\frac{a}{2}}{a}=\frac{y-\frac{b}{2}}{0}=\frac{z-\frac{c}{2}}{-c}$ 
	Phương trình pháp diện: $a(x-\frac{a}{2})+0(y-\frac{b}{2})-c(z-\frac{c}{2})=0$  
##### 4. Dạng 2.4
Cho $f(x,y,z)=0\;,\;A(a,b,c)$ 
- *Phương trình pháp diện:*$\frac{x-a}{f'_x(A)}=\frac{y-b}{f'_y(A)}=\frac{z-c}{f'_z(A)}$  
- *Phương trình tiếp tuyến*: $f'_x(A)(x-A)+f'_y(B)(y-b)+f'_y(C)(z-c)=0$ 
- ***Cách làm***: Tính $f'_x(A);f'_y(A);f'_z(A)$ rồi thay vào công thức
EX1: $ln(2x+y^2)+3z^3=3$ . $A(0,-1,1)$ 
	$\Leftrightarrow \begin{cases}f'_x=\frac{2}{2x+y^{2}}\\f'_y=\frac{2y}{2x+y^{2}}\\f'_z=9z^{2}\end{cases}\Leftrightarrow \begin{cases}f'_x(A)=2\\f'_y(A)=-2\\f'z(A)=9\end{cases}$   
	Phương trình tiếp tuyến: $2(x-0)-2(y+1)+9(z-1)=0$
	Phương trình pháp diện: $\frac{x-0}{2}=\frac{y+1}{2}=\frac{z-1}{9}$ 
##### 5. Dạng 2.5
Cho $\begin{cases}f(x,y,z)=0\\g(x,y,z)=0\end{cases}$  tại $A(a,b,c)$
Có: $(f'_x(A),f'_y(A),f'_z(A))\wedge (g'_x(A),g'_y(A),g'_z(A))=(m,n,p)$ 
- *Phương trình tiếp tuyến*: $\frac{x-a}{m}=\frac{y-b}{n}=\frac{z-c}{p}$ 
- *Phương trình pháp diện*: $m(x-a)+n(y-b)+p(z-c)=0$ 
- ***Cách làm***: Tính $f'_x,f'_y,f'_z$ và $g'_x,g'_y,g'_z$, rồi thay A vào từng số đạo hàm để ra 2 bộ số mới, nhân có hướng với nhau để ra vector $(m,n,p)$ rồi thay vào công thức.
EX1: $(L)\begin{cases}x^{2}+y^{2}=10\\y^{2}+z^{2}=25\end{cases}$ tại $A(1,3,4)$
	$\Leftrightarrow \begin{cases}f'_x=2x\\f'_y=2y\\f'_z=0\end{cases}\;;\;\begin{cases}g'_x=0\\g'_y=2y\\g'_z=2z\end{cases}$ 
	$\Leftrightarrow \begin{cases}f'_x(A)=2\\f'_y(A)=6\\f'_z(A)=0\end{cases}\Leftrightarrow \overrightarrow{n}_f=(2,6,0)\;;\;\begin{cases}g'_x(A)=0\\g'_y(A)=6\\g'_z(A)=8\end{cases}\Leftrightarrow \overrightarrow{n}_g=(0,6,8)$   
	$\overrightarrow{u}_{(L)}=\overrightarrow{n}_{f}\wedge \overrightarrow{n}_{g}=4(12,-4,3)\;//\;(12,-4,3)$ 
	Phương trình tiếp tuyến: $\frac{x-1}{12}=\frac{y-3}{-4}=\frac{z-4}{3}$ 
	Phương trình pháp diện: $12(x-1)-4(y-3)+3(z-4)$ 
#### 3. Dạng 3: Tìm hình bao của 1 họ đường phụ thuộc tham số:
Cho $f(x,y,c)=0\qquad (1)$ 
- Bước 1: Tìm điểm kì dị
	- Tính $f'_x;f'_y$ , tìm điểm A sao cho cả $f'_x;f'_y=0$  được gọi là điểm kì dị
- Bước 2: Tìm hình bao
	- Lập hệ pt: $\begin{cases}f(x,y,c)=0\\f'_c(x,y,c)=0\end{cases}$ 
	- Rút gọn $c$ sao cho chỉ còn lại pt $g(x,y)=0$ được gọi là phương trình hình bao.
- Chú ý: Khi tính ra điểm kì dị, có 2 trường hợp xảy ra:
	- TH1: $g(x,y)=0$ là hình bao và quỹ tích các điểm kì dị (là các điểm kì dị ở trên)
	- TH2: $g(x,y)=0$ là hình bao (không có điểm kì dị)
EX: $f(x,y,c)=cx^{2}-3y-c^{3}+2=0$
$\begin{cases}f'_{x}=2cx=0\\f'y=-3 \neq 0\end{cases}\Rightarrow$ Không có điểm kì dị
Ta có: $\begin{cases}f(x,y,c)=cx^{2}-3y-c^{3}+2=0\\f'_{c}(x,y,c)=x^{3}-3c^{2}=0\end{cases}$ 
$\Leftrightarrow c^{2}=\frac{x^{3}}{3}\Leftrightarrow c=\pm \sqrt{\frac{x^{3}}{3}}$
TH1: $c=\sqrt{\frac{x^{3}}{3}}$
$g(x,y)=\frac{x^{\frac{9}{2}}}{\sqrt{3}}-3y+\frac{x^{\frac{9}{2}}}{\sqrt{3}^{3}}+2=0$  
TH2:$c=-\sqrt{\frac{x^{3}}{3}}$ 
$g(x,y)=\frac{-x^{\frac{9}{2}}}{\sqrt{3}}-3y+\frac{x^\frac{9}{2}}{\sqrt{3}^{3}}+2=0$  
 
#### 4. Dạng 4: Ứng dụng phép tính vi phân trong không gian:
$\overrightarrow{r_1}(t)=x_1(t)\overrightarrow{i}+y_1(t)\overrightarrow{j}+z_1\overrightarrow{k}$ 
$\overrightarrow{r_2}(t)=x_2(t)\overrightarrow{i}+y_2(t)\overrightarrow{j}+z_2\overrightarrow{k}$ 
$$\begin{align}&\overrightarrow{r}(t)=(x(t),y(t),z(t))\\&\left|\overrightarrow{r}(t)\right|=\sqrt{x^{2}(t)+y^{2}(t)+z^{2}(t)}\\&\overrightarrow{r_1}(t).\overrightarrow{r_2}(t)=x_1(t).x_2(t)+y_1(t).y_2(t)+z_1(t).z_2(t)\\&\frac{d(\overrightarrow{r}(t)}{dt}=(x'(t),y'(t),z'(t))\end{align}$$ 
