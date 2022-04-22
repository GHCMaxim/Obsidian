### 1. Dạng 1: Tích phân trên miền Hình chữ nhật
- Basics:
	- $$\int_{a}^{b}dx\int_{c}^{d}f(x,y)dy=\int_{a}^{b}\int_{c}^{d}(f(x,y)dy)dx$$
	- $$\int_{c}^{d}dy\int_{a}^{b}f(x,y)dy=\int_{c}^{d}\int_{a}^{b}(f(x,y)dx)dy$$
- Example: $\iint\limits_{D}(3y^{2}-x)dxdy$ với $D=\{ 0\leq x\leq 2\; ;\;1\leq y\leq 2 \}$   
	$$\begin{align}&= \int_{1}^{2}dy\int_{0}^{2}(3y^{2}-x)dx\\&=\int_{1}^{2}\left[\left(3y^{2}x-\frac{x^{2}}{2}\right)\Biggr|_{0}^{2}\right]dy\\&=\int_{1}^{2}(6y^{2}-2)dy\\&=(2y^3-2y)\Biggr|_{1}^{2}\\&=12\end{align}$$
	Note: Hoàn toàn có thể đặt ngược lại.
- Chú ý: Nếu $f(x,y)=f_{1}(x).f_{2}(y)$ . $D$ là hình chữ nhật$\begin{cases}a\leq x \leq b\\c \leq y \leq d\end{cases}$ $$\int_{a}^{b}\int_{c}^{d}f(x,y)dxdy=\int_{a}^{b}f_{1}(x)dx\;.\;\int_{c}^{d}f_{2}(y)dy$$
- Example 2: $\iint\limits_{D}(SinxCosy)dxdy$ 
	-  $$\Rightarrow D:\begin{cases}0\leq x \leq \frac{\pi}{2}\\0\leq y\leq \frac{\pi}{2} \end{cases}$$
	- $$\Rightarrow \iint\limits_{D}(SinxCosy)dxdy=\int_{0}^{\frac{\pi}{2}}Sinx\;dx\;.\;\int_{0}^{\frac{\pi}{2}}Cosy\;dy$$
