# Chương 4 - Tích phân đường
## I. Tích phân đường loại 1
### 1.1 Định nghĩa
- Cho $f=f(x,y)$ xác định trên đường cong C
	- Chia C một cách tuỳ ý ra n đường cong nhỏ, chia bởi các điểm A1,...
#### b. Tính chất
- Hàm liên tục trên cung $c_{y}$ bụ chặn, trơn từng khúc thì khả tích trên C.
- $L(c)=\int\limits_{c}1dl$ 
- $\int\limits_{C}a.fdl=a.\int\limits_{C}fdl$ 
- $\int\limits_{C}(f+g)dl=\int\limits_{C}fdl+\int\limits_{C}gdl$
- Tích phân đường loại 1 không phụ thuộc chiều lấy tích phân trên C
- ...
### 1.2 Cách tính
- *TH1:* $\begin{cases}y=y(x)\\ a\leq x \leq b\end{cases} \Rightarrow dl=\sqrt{1+(y')^{2}}dx$ 
	-  $\int\limits_{C}f(x,y)dl=\int\limits_{a}^{b}f(x,y(x)).\sqrt{1+(y'(x)^{2})}dx$ 
- *TH2:* Ngược lại TH1
- *TH3:* Cung C cho bởi phương trình tham số $x=x(t);y=y(t)$
	- $I=\int\limits_{I_{1}}^{I_{2}}f(x(t),y(t)).\sqrt{(x'(t)^{2})+(y'(t))^{2}}dl$ 
### 1.3 Ứng dụng
- Độ dài đường cong C được xác định bởi công thức: $$I(C)=\int\limits_{C}dl$$
## II. Tích phân đường loại 2
### 2.1 Định nghĩa
- $P=P(x,y);Q=Q(x,y)$ xác định trên đường cong C
- Chia C một cách tuỳ ý ra n đường cong nhỏ bởi các điểm $A_{0}(x_{0},y_{0}),...$
- Trên mỗi cung $A_{k}A_{k-1}$ lấy tuỳ ý một điểm $M_{k}(x_{k},y_{k})$
- Lập tổng tích phân: $$I_{n}=\sum\limits\limits_{i=0}^{n-1}(P(M_{k}).(x_{k+1}-x_{k})+Q(M_{k})(y_{k+1}-y_{k}))$$
### 2.2 Cách tính
$$I=\int\limits_{C}P(x,y)dx+Q(x,y)dy$$
- *TH1:* C=AB: $\begin{cases}y=y(x)\\ x:x_{A} \to x_{B}\end{cases}\Rightarrow dy=y(x)dx$ 
$$I+\int\limits_{x_{A}}^{x_{B}}[P(x,y(x))+Q(x,y(x))y'(x)]dx$$