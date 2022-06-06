## Chương 3: Điện thế
### 3.1 Tính chất thế của trường tĩnh điện
#### 1. Lưu số của trường tĩnh điện
- Lưu số của một trường vector $\overrightarrow{E}$  trên đường cong I' (nối liền 2 điểm A và B), từ A tới B được xác định bởi:$$C_{AB(I')}=\int\limits_{A(I')}^{B}\overrightarrow{E}.d \overrightarrow{l}$$
#### 2. Sự bảo tàn lưu số của trường tĩnh điện
##### a. Trường tĩnh điện gây ra bởi một điện tích điểm
$$\overrightarrow{E}(\overrightarrow{r})=\frac{q}{4\pi\epsilon_0}.\frac{\overrightarrow{e}_{r}}{r^{2}}$$
Trường tĩnh điện $\overrightarrow{E}$  tạo ra trong không gian bởi một điện tích điểm q(đặt tại điểm gốc O cố định của hệ toạ độ cầu)
$\Rightarrow$ Lưu số từ A đến B trên đường cong $I'$ (Không đi qua O):$$C_{AB(I')}=\int\limits_{A(I')}^{B}\overrightarrow{E}.d \overrightarrow{r}=\frac{q}{4\pi\epsilon_0}\left(\frac{1}{r_A}-\frac{1}{r_B}\right)=C_{AB(I^")}$$
$\Rightarrow$ Lưu số của trường tĩnh điện $\overrightarrow{E}$ gây bởi một điện tích điểm $q$ được bảo toàn
#### 3. Lưu số của trường tĩnh điện dọc theo một đường cong kín
$$\begin{align}
C_{AB(I')}=\int\limits_{A(I')}^{B}\overrightarrow{E}.d \overrightarrow{r}=\frac{q}{4\pi\epsilon_0}\left(\frac{1}{r_A}-\frac{1}{r_B}\right)\\
C_{AB(I')}=\int\limits_{A(I')}^{B}\overrightarrow{E}.d \overrightarrow{l}=\int\limits_{A(I^")}^{B}\overrightarrow{E}.d.\overrightarrow{l}==C_{AB(I^")}\\

\end{align}$$
## 3.2 Liên hệ giữa điện trường và điện thế
### 1. Điện thế (Thế tĩnh điện)
- **Định nghĩa:** Hàm $V(\overrightarrow{r})$ xác định bởi: $V_B=V_A+\int\limits_A^B-\overrightarrow{E}.d.\overrightarrow{l}$  được gọi là **hàm thế tích điện**
- **Hiệu điện thế** giữa hai điểm A và B:$$V_{A}-V_{B}=\int\limits_{A}^{B}\overrightarrow{E}.d \overrightarrow{l}$$
### 2. Liên hệ giữa điện trường và điện thế
$$V_{A}-V_{B}=\int\limits_{A}^{B}\overrightarrow{E}.d \overrightarrow{l}\qquad \Rightarrow \qquad\overrightarrow{E}.d \overrightarrow{l}=-dV$$
- Trường tĩnh điện là trường có Gradiant: $$\overrightarrow{E}=-\overrightarrow{\text{grad}}_{M}V(M)$$
- Một trường vector $\overrightarrow{E}$ có lưu số bảo toàn là một trường có gradient
### 3. Sự bất biến với mức (jauge)
- Thế tĩnh điện được xác định sai khác một hằng số: $$V'(\overrightarrow{r})=V(\overrightarrow{r})+V_{0'} (V_{0}=cte)$$
- Để xác định giá trị cụ thể của thế tĩnh điện, cần chọn mức (chọn gốc nơi thế tĩnh điện = 0)
$\Rightarrow$ Trường tĩnh điện là bất biến với mức, nghĩa là với mốc để tính thế tĩnh điện
## 3.3 Điện thế gay bởi điện tích điểm, hệ điện tích điểm, hệ điện tích phân bố liên tục
### 1. Điện thế gây bởi 1 điện tích điểm
$$\overrightarrow{E}(\overrightarrow{r})=\frac{q}{4\pi\epsilon_0}.\frac{\overrightarrow{e}_{r}}{r^{2}}$$
$$\Rightarrow-dV(\overrightarrow{r})=\overrightarrow{E}.d \overrightarrow{r}=\frac{q}{4\pi\epsilon_{0}}.d(\frac{-1}{r})$$
$$\Rightarrow V(M)=\frac{q}{4\pi\epsilon_{0}.r}+cte$$
### 2. Điện thế gây bởi hệ điện tích điểm
$$V(M)=\frac{1}{4\pi\epsilon_{0}}\sum\limits_{i=1}^{N} \frac{q_{i}}{P_{i}M}+cte$$
### 3. Điện thế gây bởi điện tích phân bố liên tục
$$\overrightarrow{E}_{\mathscr{D}}(M)=\frac{1}{4\pi\epsilon_{0}}\sum\limits_{P\in\mathscr{D}}dq_{p}. \frac{\overrightarrow{PM}}{PM^{3}} $$
$$\delta V(M)=\frac{1}{4\pi\epsilon_{0}}. \frac{dq_{p}}{PM}$$
$$V(M)=\iiint\limits_\mathscr{D} \frac{1}{4\pi\epsilon_{0}} \frac{\rho(P).d\tau}{PM}$$
- Phân bố theo bề mặt: $dq_{p}=\sigma(P).dS$
$$V(M)=\iint\limits_\mathscr{D} \frac{1}{4\pi\epsilon_{0}} \frac{\sigma(P).dS}{PM}$$
- Phân bố theo chiều dài: $dq_{p}=\lambda(P).dl$
$$V(M)=\iint\limits_\mathscr{D} \frac{1}{4\pi\epsilon_{0}} \frac{\lambda(P).dl}{PM}$$
## 3.4 Thế năng tương tác tĩnh điện
### 1. Thế năng của một điện tích điểm đặt trong 1 trường
#### a. Công của lực tĩnh điện
$$\delta \,W=-q.dV$$
$\Rightarrow$ Công của lực $\overrightarrow{f}$  ứng với chuyển dời của điện tích q từ A tới B:
$$W_{AB}=\int\limits_{A}^{B}\delta\,W=\int\limits_{V_{A}}^{V_{B}}-q.dV=-q(V_{B}-V_{A})$$
	- Không phụ thuộc đường đi I' để đi từ A đến B
	- Chỉ phụ thuộc vị trí của điện tích (A và B)
$\Rightarrow$ Trường tĩnh điện có tính chất thế
#### b. Thế năng
- Thế năng tương tác giữa một điện tích q và một trường tĩnh điện $\overrightarrow{E}$ (tạo ra điện thế V) bằng: $\mathscr{E}_{p}=q.V$ 
- Lực Coulomb $\overrightarrow{f}=q.\overrightarrow{E}$ do trường tĩnh điện tác dụng lên điện tích q dẫn xuất từ thế năng này, được xác định bởi: $$\overrightarrow{f}=q.\overrightarrow{E}=-\overrightarrow{\text{grad}}\;\mathscr{E}_{p}$$
$$\delta \,W=\overrightarrow{f}.d \overrightarrow{M}=q.\overrightarrow{E}.d \overrightarrow{M}=-d(q.V)=-d.\mathscr{E}_p$$
$$W_{AB}=-q(V_{B}-V_{A})=-\mathscr{E}_{p}(B)+\mathscr{E}_{p}(A)=-\Delta\mathscr{E}_{p}$$
### 2. Năng lượng tương tác của hai điện tích điểm
#### a. Công để thành lập hệ hai điện tích
$$W_{OP}=q_{2}.V_{1}(M_{2})= \frac{q_{1}.q_{2}}{4\pi\epsilon_{0}.M_{1}M_{2}}$$

#### b. 
$$\mathscr{E}_{p_{12}}=q_{1}.V_{2}(M_{1})=q_{2}.V_{1}(M_{2})=\frac{1}{2}[q_{1}.V_{2}(M_{1})+q_{2}.V_{1}(M_{2})]$$