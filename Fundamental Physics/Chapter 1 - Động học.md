# Động học
### Mục tiêu chính:
- Xác định vị trí một biến cố trong không gian và thời gian
- Các hệ toạ độ thường dùng
- Đạo hàm của 1 đại lượng vector
- Khái niệm về hệ quy chiếu
- Các biểu thức vector vận tốc và vector gia tốc của một động điểm.
- Xác định quỹ đạo và thời gian quãng đường đi

### I. Hệ quy chiếu:
#### 1. Chuyển động của một vật
- Là sự chuyển dời của 1 vật đó đối với các vật khác trong không gian và thời gian
#### 2. Hệ quy chiếu
- = Mốc (Gắn hệ toạ độ) + Thời gian
#### 3. Chuyển động có tính tương đối
- Phụ thuộc vào người quan sát
#### 4. Không gian và thời gian trong cơ học cổ điển
-  CHCD là lý thuyết xác định dựa trên quan điểm về không gian, thời gian và chuyển động của Newton
- ![[Drawing 2022-04-09 17.46.53.excalidraw.png|400]]
- **Thời gian** có tính **tuyệt đối**.
- **Khoảng thời gian** giữa 2 biến cố không phụ thuộc vào hệ quy chiếu
- **Hệ toạ độ thời gian = thời điểm gốc + 1 định vị thời gian**
=> t: Số đơn vị thời gian kể từ thời điểm gốc
- **Vị trí không gian** có tính **tương đối**
$$x = x' + \overline{OO'}; y = y'; z = z' $$
- **Khoảng không gian** có tính **tuyệt đối**
$$ l \equiv x_B - x_A = x'_B - x'_A \equiv l_0 $$
### II. Vector vị trí của 1 điểm trong các hệ toạ độ Decartes, trụ, cầu
#### 1. Vector Vị trí
- Vector vị tí của M: $\overrightarrow{r} = \overrightarrow{OM}$
#### 2. Cơ sở Vector
- ($\overrightarrow{e_1};\overrightarrow{e_2};\overrightarrow{e_3}$) là 1 cơ sở vector chuẩn hoá
- ![[Pasted image 20220409190740.png]]
- Một vector $\overrightarrow{u}$ được phân tích một cách duy nhất: $\overrightarrow{u}=u_1\overrightarrow{e_1}+u_2\overrightarrow{e_2}+u_3\overrightarrow{e_3}$
- ($\overrightarrow{e_1};\overrightarrow{e_2};\overrightarrow{e_3}$) là 1 cơ sở vector trực giao, chuẩn hoá thuận: 
	$$\begin{align}
	\overrightarrow{e_3} = \overrightarrow{e_1} \wedge \overrightarrow{e_2}\\
	\overrightarrow{e_1} = \overrightarrow{e_2} \wedge \overrightarrow{e_3}\\
	\overrightarrow{e_2} = \overrightarrow{e_3} \wedge \overrightarrow{e_1}
	\end{align}$$
#### 3. Góc ở trong mặt phẳng
- Quy ước: Quy tắc bàn tay phải:
![[Pasted image 20220409191247.png]]
#### 4. Vector vị trí của 1 điểm trong hệ toạ độ thông thường
##### a. Hệ toạ độ Decartes
- Hệ toạ độ trực chuẩn thuận
- Cơ sở địa phương $(\overrightarrow{e_x};\overrightarrow{e_y};\overrightarrow{e_z})$ gắn với điểm O cố định
-  Vector vị trí của M: $\overrightarrow{r}=\overrightarrow{OM}=x.\overrightarrow{e_x}+y\overrightarrow{e_y}+z.\overrightarrow{e_z}$ 
- Các toạ độ của điểm $M(x,y,z)$ xác định duy nhất 1 điểm M và ngược lại.
- ![[Pasted image 20220410201502.png]]
##### b. Hệ toạ độ trụ
- Hệ toạ độ trực chuẩn thuận
- Cơ sở địa phương $(\overrightarrow{e_r},\overrightarrow{e_\theta},\overrightarrow{e_z})$  gắn với M
	- $\overrightarrow{e_r}:\overrightarrow{OH}=r.\overrightarrow{e_r}$
	- $\overrightarrow{e_\theta}=\overrightarrow{e_z}\wedge\overrightarrow{e_r}$ 
- Vector vị trí của M: $\overrightarrow{OM}=r.\overrightarrow{e_r}+z.\overrightarrow{e_z}$ 
- Cắc toạ độ trụ của M: $$\begin{align}&r=OH;r>0\\&\theta=(\overrightarrow{e_x},\overrightarrow{OH}), \overrightarrow{e_z}(+)\\&z:\text{Toạ độ Decartes thứ 3}\end{align}$$
- $(r,\theta,z)$ xác định duy nhất 1 M
- Chú ý:
	- $\overrightarrow{e_r};\overrightarrow{e_\theta}\;//\;Oxy$
	- $\overrightarrow{e_\theta}$ chỉ về hướng $\theta$ tăng
