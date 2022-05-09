### 3.1 Công suất, công và định lý động năng
#### 1. Công suất của một lực trong một hệ quy chiếu $R$
##### a. Định nghĩa
$$\begin{align}&\mathscr{P}(\overrightarrow{F})_{/R}=\overrightarrow{F}.\overrightarrow{v}(M)_{/R}\qquad(1)\\\text{hay}\;&\mathscr{P}=\overrightarrow{F}.\overrightarrow{v}\end{align}$$
- Đơn vị: $W$ ($1W = 1kg.m^2.s^{-3}$)
- ***Note: Hệ SI***:
	- *Chiều dài: m
	- *Khối lượng: kg
	- *Thời gian: s*
	- Lượng chất: mol
	- Nhiệt độ: K
	- *Đơn vị cường độ dòng điện: A
	- Độ sang: Calendar
##### b. Tính chất
- Công suất của một lực tiếp xúc không ma sát: $\mathscr{P}(\overrightarrow{F})_{/R}=\overrightarrow{R}.\overrightarrow{v}=0$
- Công suất có tính cộng được: $\mathscr{P}(\overrightarrow{F_1}+\overrightarrow{F_2})=(\overrightarrow{F_1}+\overrightarrow{F_2}).\overrightarrow{v}=\overrightarrow{F_1}.\overrightarrow{v}+\overrightarrow{F_2}.\overrightarrow{v}=\mathscr{P}.$ 
#### 2. Công của một lực trong hệ quy chiếu $R$
##### a. Định nghĩa
$$dW(\overrightarrow{F})=\mathscr{P}(\overrightarrow{F})_{/R}.dt=\overrightarrow{F}_{/R}.\overrightarrow{v}(M).dt=\overrightarrow{F}.d \overrightarrow{M}\qquad(2)$$
- $(d \overrightarrow{M}=d \overrightarrow{OM})$  với $d \overrightarrow{M}$ là vector chuyển dời nguyên tố của M
- Đơn vị:  $J$ ($1J=1kg.m^2.s^{-2}$)
- Còn được gọi là lưu thông nguyên tố của $\overrightarrow{F}$
- $d\overrightarrow{M}=dx.\overrightarrow{i}+dy.\overrightarrow{j}+dz.\overrightarrow{k}$ (Decartes)
##### b. Đặc điểm:
- Công có tính cộng được
- Công trong trường hợp chuyển dời hữu hạn: $W=\int_{t_1}^{t_2}\mathscr{P}(t).dt=\int_{M_1}^{M_2}\overrightarrow{F}.d \overrightarrow{M}$ 
	- Công của $\overrightarrow{F}$ là sự lưu thông của $\overrightarrow{F}$
