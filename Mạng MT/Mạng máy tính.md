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
- Thông lượng:
	- Là tốc độ truyền tin qua một điểm nào đó trong mạng (bits/s)
	- Thông lượng tức thời: Tại 1 thời điểm
	- Thông lượng trung bình: Trong 1 khoảng thời gian
	- Nút thắt (bottleneck): Là điểm làm giới hạn thông lượng trên đường truyền
- Độ trễ: $$ d_{all} = d_{proc} + d_{queue}+ d_{tran} + d_{prop}$$
	- $d_{tran}$ : Kích thước gói tin/ băng thông
	- $d_{prop}$ : Độ dài đường truyền/tốc độ lan truyền ($\approx 2.10^{8} m/s$ )
	- $d_{proc}$ (Trễ xử lý): Kiểm tra lỗi bit và xác định liên kết ra (Cỡ $\mu s$ )
	- $d_{queue}$ (Trễ hàng đợi): Phụ thuộc vào hàng đợi, dựa trên tỉ lệ $L. \frac{a}{R}$ 
		- $L.\frac{a}{R} \approx 0 \rightarrow$ Trễ hàng đợi nhỏ 
		- $L. \frac{a}{R} >1 \rightarrow$ Mất gói tin
- Trễ khứ hồi (Round Trip Time = $t_{3}-t_{0}$)
![](https://lh7-us.googleusercontent.com/rhfgZJDmGkgcBXTdKXYbVfnXtnd64TXmLvzqFUlDo4b_0RqoDU6MKeb5MQ8K1PHPmNZlzVOB7sosbDXbr9Mz8P0yidVhP9ldq_VhnKZIILCLhvf_S7G16p5Q3lG_gxowA0jVnO6If5sltJvE8H39sA)
- MTU (Maximum Tranmission Unit): Kích thước tối đa của gói tin có thể truyền
	- Mục đích 1: Giảm tỉ lệ gói tin bị lỗi bit (Do BER là hằng số $\rightarrow$ Gói tin càng nhỏ càng ít lỗi)
	- Mục đích 2: Giảm xác suất phải truyền lại do mất gói tin:
		- Kích thước hàng đợi cố định $\rightarrow$ Nếu mất gói tin thì truyền lại cũng đơn giản hơn $\rightarrow$ MTU làm giảm kích thước dữ liệu phải truyền lại
		- Ngược lại, MTU không thể quá nhỏ vì sẽ giảm hiệu suất truyền. Do gói tin gồm header(hằng số) và payload (phần hữu ích) 
			$\rightarrow$ **Hiệu suất = Payload / (Header + Payload)** 
			$\Rightarrow$ Nếu MTU quá nhỏ thì hiệu suất sẽ thấp
### Kiến trúc phân tầng
#### Nguyên tắc
##### Chia để trị
- Xác định, tổ chức, điều phối và phân công thực hiện các nvu
##### Phân tầng
- Mỗi tầng:
	- Có thể thực hiện 1 hoặc nhiều chức năng.
	- Các chức năng có thể thực hiện: 
		- Cung cấp dịch vụ cho tầng trên
		- Sử dụng dịch vụ tầng dưới
		- Độc lập với các tầng còn lại
	- Mỗi dịch vụ có thể có 1 hoặc nhiều cách triển khai khác nhau, cho phép tầng trreen lựa chọn dịch vụ phù hợp
	- Lợi ích: Dễ thiết kế, triển khai, tái sử dụng và nâng cấp
##### Điểm truy cập dịch vụ (Service Access Point)
- Là điểm trừu tượng, tại đó tầng trên chỉ quan tâm cách sử dụng dvu tầng dưới, không quan tâm cách thực hiện
- Quan điểm lập trình: Cung cấp API (Application Programming Interface), trong đó, tên hàm và các thức truyền đổi số không đổi, nội dung hàm có theer thay đổi
#### Truyền thông trong kiến trúc phân tầng:
##### Nguyên lý chung
- Tầng trên sử dụng dịch vụ tầng dưới
+ Các tầng ngang hàng sử dụng chung cách thức và phương tiện trao đổi dữ liệu.
##### Cách thức xử lý dữ liệu tại mỗi tầng
 - Chia thành các đơn vị dữ liệu giao thức - PDU (Protocol Data Unit) gồm:
	- Header: chứa địa chỉ, thông tin để hệ thống mạng xử lý
	- Payload: dữ liệu cần truyền tải
+ Chức năng mỗi tầng khác nhau, cách thức xử lý dữ liệu khác nhau
$\Rightarrow$ Cần phối hợp chức năng giữa các tầng trong quá trình truyền tải
##### Gửi và nhận:
 - Bên gửi: thêm header phục vụ xử lý dữ liệu và chuyển cho tầng dưới (Encapsulation).
 - Bên nhận: xử lý, tách header và chuyển dữ liệu cho tầng trên (Decapsulation).
 - Do phía nhận phải hiểu nội dung PDU của phía gửi → PDU tại các tầng đồng cấp của hai bên giống nhau 
 $\Rightarrow$ Cần có giao thức chung (Network protocol): Là tập hợp các quy tắc quy định khuôn dạng, ngữ nghĩa, thứ tự các thông điệp được gửi và nhận giữa các nút mạng và các hành vi khi trao đổi các thông điệp đó.
 VD: Mô hình giao thức chung mỗi tầng:
 ![](https://lh7-us.googleusercontent.com/W6qqPczSra4P9v8YkJIycx0R1xkf-X3zATAwKfd9xpfPOZJrem9UsoQ8fKhMYWQf4dyfrC06HWHoL6AZ9FoOj0Ih32o_3qTM-Dlk4Hv4RqEeNuJbbZUSDz4_zYntlQ1eiRtj0mr49D2_HHi3WirbqQ)

##### Chồng giao thức:
+ Do mỗi tầng có nhiều cách thực hiện các chức năng 
$\Rightarrow$ Sinh ra các giao thức khác nhau, bao gồm: 
	- Gọi dịch vụ của tầng dưới
	- Cung cấp dịch vụ cho tầng trên.
$\Rightarrow$ Cần có giao thức chung cho mỗi tầng
$\Rightarrow$ Khái niệm chồng giao thức: Là ngăn xếp các giao thức truyền thông trên kiến trúc phân tầng, trong đó:
	- Các tầng đồng cấp ở mỗi bên sử dụng chung giao thức để điều khiển quá trình truyền thông logic giữa chúng
	- 2 cách điều khiển truyền thông logic giữa các tầng đồng cấp:
		- Cách 1: Hướng liên kết (connection oriented): tin cậy Dữ liệu được truyền qua một liên kết đã được thiết lập. Ba giai đoạn: Thiết lập liên kết, Truyền dữ liệu, Hủy liên kết. 
		- Cách 2: Hướng không liên kết (connectionless): không tin cậy Không thiết lập liên kết, chỉ truyền dữ liệu. “Best effort”: truyền ngay với khả năng tối đa.
+ Protocol Stack: Last in first out → gọi là chồng giao thức (Stack).
#### Mô hình hệ thống mạng thực tế
+ Là mô hình phân tầng chức năng TCP/IP.
+ Giúp cho các nút có phần cứng khác nhau trong hệ thống có chung mô hình phần mềm để trao đổi dữ liệu.
+ Sử dụng để xây dựng hệ thống mạng, truyền thông về mặt chức năng (phần mềm).
+ Các phần mềm xây dựng trên phần cứng của mạng đều có mô hình TCP / IP.
+ Triển khai kiến trúc phân tầng:
	- Toàn bộ 5 tầng trên các thiết bị đầu cuối.
	- Chỉ có 3 tầng dưới cùng trên các thiết bị chuyển tiếp.