-  ![[Pasted image 20220410201904.png]]
##### c. Hệ toạ độ cực
- Khi điểm M chuyển động trong mặt phẳng P:
	- Cần 2 toạ độ để xác định M:
		- $\overrightarrow{OM}=r.\overrightarrow{e_r}$
		- $\theta=(\overrightarrow{e_x};\overrightarrow{e_r})\;,\;\overrightarrow{e_z} (+)$ 
		- $\overrightarrow{OM}=x.\overrightarrow{e_x}+y.\overrightarrow{e_y}$ 
![[Pasted image 20220411001008.png]]
##### d. Liên hệ toạ độ trụ, Decartes
$$\begin{align}&\overrightarrow{e_r}=Cos\theta.\overrightarrow{e_x}+Sin\theta.\overrightarrow{e_y}\\&\overrightarrow{e_\theta}=-Sin\theta.\overrightarrow{e_x}+Cos\theta.\overrightarrow{e_y}\\&\overrightarrow{e_z}=\overrightarrow{e_x}\wedge\overrightarrow{e_y}=\overrightarrow{e_r}\wedge\overrightarrow{e_\theta}\\&x=rCos\theta\ ;\; y=Sin\theta\\& r=\sqrt{x^2+y^2}\end{align}$$
##### e. Hệ toạ độ cầu
- Hệ toạ độ trực chuẩn thuận
- Cơ sở địa phương trực chuẩn $(\overrightarrow{e_r};\overrightarrow{e_\theta};\overrightarrow{e_\varphi})$ 
	- $\overrightarrow{e_r}:\overrightarrow{OM}=r.\overrightarrow{e_r}$
	- $\overrightarrow{e_\varphi}=\frac{\overrightarrow{e_z}.\overrightarrow{OH}}{OH}=\overrightarrow{e_z}\wedge\overrightarrow{u}$ 
	- $\overrightarrow{e_\theta}=\overrightarrow{e_\varphi}.\overrightarrow{e_r}$ 
- Vector vị trí của M: $\overrightarrow{OM}=r.\overrightarrow{e_r}$ 
- Các toạ độ cầu:
	- $r=OM\;;\;r>0$
	- $\theta=(\overrightarrow{e_z};\overrightarrow{e_r}), \overrightarrow{e_\varphi}\;(+)$ 
	- $\varphi=(\overrightarrow{e_x},\overrightarrow{OH}),\overrightarrow{e_z}\;(+)$   
- $(r,\theta,\varphi)$ xác định duy nhất 1 M
- 1 M có vô số toạ độ $(r,2n\pi+\theta,2m\pi+\varphi)$ 
- Chú ý:
	- $\overrightarrow{e_\varphi}\;//\;Oxy$
	- $\overrightarrow{e_\theta}\;//\;(Oxy);OM$ 