- Công trong trường hợp của một lực không đổi: $W=\overrightarrow{F}.\overrightarrow{M_{1}M_{2}}$ 
#### 3. Định lý về công suất động học
$$\mathscr{P}(\overrightarrow{F})_{/R_g}=\frac{d\mathscr{E}_k}{dt}\qquad(3)$$
- ($\mathscr{E}_k(M)_{/R_g}\equiv\mathscr{E}_k=\frac{mv^2}{2}$)
- $$\begin{align}\overrightarrow{F}=m.\overrightarrow{a}\\\overrightarrow{v}.\overrightarrow{F}=\overrightarrow{v}.m.\overrightarrow{a}\\\mathscr{P}(\overrightarrow{F})_{/R_g}\equiv\overrightarrow{F}.\overrightarrow{v}=m.\overrightarrow{v}.\frac{d \overrightarrow{v}}{dt}=\frac{1}{dt}d(\frac{mv^2}{2})...\end{align}$$
#### 4. Định lý động năng
##### a. Phát biểu
$$W=\int_{t_1}^{t_2}dW=\int_{t_1}^{t_2}\mathscr{P}dt=\int_{M_1}^{M_2}\overrightarrow{F}.d.\overrightarrow{M}=\mathscr{E}_k(t_2)-\mathscr{E}_k(t_1)=\Delta\mathscr{E}_k\qquad(4)$$
- $W$ là công của lực tổng cộng áp dụng vào chất điểm $M$ trong khoảng thời gian $[t_1,t_2]$ 
- $W$ phụ thuộc vào quỹ đạo chuyển động của chất điểm
- $\Delta \mathscr{E}_k$ là độ biến thiên động năng giữa hai thời điểm $t_1,t_2$
$\Rightarrow$ $W=\Delta\mathscr{E}_k\qquad(4)$ 
##### b. Định lý về đọng năng và phương trình chuyển động
![[Pasted image 20220418163702.png]]
$$\overrightarrow{F}=-k.x.\overrightarrow{e_x}$$
$$\begin{align}&\mathscr{E}_k(t)-\mathscr{E}_{k}(0)=\frac{1}{2}m.v^{2}=\frac{1}{2}m(\frac{dx}{dt})^{2}=\int_{a}^{x}-kx'.dx'=\frac{1}{2}ka^{2}-\frac{1}{2}kx^2\\\Rightarrow&\dot{x}^2=-\omega_{0}^{2}.(x^{2}-a^{2})\\\frac{d}{dt}\Rightarrow&\dot{x}.(\ddot{x}+\omega_{0}^{2}.x)=0\end{align}$$
### 3.2 Trường lực bảo toàn và thế năng. Mối liên hệ giữa lực bảo toàn và thế năng.
#### 1. Các ví dụ mở đầu
#### 2. Thế năng
##### a. Hạt trong trường trọng lực đều
$$\begin{align}W&=-(mgz_2-mgz_1)\qquad(1)\\&=-(\mathscr{E}_{p_2}-\mathscr{E}_{p_1})\end{align}$$
![[Drawing 2022-04-18 16.45.16.excalidraw]]
$$\begin{align}dW=\overrightarrow{P}.d \overrightarrow{M}=-mg.dz=-d(mgz)=-d\mathscr{E}_p\\\overrightarrow{P}=m.\overrightarrow{g}=-mg.\overrightarrow{e_z};\;d.\overrightarrow{M}=dx.\overrightarrow{e_x}+dy.\overrightarrow{e_y}+dz.\overrightarrow{e_z}\end{align}$$
$$\mathscr{E}_p=mgz+cte\qquad(2)$$
- $W$ là công của trọng lực khi điểm $M$ đi từ điểm $M_1(z_1)$ đến điểm $M_2(z_2)$
- $\mathscr{E}_p$ là thế năng của trọng lực.
##### b. Lực phục hồi đàn hồi
$$\begin{align}W=-\left[\frac{1}{2}k(l_{2}-l_{0})^{2}-\frac{1}{2}k(l_{1}-l_{0})^{2}\right]\qquad(3)\\=-(\mathscr{E}_{p_2}-\mathscr{E}_{p_1})\end{align}$$
$$\begin{align}dW=\overrightarrow{F}.d \overrightarrow{M}=-k(l-l_{0}).\overrightarrow{e}.d(l.\overrightarrow{e})=-k(l-l_{0}).dl=-d\mathscr{E}_{p}\\\overrightarrow{F}=-k.(l-l_{0}).\overrightarrow{e}\;;\;d\overrightarrow{M}=d(l.\overrightarrow{e})\end{align}$$
$$\mathscr{E}_{p}=\frac{1}{2}k(l-l_{0})^{2}+cte\qquad(4)$$
- $\mathscr{E}_{p}$ là thế năng của lực đàn hồi
#### c. Định nghĩa
- Một trường lực, trong hệ quy chiếu $R_1$ được xuất ohats từ một thế năng nếu tồn tại một hàm số $\mathscr{E}_{p}(\overrightarrow{r})$ sao cho:$$dW=-d\mathscr{E}_p\qquad(5)\Rightarrow\mathscr{E}_p(\overrightarrow{r})$$
- $\mathscr{E}_p(\overrightarrow{r})$ là thế năng sinh ra(kết hợp với) trường lực đó
- $dW$ là công nguyên tố của lực
#### d. Tính chất
$$W=\int_{M_1}^{M_2}\overrightarrow{F}.d \overrightarrow{M}=\int_{M_1}^{M_2}-d\mathscr{E}_{p}=\mathscr{E}_{p}(M_{1})-\mathscr{E}_{p}(M_{2})\qquad(6)$$
- Công của một lực bảo toàn không phụ thuộc vào đường đi, chỉ phụ thuộc vào điểm đầu, điểm cuối
- Thế năng có tính cộng được (được sinh ra từ tính cộng được của các công)
#### e. Sự giải thích của vật lý về thế năng
- Thế năng biểu diên 1 năng lượng có thể gọi là năng lượng tích lũy
#### f. Biểu thuc của trường lực
$$\begin{align}\overrightarrow{F}&=-\overrightarrow{grad}\mathscr{E}_{p}(\overrightarrow{r})\\\overrightarrow{F}&=d \overrightarrow{M}\equiv dW=-d\mathscr{E}_{p}=-\overrightarrow{grad}\mathscr{E}_{p}.d \overrightarrow{M}\end{align}$$
### 3.3 Cơ năng trong hệ quy chiếu Galile và định luật bảo toàn cơ năng
#### 1. Cơ năng của 1 chất điển trong 1 HQC Galile $R_g$
$$\mathscr{E}_M=\mathscr{E}_p+\mathscr{E}_{k}$$
- $\mathscr{E}_M$ là cơ năng của chất điểm trong $R_g$
#### 2. Sự vận động bảo toàn và tích phàn đầu của năng lượng
- Chất điểm vận động bảo toàn trong $R_g$
$$\mathscr{E}_M= cte$$
B T: AD4 , BT1,7.