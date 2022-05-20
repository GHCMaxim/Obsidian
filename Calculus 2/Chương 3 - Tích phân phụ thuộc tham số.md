## 1. Tích phân xác định phụ thuộc tham số
### 1.1 Định nghĩa
- Cho hàm số $f(x,y)$ liên tục trên $[a,b]\times[c,d]$ . Khi đó:$$l(y)=\int\limits_{a}^{b}f(x,y)dx$$
là một hàm số xác định trên $[c,d]$ và được gọi là một tíclh phân phụ thuộc tham số
- Mục đích: Khảo sát tính liên tục, khả vi, khả tích của $l(y)$
### 1.2 Tính chất
#### a. Tính liên tục
- Định lý: Nếu $f(x,y)$ là hàm số liên tục trên $[a,b]\times[c,d]$ thì $l(y)$ là hàm số liên tục trên $[c,d]$:$$\lim_{y\to y_0}l(y)=\lim_{y\to y_0}\int\limits_{a}^{b}f(x,y)dx=\int\limits_{a}^{b}f(x,y_{0})dx=l(y_{0})$$
#### b. Tính khả vi
- Nếu:
	- $f(x,y)$ là hàm số liên tục trên $[a,b]\times[c,d]$
	- $f'_{y}(x,y)$ là àm số liên tục trên $[a,b]\times[c,d]$
thì $l(y)$ là hàm số khả vi trên $(c,d)$ và:$$l'(y)=\left(\int\limits_{a}^{b}f(x,y)dx\right)'_{y}=\int\limits_{a}^{b}f'_{y}(x,y)dx$$
#### c. Tính khả tích
- Nếu $f(x,y)$ là hàm số liên tục trên $[a,b]\times[c,d]$ thì $l(y)$ là hàm số khả tích trên $[c,d]$ và$$\int\limits_{c}^{d}l(y)dy=\int\limits_{c}^{d}\left(\int\limits_{a}^{b}f(x,y)dx\right)dy=\int\limits_{a}^{b}\left(\int\limits_{c}^{d}f(x,y)dy\right)dx$$
### 1.3 Tích phân phụ thuộc tham số với cận biến đổi
$$J(y)=\int\limits_{a(y)}^{b(y)}f(x,y)dx\;\text{with}\;y\in [c,d]$$
- Nếu:
	- $f(x,y)$ liên tục trên $[a,b]\times[c,d]$ 
	- $f'_{y}(x,y)$ là àm số liên tục trên $[a,b]\times[c,d]$
	- $a(y),b(y)$ liên tục trên $[a,b]\times[c,d]$ và $a\leq a(y),b(y)\leq b V y\in [c,d]$ thì $J(y)$ là một hàm số khả vi đối với $y$  trên $[c,d]$ và:$$J'(y)=\int\limits_{a(y)}^{b(y)}f'_{y}(x,y)dx+f(b(y),y)b'_{y}(y)-f(a(y),y)a'_{y}(y)$$





#### Một số phương pháp tính TPSR phụ thuộc tham số
##### I. Đạo hàm qua dấu tích phân
1. Tính $l'(y)$ bằng cách $l'(y)=\int\limits_{a}^{+\inf}f'_{y}(x,y)dx$
2. $l(y)$ bằng cách $l(y)=\int\limits l'(y)dy+C$ 
3.  Tính $l(y_{0})$ với một giá trị đặc biệt nào đó của $y_{0}$ để suy ra C
##### II. Đổi thứ tự lấy tích phân
1. Biểu diễn $f(x,y)=\int\limits_{c}^{d}F(x,y)dy$
2. Sử dụng tính chất đổi thứ tự lấy tích phân:$$\int\limits_{a}^{+\infty}f(x,y)dx=\int\limits_{a}^{+\infty}\left(\int\limits_{c}^{d}F(x,y)dy\right)dx=\int\limits_{c}^{d}\left(\int\limits_{a}^{+\infty}F(x,y)dx\right)dy$$
Chú ý: Phải kiểm tra điều kiện đổi thứ tự lấy tích phân

### 2.2 Tính chất
#### b. Tính khả vi
- Nếu 
	1. $f(x,y)$ và $f'_{y}(x,y)$ liên tục trên $[a,+\infty)\times [c,d]$ 
	2. $l(y)=\int\limits_{a}^{+\infty}f(x,y)dx$ hội tụ trên $[c,d]$
	3. $\int\limits_{a}^{+\infty}f(x,y)dx$ hội tụ đều trên $[c,d]$
	thì $l(y)$ là hàm số khả vi trên $[c,d]$ và $l'(y)=\int\limits_{a}^{+\infty}f'_{y}(x,y)dx$ 
## 3. Tích phân Euler
### 3.1 Hàm Gamma
$$\Gamma(p)=\int\limits_{0}^{+\infty}x^{p-1}e^{-x}dx$$ xác định trên: $(0,+\infty)$ 
- Các tính chất:
	1. Hạ bậc: $\Gamma(p+1)=p\Gamma(p)$ 
		Ý nghĩa: Chỉ cần nghiên cứu $\Gamma(p)$ với $0<p\leq 1$ mà thôi
		Nếu $\alpha\in(n,n+1]$ thì $\Gamma(\alpha)=(\alpha-1)(\alpha-2)...(\alpha-n)\Gamma(\alpha-n)$ 
		Đặc biệt: $\begin{cases}\Gamma(1)=1\\\Gamma(\frac{1}{2})=\sqrt(\pi)\end{cases}$ nên $\begin{cases}\Gamma(n)=(n-1)!\\\Gamma(n+\frac{1}{2}=\frac{(2n-1)!!}{2^{n}}\sqrt(\pi)\end{cases}$ 
	2. Đạo hàm của hàm Gamma: $\Gamma^{(k)}(p)=\int\limits_{0}^{+\infty}x^{p-1}(ln^{k}x)e^{-x}dx$ 
	3. $\Gamma(p)\Gamma(1-p)=\frac{\pi}{sin p\pi} \;\forall\; 0<p<1$ 
### 3.2 Hàm Beta
- Dạng 1: $B(p,q)=\int\limits_{0}^{1}x^{p-1}(1-x)^{q-1}dx$ 
- Dạng 2: $B(p,q)=\int\limits_{0}^{+\infty}\frac{x^{p-1}}{(1+x)^{p+q}}dx$
- Dạng 3: $B(p,q)=2\int\limits_{0}^{\frac{\pi}{2}}Sin^{2p-1}xCos^{2q-1}xdx$
Mối liên hệ giữa hàm Gamma và Beta:
	1. $B(p,q)=\frac{\Gamma(p)\Gamma(q)}{\Gamma(p+q)}$
	2. $B(p,1-p)=\Gamma(p)\Gamma(1-p)=\frac{\pi}{sin p\pi}$
Các tính chất:
	1. 