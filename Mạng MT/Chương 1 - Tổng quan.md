![[Chương 1 - Tổng quan.pdf]]
### Cơ bản về mạng máy tính
#### Mạng máy tính:
- Là tập hợp các máy tính kết nối với nhau dựa trên 1 kiến trúc nào đó để có thể trao đỏi dữ liệu
	- Máy tính: máy trạm, máy chủ, bộ định tuyến
	- Kết nối = 1 phương tiện truyền theo 1 kiến trúc mạng
#### Giao thức mạng (Internet Protocol):
- Là một quy tắc để truyền thông tin trong đó bao gồm:
	- Gửi một yêu cầu hoặc thông tin
	- Nhận một thông tin hoặc yêu cầu hành động
	- Các yêu cầu, thông tin được gửi dưới dạng thông điệp
- Định nghĩa 
	- Khuôn dạng dữ liệu, thông điệp 
	- Thứ tự truyền, nhận thông điệp giữa các thực thể trên mạng  
	- Các hành động tương ứng khi nhận được thông điệp
#### Đường truyền vật lý
- Là các phương tiện vật lý có khả năng truyền dẫn tín hiệu gồm 2 loại:
	- Hữu tuyến (cáp)
	- Vô tuyến (sóng)
- Một số thông số thông dụng:
	- *Băng tần* : Độ rộng thần số tín hiệu có thể truyền đi
		- $f_{min}$: Tần số nhỏ nhất
		- $f_{max}$: Tần số lớn nhất
		- $f_{max} - f_{min}$ : Băng tần
	- Bit Error Rate/Ratio (BER)
	- Độ suy hao: Mức suy giảm tín hiệu khi truyền
#### Phân loại mạng máy tính:

|                     | Mạng cá nhân | Mạng cục bộ           | Mạng đô thị            | Mạng diện rộng      |
| ------------------- | ------------ | --------------------- | ---------------------- | ------------------- |
| Phạm vi kết nối     | vài chục m   | vài km                | hàng trăm km           | vài nghìn km        |
| Số lượng người dùng | 1 - 1e2      | 10 - 1e6              | 1e7+                   | 1e8+                |
| Mục đích phục vụ    | Cho cá nhân  | Cho gia đình, tổ chức | Cho thành phố, khu vực | The internet itself |

### Kiến trúc mạng
#### Mạng Internet
-  Trên 5 tỉ thiết bị kết nối  
- 3.2 tỉ người dùng(40%)  
- Đường truyền: cáp quang, cáp đồng, Wimax, 3G…  
- Truyền tải ~3x109 GB mỗi ngày  
- Dịch vụ: Web, email, mạng xã hội, Skype…
#### Network of Networks
- Không có khả năng mở rộng $\Rightarrow$ Số lượng kết nối sẽ là $O(n^2)$ 
	$\Rightarrow$ Giải quyết bằng kết nối mạng vào 1 trạm chuyển tiếp của 1 nhà cung cấp toàn cầu (ISP)
	- Nhiều ISP thì cần có trạm trung chuyển giữa chúng
	- Thêm mạng khu vực (Regional net) kết nối với các ISP toàn cầu
	- Mạng lõi sẽ bao gồm các ISP và Regional Net
	- Mạng biên: 
		- Nút mạng đầu cuối (end-system, hosts): PC, phones, servers, ...
		- Mạng truy nhập (Access Networks): Router, Switch, hub, ...
### Chuyển mạch gói/kênh
#### Các công thức, thông số cần nhớ:
- **Bandwidth (R)**: Lượng dữ liệu truyền tối đa trong 1 đơn vị thời gian (Mbps)
- **Latency**: Thời gian truyền dữ liệu từ A $\rightarrow$ B
	- **Trễ truyền dẫn (Propagation delay)** : $$D_{PR} = \frac{D}{S}$$
		- $D$ : Độ dài đường truyền
		- $S$ : Tốc độ tín hiệu (usually Speed of light $3*10^{8}$ m/s)
	- **Trễ truyền tin (Tranmission delay)**: $$D_{T}= \frac{N_{B}}{R}$$
		- $N_{B}$ : Kích thước dữ liệu
		- $R$ : Băng thông
	
Example: Tranfering 100Bytes from A to B, given:
	- R = 1Mbps
	- D = 200km
	- S = 1ms
- Time to transfer 1 bit with 0 delay: $\frac{1}{10^{6}}$s $\Rightarrow$ Time to transfer 800bits: $800* \frac{1}{10^{6}}$s
- Time for first bit to reach B: $\frac{1}{10^{6}}+ \frac{1}{10^{3}}$
$\Rightarrow$ Time for final bit to reach B: $800$...


