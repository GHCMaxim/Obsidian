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
