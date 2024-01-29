![[Chương 1 - Tổng quan.pdf]]
### Cơ bản về mạng máy tính
#### Khái niệm cơ bản

##### Mạng máy tính:
- Là tập hợp các máy tính kết nối với nhau dựa trên 1 kiến trúc nào đó để có thể trao đỏi dữ liệu
	- Máy tính: máy trạm, máy chủ, bộ định tuyến
	- Kết nối = 1 phương tiện truyền theo 1 kiến trúc mạng
##### Mô hình truyền thông
![[Pasted image 20240129120332.png]]
##### Giao thức mạng (Internet Protocol):
- Là một quy tắc để truyền thông tin trong đó bao gồm:
	- Gửi một yêu cầu hoặc thông tin
	- Nhận một thông tin hoặc yêu cầu hành động
	- Các yêu cầu, thông tin được gửi dưới dạng thông điệp
- Định nghĩa 
	- Khuôn dạng dữ liệu, thông điệp 
	- Thứ tự truyền, nhận thông điệp giữa các thực thể trên mạng  
	- Các hành động tương ứng khi nhận được thông điệp
##### Đường truyền vật lý
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
##### Kiến trúc mạng
Bao gồm:
- Hình trạng (Topology): Cách thức kết nối của các nút mạng
	- Vật lý: Dựa trên cáp kết nối
	- Logic: Dựa trên cách thức truyền tín hiệu: Point - Point, Point - Multiple Points
- Giao thức (Protocol): Cách thức trao đổi dữ liệu với nhau của các nút mạng
##### Phân loại mạng máy tính:

|  | Mạng cá nhân (PAN) | Mạng cục bộ (LAN) | Mạng đô thị (MAN) | Mạng diện rộng (WAN) |
| ---- | ---- | ---- | ---- | ---- |
| Phạm vi kết nối | vài chục m | vài km | hàng trăm km | vài nghìn km |
| Số lượng người dùng | 1 - 1e2 | 10 - 1e6 | 1e7+ | 1e8+ |
| Mục đích phục vụ | Cho cá nhân | Cho gia đình, tổ chức | Cho thành phố, khu vực | The internet itself |
| Công nghệ | Bluetooth, NFC | Ethernet, LAN |  | 3G, 4G, GPON |

##### Kiến trúc mạng - Mạng của các mạng
###### Mạng biên
- Các nút mạng đầu cuối (end points, systems, hosts): PC, phones, servers
- Các nút mạng truy cập (access networks): Đường truyền, thiết bị kết nối (routers, etc...)
###### Mạng lõi (Network core)
- Đường truyền, thiết bị kết nối, mạng khu vực (Regional Net), trạm chuyển tiếp nhà cung cấp (ISP), trạm trung chuyển internet (IXP)
![](https://lh7-us.googleusercontent.com/OMlgZv0jolt4TbXBfE-OPCd1uK9b-rKJ1p1mS7gx0tcUy7aW50CNcJHR6fmhK2oVKHf-AY9_Wg8MVHngIbiZ9EGH9UjQQs0Pv0k-LUl8yK9Au9JRjRj4arrxgDOQmqF2Ny_4j_76a4EhCLYo6YESaQ)

#### Lịch sử internet
##### 1969:
- Bắt đầu từ 1 thí nghiệm của ARPA, liên kết 2 nút mạng UCLA và SRI
- 12/1969: Mạng hoàn chỉnh với 4 nút, tốc độ truyền tin 56kbps
##### Thập niên 70:
- Xuất hiện các mạng riêng (đầu TN 70)
- ARPANET mở rộng (3m+ gói tin/ngày năm 74)
- 74: Cerf và Kahn nhận Turing Award nhờ nguyên lý kết nối các hệ thống mở
- 76: 