![[Pasted image 20220411003618.png]]
##### f. Liên hệ toạ độ cầu, Decartes
$$\begin{align}&\overrightarrow{e_r}=Sin\theta.Cos\varphi.\overrightarrow{e_x}+Sin\theta.Sin\varphi.\overrightarrow{e_y}+Cos\theta.\overrightarrow{e_z}\\&\overrightarrow{e_\varphi}=\overrightarrow{e_z}\wedge\overrightarrow{u}=-Sin\varphi.\overrightarrow{e_x}+Cos\varphi.\overrightarrow{e_y}\\&\overrightarrow{e_\theta}=\overrightarrow{e_\varphi}\wedge\overrightarrow{e_r}=Cos\theta.Cos\varphi.\overrightarrow{e_x}+Cos\theta.Sin\varphi\overrightarrow{e_y}-Sin\theta.\overrightarrow{e_z}\\\\&x=rSin\theta.Cos\varphi\;;\;y=r.Sin\theta.Sin\varphi\;;\;z=r.Cos\theta\end{align}$$
### III. Đạo hàm 1 vector
#### 1. Định nghĩa
- $\overrightarrow{U}_{\xi}$ là 1 vector phụ thuộc vào $\xi$
- Đạo hàm của $\overrightarrow{U}_\xi$ đối với $\xi$: $$\frac{d\overrightarrow{u}}{d\xi}=\lim_{\Delta\xi \to 0}{\frac{\overrightarrow{U}(\xi+\Delta\xi)-\overrightarrow{U}(\xi)}{\Delta\xi}}$$
- Đạo hàm của 1 vector thuộc hệ quy chiếu:
$$\frac{d\overrightarrow{U}}{d(\xi)_{/R}}$$
#### 2. Tính chất
#### 3. Đạo hàm của 1 vector có độ dài không đổi
- $\overrightarrow{U}_{\xi}$ là một vector có độ dài không đổi những hướng có thể thay đổi:$$\frac{dU^2}{d\xi}=\frac{d}{d\xi}(\overrightarrow{u},\overrightarrow{u})=0$$
- Trong hệ Decartes:$$\begin{align}\overrightarrow{U}_{(\xi)}=U_x.\overrightarrow{e_x}+U_{y}.\overrightarrow{e_{y}}+U_z.\overrightarrow{e_{z}}\\\Rightarrow(\frac{dU}{d\xi})_{/R}=\frac{dU_x}{d\xi}.\overrightarrow{e_x}...\end{align}$$
#### 5. Đạo hàm của các vector của cơ sở địa phương trong toạ độ trụ
$$\begin{align}
\overrightarrow{e_r}=Cos\theta.\overrightarrow{e_x}+Sin\theta.\overrightarrow{e_y}\\
\overrightarrow{e_\theta}=-Sin\theta e_x+Cos\theta e_y\\
\Rightarrow \left(\frac{d.\overrightarrow{e_r}}{d\theta}\right)_{/R}=\overrightarrow{e_\theta}\\
\Rightarrow \left(\frac{d.\overrightarrow{e_{\theta}}}{d\theta }\right)_{/R}=-\overrightarrow{e_{r}}
\end{align}$$
#### 6. Đạo hàm của vector của cơ sở địa phương trong toạ độ cầu
$$\begin{align*}
&\frac{d \overrightarrow{e_r}}{d\theta}=\overrightarrow{e_{\theta}}\\\\
&\frac{d \overrightarrow{e_{r}}}{d\varphi}=- \overrightarrow{e_r}\\
&\frac{d \overrightarrow{e_{r}}}{d\varphi}=Sin\theta.\overrightarrow{e_{\varphi}}\\
&\frac{d \overrightarrow{e_{\theta}}}{d\varphi}=Cos\theta.\overrightarrow{e_{\varphi}}
\end{align*}$$
### IV. Vector vận tốc trong hệ toạ độ Decartes, trụ, cầu
#### 1. Định nghĩa:
$$\overrightarrow{v}(M)_{/R}=\left(\frac{d \overrightarrow{OM}}{dt}\right)_{/R}$$
#### 2. Decartes:
$$\overrightarrow{v}(M)_{/R}=\left(\frac{d \overrightarrow{OM}}{dt}\right)_{/R}=\frac{dx}{dt}\overrightarrow{e_{x}}+\frac{dy}{dt}\overrightarrow{e_{y}}+\frac{dz}{dt}\overrightarrow{e_{z}}$$
hay:
	 $\begin{align}\overrightarrow{v}(M)&=x.\overrightarrow{e_{x}}+y.\overrightarrow{e_{y}}+z.\overrightarrow{e_{z}}\\&=\overrightarrow{v_{x}}+\overrightarrow{v_{y}}+\overrightarrow{v_{z}}\end{align}$
$\Rightarrow \overrightarrow{v}(M)=\sqrt{v_{x}^{2}+v_{y}^{2}+v_{z}^{2}}=\sqrt{x^{2}+y^{2}+z^{2}}$ 
#### 3. Trụ:
$$\begin{align}
&\overrightarrow{OM}=r.\overrightarrow{e_r}+z.\overrightarrow{e_{z}}\\
&\overrightarrow{v}(M)_{/R}=\left(\frac{d.\overrightarrow{OM}}{dt}\right)=r.\overrightarrow{e_r}+r.\dot{\theta}.\overrightarrow{e_\theta}+z.\overrightarrow{e_{z}}=\overrightarrow{v_{r}}+\overrightarrow{v_{\theta}}+\overrightarrow{v_{z}}\\
&\frac{d \overrightarrow{e_{r}}}{dt}_{/R}=\frac{d.\overrightarrow{e_r}}{d\theta}.\frac{d\theta}{dt}=\ddot\theta.\overrightarrow{e_{\theta}}\\
&\Rightarrow \overrightarrow{v}(M)=\sqrt{\overrightarrow{v_{r}}^2+\overrightarrow{v_{\theta}}^{2}+\overrightarrow{v_{z}}^{2}}=\sqrt{\ddot{r}^{2}+\dot{r}^{2}\dot{\theta}^2+\ddot{z}^2}\\
\end{align}$$