## Chương 4 - Định lý Gauss
### 4.1 Thông lượng của trường tĩnh điện gây bởi một điện tích điểm
#### 1. Định nghĩa
##### a. Thông lượng trường tĩnh điện $\overrightarrow{E}$ qua một điện tích nguyên tố $dS$
$$D\phi=\overrightarrow{E}.\overrightarrow{dS}=E.dS.cos\alpha$$
![[IMG_20220613_160828.jpg]]

Thông lượng của trường tĩnh điện $E$ của một điện tích q nằm tại O, qua một điện tích nguyên tố, liên kết với góc đặc đại số dưới đó từ O, nhìn diện tích dS định hướng, bởi hệ thức:$$d\phi=\overrightarrow{E}.\overrightarrow{dS}=\frac{q}{4\pi\epsilon_{0}}.d\Omega$$
$$d\Omega=dS.\frac{cos\alpha}{r^{2}}=dS. \frac{\overrightarrow{n}.\overrightarrow{e}_{r}}{r^{2}}$$

![[IMG_20220613_161045.jpg]]
##### b. Thông lượng trường tĩnh điện $\overrightarrow{E}$ qua một mặt kín $S$
$$\phi=\oint_{S}\overrightarrow{E}.\overrightarrow{dS}=\oint_{S}\overrightarrow{E}.\overrightarrow{n}_{\text{ext}}.dS$$
#### 2. Quy ước về định hướng của một mặt kín
##### a. Thông lượng của trường qua một mặt kín chứa điện tích $q$
$$\phi=\oint_{S}\overrightarrow{E}.\overrightarrow{n}_{\text{ext}}.dS=\frac{q}{\epsilon_{0}}$$
##### b. Thông lượng của trường qua một mặt kín không chứa điện tích
$$\phi= \oint_{S}\overrightarrow{E}.\overrightarrow{n}_{\text{ext}}.dS=0$$
- Mặt kín S bao quanh điện tích q:$\phi_{1}=\phi_{2}=\phi_{3}=\frac{q}{\epsilon_{0}}$
- ...
### 4.2 Định lý Gauss
#### 1. Dạng tích phân
Thông lượng của trường của một phân bố $\mathscr{D}$ gửi qua một mặt kín $S$ bằng điện tích của $\mathscr{D}$ nằm ở bên trong $S$ chi cho $\epsilon_{0}$ :$$\phi=\oint_{S}\overrightarrow{E}.\overrightarrow{dS}= \frac{Q_{\text{int}}}{\epsilon_{0}}$$
#### 2. Dạng vi phân
$$\text{div}\overrightarrow{E}=\frac{\rho}{\epsilon_{0}}$$
$$\Delta V + \frac{\rho}{\epsilon_{0}}=0$$
- Xét một vật dẫn ở trạng thái cân bằng tĩnh điện
- Tại một điểm M rất gần một điểm Q nằm trên bề mặt ngoài của một vật dẫn, với mật độ điện mặt $\sigma(Q)$ , trường tĩnh điện xác định bởi: $$\overrightarrow{E}(M)= \frac{\sigma(Q)}{\epsilon_{0}}.\overrightarrow{n}(Q)$$
- Bề mặt của một vật dẫn là một mặt đẳng thế
### 4.3 Áp dụng định lý Gauss để tính điện trường gây bởi các phân bố có tính đối xứng cao
#### 1. Các bước thực hiện:
1. Nhận xét về tính đối xứng
2. Chọn mặt Gauss
3. Áp dụng định lý Gauss
#### 2. Ví dụ áp dụng
##### a. Phân bố có tính đối xứng phẳng
- *Bài toán*: Xác định trường tạo bởi một lớp phẳng vô hạn, bề dày $e$ và có mật độ điện khối $\rho$
	- (1) Nhận xét về tính đối xứng: $$\begin{align}\overrightarrow{E}(x,y,z)=E(x,y,z).\overrightarrow{e_{z}}=E(z).\overrightarrow{e_{z}}\\E(-z)=-E(z)\end{align}$$
	- (2) Chọn mặt Gauss: $$\begin{align}&\phi=\oint_{S}\overrightarrow{E}.\overrightarrow{dS}=S.E(z)-S.E(-z)=2.S.E(z)\qquad(**)
	\\
	& Q_{\text{int}}=\begin{cases}\rho.S.2z \; si\; 0\leq |z| \leq \frac{e}{2}\\ \\
\rho.S.e\;si\; \frac{e}{2}\leq|z|\end{cases} 
	\end{align}$$
	- *Kết luận 1:* Trường tạo bởi một lớp phẳng vô hạn, dày e và có mật dộ điện khối $\rho$: $$\overrightarrow{E(z)}=\begin{cases}(\frac{\rho.z}{\epsilon_{0}}).\overrightarrow{e_z}\;si\;0\leq|z|\leq \frac{e}{2}\\ \\
(\frac{\rho.e}{2.\epsilon_{0}}).\overrightarrow{e_{z}}\;si\; \frac{e}{2}\leq z\\ \\
\frac{-\rho.e}{2.\epsilon_{0}}.\overrightarrow{e_z}\;si\;z\leq- \frac{e}{2}\end{cases}\Rightarrow V=\begin{cases} \frac{-\rho.z^{2}}{2.\epsilon_{0}}\;si\;0\leq|z|\leq \frac{e}{2}\\...\end{cases}$$

![[IMG_20220613_163722.jpg]]- *Bài toán 2:* Xác định trường tạo bởi một mặt phẳng vô hạn, có mât độ điện mặt $\rho$
#### b. Phân bố có tính đối xứng trụ
- *Bài toán 1:* Xác định trường tạo bởi một khối trụ dài vô hạn có trục (Oz), có bán kính R và có mật độ điện khối $\rho$
