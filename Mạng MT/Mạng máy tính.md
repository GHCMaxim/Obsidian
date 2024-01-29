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
- 76: Ethernet đc phát triêwnr ở Xerox PARC
##### Thập niên 80:
- 80: TCP/IP Protocol được chuẩn hoá và phổ biến, được tích hợp vào UNIX bởi Berkeley
- Thêm nhiều mạng mới: MFENET, HEPNET, SPAN, BITnet, CSnet, NSFnet, Minitel,... được nối với nhau
- Thêm nhiều dịch vụ: FTP, Mail, DNS,...
##### Thập niên 90:
- Đầu 90: Web phát triển với HTML và HTTP protocol
- 94: Xuất hiện trình duyệt Mosaic, Netscape
- Cuối 90 - 2000:
	- Nhiều ứng dụng mới: Chat, P2P sharing
	- E-Commerce: Yahoo, Amazon, Google
	- 50m+ máy trạm, 100m+ users
	- Internet for everyone $\Rightarrow$ CyberSec issue
- 97: Việt Nam có Internet
### Chuyển mạch kênh và chuyển mạch gói
#### Đặt vấn đề:
##### Thông số kết nối giữa 2 máy
- Băng thông (bandwidth): Lượng dữ liệu truyền tối đa trong 1 đvị thời gian (bps - bits per s)
- Trễ (Latency): Thời gian truyền dữ liệu từ A đến B.
	- Trễ truyền tải = Kích thước dữ liệu / Băng thông
	- Trễ truyền dẫn = Độ dài liên kết / Tốc độ dữ liệu ($\approx 2.10^{8}m/s$ )
##### Kết nối giữa nhiều nút mạng
- Sử dụng mạng chuyển mạch:
	- Mỗi host kết nối với 1 thiết bị chuyển mạch
	- Các thiết bị chuyển mạch kết nối điểm - điểm và chuyển tiếp dữ liệu tới đích = định tuyến
	- Chia sẻ tài nguyên đường truyền
#### Chuyển mạch kênh

![](https://lh7-us.googleusercontent.com/gjv2m-ESWcA2O5EfIDg-UjeK-W568K06zFG4kOoQUcgIbCdwEp4vx09ItPX0_3sYh4cLDyhAufkhFY5BH9XMBdOMObgnmLH1AoX4iTO_AjqMliiBiQ_dktZZDf7wbcJRcTEt_0aT1rQAbnqh-b4Wig)

(1): A phát yêu cầu thiết lập kênh
(2): Các thiết bị chuyển mạch thiết lập kênh
(3): A bắt đầu truyền dữ liệu
(4): A truyền xong: Phát yêu cầu huỷ kênh

##### Trên mỗi thiết bị chuyển mạch:
-  Ghép kênh: Gửi dữ liệu của nhiều kênh trên nhiều liên kết vật lý.
-  Các kỹ thuật:
	- Theo thời gian (TDM): Sử dụng tài nguyên trong khe thời gian được phân
	- Theo tần số (FDM): Sử dụng một băng tần tín hiệu riêng
-  Phân kênh: Phân dữ liệu nhận được trên liên kết vật lý vào các kênh tương ứng và chuyển đến đúng đích
##### Ưu điểm: 
- Kênh thiết lập sẵn $\rightarrow$ Trễ chuyển mạch rất thấp
- Tài nguyên dành riêng và không đổi khi truyền $\rightarrow$ Đảm bảo chất lượng dịch vụ
##### Nhược điểm:
- Dễ mất thông tin khi truyền
- Tốn thời gian khi dữ liệu nhỏ
- Bắt đầu lại quá trình nếu lỗi trên thiết bị chuyển mạch
- Hiệu suất sử dụng đường truyền thấp
#### Chuyển mạch gói
##### Luật chuyển
- Dữ liệu được chia thành các gói tin (package) bao gồm: Tiêu đề (header), địa chỉ, số thứ tự và dữ liệu (Payload)
- Thiết bị chuyển mạch chuyển tiếp gói tin dựa trên tiêu đề
- Chỉ chuyển tiếp khi nhận được toàn bộ gói tin.
+ Công đoạn xử lý: kiểm tra lỗi, gửi gói tin (thường nhỏ so với trễ truyền tin).
+ Mỗi gói tin có thể được xử lý độc lập, đường đi khác nhau, không còn đúng thứ tự.
+ Tài nguyên dùng chung cho tất cả các kết nối.
##### Cách thức chuyển
- Unicast: Chuyển tới 1 nút mạng
- Multicast: Chuyển tới một nhóm nút mạng
- Broadcast: Chuyển tới tất cả nút mạng
##### So sánh với chuyển mạch kênh:
- Hiệu suất sử dụng đường truyền cao
- Không tốn thơi gian thiết lập kênh
##### Trên mỗi thiết bị chuyển mạch
- CÓ 1 hàng đợi FIFO để sắp xếp các gói tin
- Mất gói tin nếu hàng đợi đã đầy
##### Các thông số cơ bản:
- Băng thông = Tốc độ truyền tin / Dung lượng
- Thông lượng