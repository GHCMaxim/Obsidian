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

### Mô hình TCP / IP
#### Tầng 1: Tầng vật lý
##### Tổng quan:
***Nhiệm vụ:***
- Biến đổi dòng bit dữ liệu thành tín hiệu vật lý để chuyển đi
***Phương tiện truyền:***
- Cáp đồng trục:
	- Phân loại:
		- Cáp gầy: đường kính 5mm
		- Cáp béo (chuẩn): đường kính 9.5mm
	- Băng thông:
		- Cơ sở: 10Mbps
		- Băng rộng: 400Mbps
	- Nhược điểm: Tốc độ thấp, nặng và cứng, không linh hoạt
- Cáp xoắn đôi
	- Phân loại:
		- UTP (không có vỏ bảo vệ)
		- STP (Có giấy bạc bảo vệ): Chống nhiễu, tin cậy tốt hơn
	- Tốc độ:
		- Cat4: 10Mbps
		- Cat5, 5e: 100Mbps
		- Cat6: 1Gbps
	- Kết nối: 
		- Đấu thẳng: 2 đầu cáp bấm cùng kiểu $\Rightarrow$ Kết nối 2 thiết bị khác loại
		- Đấu chéo: 2 đầu cáp bấm khác kiểu $\Rightarrow$ Kết nối 2 thiết bị cùng loại
	- Trong 8 lõi:
		- 4 lõi vô dụng
		- 2 lõi cấp nguồn tin
		- 1 lõi truyền tin
		- 1 lõi nhận tin
		$\Rightarrow$ Có thể vừa gửi vừa nhận
	- Ứng dụng: Trong mạng LAN cỡ nhỏ, đi xa max 100m
- Cáp quang:
	- Cấu tạo: lõi to bằng sợi tóc, lớp cladding đều bằng thuỷ tinh, lớp bảo vệ bằng nhựa.
	- Truyền tín hiệu: dựa trên hiện tượng phản xạ toàn phần.
	- Băng thông: hàng chục, trăm Gbps.
	- Chống nhiễu tuyệt đối, suy hao tín hiệu nhỏ, có thể truyền xa vài km.
	- Ứng dụng:
		- Xây dựng cáp trục các mạng LAN lớn.
		- Là công nghệ kết nối Internet của các nhà mạng
		- Xây dựng hệ thống cáp trục cho Internet xuyên đại dương.
***Mã đường dây (Line Coding):***
- Nguyên lý: sử dụng tín hiệu rời rạc, có điện áp khác nhau biểu diễn các bit.
- Yêu cầu: giảm thành phần 1 chiều, đồng bộ đầu thu và đầu phát tránh thành phần tần số thấp hoặc cao
1. Mã Unipolar (đơn cực): sử dụng 2 mức điện áp 0 và +V.
	- Các loại mã: Có xung vuông: 1 Không có xung: 0
	- 2 mã điển hình:
	    - NRZ – L: 0: điện áp thấp 1: điện áp cao
	    - NRZ – I: 0: không chuyển mức đầu xung 1: có chuyển mức đầu xung
2. Mã Dipolar: một chu kỳ mã được chia 2 phần.
	- Luôn có chuyển mức giữa xung → nửa chu kỳ dương, nửa chu kỳ âm → trong toàn bộ mã, thành phần 1 chiều bằng 0.
	- 2 mã điển hình:
	    + Manchester: 0: chuyển điện áp cao → thấp 1: chuyển điện áp thấp → cao
	    + Manchester vi sai: 0: có chuyển mức đầu xung 1: không chuyển mức đầu xung
3. Mã Bipolar: sử dụng 3 mức điện áp (+V, 0, -V) để mã hoá các bit nhị phân “0” và ”1”.
	- Bit “0” biểu diễn bằng mức điện áp 0, bit “1” biểu diễn luân phiên bởi +V và –V.
	- RZ (return zero): chỉ duy trì tín hiệu trong nửa tín hiệu, về 0 trong nửa còn lại.
	- Nhược điểm: phải dùng 2 xung biểu diễn 1 tín hiệu.  
4. Mã HDBn: đồng bộ giữa bên thu và phát, phát triển từ mã Bipolar RZ.
	- Quy tắc: Nếu số ký hiệu “0” liên tiếp vượt quá n thì nhóm ký hiệu “0” này sẽ được thay bằng một mã đặc biệt.
	- Mã điển hình: HDB3: (như hình dưới đây):
![Chart, box and whisker chart  Description automatically generated](https://lh7-us.googleusercontent.com/A1BRvK4_OS-SAvS024dwwmT2DN-_goqyM522V_IRubHe3lFcPNQ5LiXILpqRa4Tl_VFSolq4uaB07ECXh4NmLL0HtW8_-aRFjTZV2dAAvelfdQscM5HK-cH-mvG1EJNK9B9lqjqF2ZPHkFuyeogSNA)
	- Ví dụ: Khi có nhiều hơn 4 số 0, nhóm được thay đổi thành 000V hoặc B00V (với V vi phạm quy tắc đan dấu của mã Bipolar).

5. Mã nBmT:
- Quy tắc: thay thế n ký hiệu nhị phân bằng m ký hiệu ba mức (B – binary, T – tenary).
- Ý nghĩa: Bằng cách tăng số mức của ký hiệu, cho phép giảm độ rộng băng tần. 
***Ghép kênh và phân kênh (Division Multiplexing):***
1. Theo tần số (FDM):
	+ Sử dụng trong các hệ thống điện thoại thế hệ cũ,và thông tin vô tuyến.
	+ Chia băng tần của kênh truyền thành nhiều băng tần nhỏ cho nhiều người sử dụng
	+ Ưu điểm: Cho phép giảm ISI (nhiễu ký tự) bằng cách giảm băng tần của tín hiệu.
	+ Nhược điểm: không mềm dẻo khi ghép kênh các tín hiệu có độ rộng băng tần khác nhau vào khe tần số (do có độ rộng cố định).
$\Rightarrow$ Bộ dao động điều chế có giá thành tương đối đắt do yêu cầu sự ổn định tần số.
2. Theo thời gian (TDM):
	+ Tại cùng băng tần mỗi người sử dụng được chia một khe thời gian (time slot) trong một khung thời gian để truyền một phần thông tin của mình.
	+ Phân loại:
		- Ghép bit: mỗi khe thời gian chỉ truyền một bit.
		- Ghép byte: mỗi khe thời gian là 1 byte thông tin. Nếu tốc độ truyền là r (bit / s) thì:
			- Độ rộng bit: $(t_{s}) = 8/r$
			- Độ rộng khung thời gian: $t_{f} = t_{s} . (\textrm{số kênh})$
	+ Ưu điểm:
		- Mềm dẻo hơn FDM do có thể phân phối nhiều khe thời gian trong khung thời gian cho cùng một người sử dụng.
		- Cấu hình thiết bị đơn giản hơn FDM
	+ Nhược điểm:
		- Cần đồng bộ thời gian thu – phát giữa trạm gốc và tất cả các thiết bị di động.
		- Yêu cầu tốc độ truyền (ký hiệu) lớn hơn khá nhiều so với FDM, do vậy băng tần yêu cầu lớn hơn, độ rộng ký hiệu hẹp hơn khiến ảnh hưởng của ISI lớn hơn.  
3. Theo mã (CDM):
	- Ban đầu, được sử dụng trong quân sự (do bảo mật cao và chất lượng tốt). Hiện nay, dùng chủ yếu trong thông tin di động.
	+ Nguyên lý chung: tín hiệu cần truyền được trải phổ sao cho tín hiệu sau điều chế có phổ rộng hơn nhiều so với tín hiệu ban đầu.
	+ Do đó, nhiễu thường chỉ tác động vào một miền tần số trên toàn bộ phổ của tín hiệu.
	+ Quan trọng: tín hiệu của nhiều người sử dụng có thể gửi đi trên cùng một băng tần tại cùng một thời điểm bằng cách sử dụng các từ mã khác nhau.

	+ 2 phương pháp:
		- Trải phổ trực tiếp (Direct-Sequence Spread Spectrum – DSSS):
			- Phổ của tín hiệu đầu vào sẽ được trải rộng đều trên miền tần số, công suất trên một đơn vị tần số sẽ giảm xuống.
			- Cho phép nhiều người dùng chung băng tần.
			- Ở bên thu, tín hiệu trải phổ được coi như tín hiệu nhiễu băng rộng với công suất nhỏ và có thể loại bỏ dễ dàng.
			- Phổ biến và sử dụng rộng rãi do dễ cài đặt và tốc độ cao.
		- Trải phổ nhảy tần (Frequency Hopping Spread Spectrum – FHSS):
			- FHSS trải phổ bằng cách truyền tín hiệu trên một kênh truyền băng hẹp trong một khoảng thời gian ngắn, sau đó nhảy sang một kênh khác.
			- Diễn ra liên tục với các tần số nhảy đã định nghĩa sẵn, chỉ bên thu và phát biết trước.
			- Do sử dụng băng hẹp ngẫu nhiên, FHSS có tỷ số SNR khá lớn. Đối với những đầu thu khác, tín hiệu FHSS được coi như các nhiễu xung băng hẹp trong một chu kỳ ngắn.
#### Tầng liên kết dữ liệu
##### Tổng quan: Các chức năng chính
1. Đóng gói:
	- Đơn vị dữ liệu: Khung tin (frame)
	- Bên gửi: Thêm header, trailer cho gói tin nhận được từ tầng mạng
	- Bên nhận: Bỏ header và trailer, đẩy lên tầng mạng
2. Định địa chỉ:
	- Sử dụng địa chỉ MAC 48bits, quản lý bởi IEEE
		- Mỗi cổng mạng gán 1 MAC, không thể thay đổi $\rightarrow$ địa chỉ vật lý của cổng mạng.
		- Không phân cấp, có tính di động
		+ Không cần thay đổi địa chỉ MAC khi host chuyển sang mạng khác.
		+ **Địa chỉ quảng bá trong mạng LAN:** FF-FF-FF-FF-FF-FF (nếu muốn truyền đến mọi nút, chỉ cần đến MAC quảng bá).
3. Điều khiển truy nhập đường truyền: Đơn và đa truy nhập
4. Kiểm soát luồng: Đảm bảo bên nhận không bị quá tải
5. Kiểm soát lỗi: Phát hiện và sửa lỗi bit trong khung tin.
		a. Parity (1bit): Thêm vào 1 bit vào gói tin check:
			- Parity lẻ: số bit 1 nhận giá trị lẻ
			- Parity chẵn: số bit 1 nhận giá trị chẵn
		b. Checksum:
			- Nguyên lý tạo ra mã checksum n bit:
				- Phía gửi:
					- Chia dữ liệu thành các phần có kích thước n bits
					- Tính tổng các phần. Nếu kết quả tràn quá n bit, cộng các bit tràn vào kết quả
					- Đảo bit kết quả cuối cùng nhận Checksum
					- Truyền checksum kèm dữ liệu
				- Phía nhận:
					- Tách dữ liệu và checksum
					- Chia dữ liệu thành các phần có size n bits.
					- Tính tổng các phần và checksum.
					- Nếu kết quả tràn, cộng tràn vào kết quả
					- Nếu kết quả cuối xuất hiện 0 $\rightarrow$ lỗi
		c.  Vòng CRC:
			- Phía gửi:
				- Chọn 1 đa thức sinh bậc k: (thường là 𝑥4 + 𝑥 + 1)
				- Biểu diễn đa thức dưới dạng chuỗi bit P (các hệ số của đa thức là giá trị bit của P).
				- Thêm k bit 0 vào frame dữ liệu F được Fk.
				- Chia Fk cho P, lấy phần dư R.
				- Ghép phần dư vào chuỗi dữ liệu được FR.
			- Phía nhận:
				- lấy FR chia cho P.
				- Nếu chia hết → truyền đúng.
				- Nếu có dư, căn cứ vào số dư (syndrome) để phát hiện và sửa lỗi (nếu được).
6. Chế độ truyền:
	- Simplex (đơn công): 1 chức năng (chỉ gửi hoặc nhận)
	+ Half – duplex (bán song công): có cả 2 chức năng nhưng chỉ được dùng 1 trong 1 thời điểm (bộ đàm)
	+ Full – duplex (song công): có thể sử dụng cùng lúc cả 2 chức năng.
7. Triển khai trên hệ thống mạng
	+ Điều khiển truyền dữ liệu trên liên kết vật lý giữa 2 nút mạng kế tiếp.
	+ Triển khai trên mọi nút mạng
	+ Triển khai và cung cấp dịch vụ phụ thuộc vào đường truyền (WiFi, Wimax, 3G, cáp quang, cáp đồng...)
	+ Truyền thông tin cậy (cơ chế giống TCP nhưng đơn giản hơn) hoặc không.
8. Triển khai trên các nút mạng:
	+ Được đặt trên card mạng (NIC - Network Interface Card) hoặc trên chip tích hợp cùng với tầng vật lý
	+ NIC được kết nối với hệ thống bus
##### Điều khiển truy nhập đường truyền
***Các dạng liên kết***:
- Điểm - điểm: ADSL, Telephone Modem,...
- Điểm - Đa điểm:
	- LAN có dạng bus, LAN hình sao dùng hub
	- Mạng không dây
***Phân loại các giao thức đa truy nhập:***
1. Kỹ thuật chia kênh:
	- Chia tài nguyên của đường truyền thành nhiều phần nhỏ cho các nút mạng: (theo thời gian - TDMA, theo tần số - FDMA, theo mã - CDMA).
2. Truy nhập ngẫu nhiên:
	- Không chia kênh, cho phép đồng thời truy nhập, chấp nhận có xung đột
	- Cần cơ chế phát hiện và tránh xung đột
	- e.g. Pure Aloha, Slotted Aloha, CSMA / CD, CSMA / CA,...
3. Lần lượt:
	- Theo hình thức quay vòng (Ví dụ: Token Ring, Token Bus…)
***Kỹ thuật chia kênh:***
1. FDMA (frequency division multiple access):
![Graphical user interface  Description automatically generated](https://lh7-us.googleusercontent.com/zm1kz7O838KNRKfMANCDxEzgoZvETnqsi_YKN_AySCEO4AQUu0_1kSxqiT5KgpxAoersslZ7oTGW5u1g_Ey_ncDbecdXP3-LvvtA66fVmzfsUBd2V_4EWVXWsAZAnMK-Q4cPBh7CzueckTZJ2OHm0A)

2. TDMA (time division multiple access): 
![](https://lh7-us.googleusercontent.com/KmdR-A8XkcXbHYSC0CCSygyd-wD4yYEQxxPRYhkDzMkNSq_iGdX_YmzdRdzQZjPJSrfbZKegia8vkwktRE8rM3LJib9ah33Fnz3Mr-4qF7n8hxGNtZlxhPXqEl2mZJHKlGg9B5SaROwwGMBZri5fHQ)

3. CDMA (code division multiple access):
Mọi máy sử dụng 1 dải tần số. Các kênh thuê bao được tách biệt bằng cách sử dụng mã ngẫu nhiên. Các tín hiệu của nhiều thuê bao khác nhau sẽ được mã hoá bằng các mã  ngẫu nhiên khác nhau, sau đó trộn lẫn và phát đi trên dải tần chung và chỉ được phục hồi ở thiết bị đầu cuối với mã ngẫu nhiên tương ứng.

***Truy cập ngẫu nhiên:***
1. Aloha (Pure Aloha):
    + Frame - time: thời gian để truyền hết một frame có kích thước lớn nhất  
	-  Khi một nút mạng cần truyền dữ liệu:
		- Frame đầu tiên: truyền ngay. Nếu có đụng độ thì truyền lại với xác suất p.
		- Các frame sau: truyền với xác suất là p. (chưa chắc đã được truyền)
		- Trong 1 frame - time chỉ được truyền 1 frame.
		- Xác suất truyền thành công là khoảng 18.4%.
2. Slotted Aloha: Hoạt động như Aloha với các yêu cầu:
+ Frame-time là như nhau với mọi nút
+ Tất cả các nút phải đồng bộ về thời gian
+ Xác suất truyền thành công: 36.8%
$\Rightarrow$ Khó triển khai trên thực tế (phải đồng bộ thời gian).
3. Cảm nhận sóng mang (Carrier Sense Multiple Access):
	+ CSMA / CA (collision avoidance): 
		+ Cảm nhận sóng mang trên đường truyền, nếu không có thì truyền dữ liệu.
		+ Xảy ra đụng độ do trễ trên đường truyền.
	+ CSMA / CD (collision detection):
		- Một thiết bị có frame cần truyền sẽ lắng nghe cho đến khi nào đường truyền không còn bị chiếm sẽ bắt đầu gửi frame.
		- Máy gửi cũng bắt đầu lắng nghe để đảm bảo rằng không có xung đột xảy ra.
		- Nếu có xung đột, tất cả các máy trạm đã từng gửi ra frame sẽ gửi tín hiệu nghẽn để đảm bảo tất cả các máy trạm đều nhận ra xung đột.
		- Sau khi tín hiệu nghẽn là hoàn tất, mỗi máy gửi của những frame bị xung đột sẽ khởi động một bộ định thời (ngẫu nhiên) và chờ hết khoảng thời gian này sẽ cố gắng truyền lại. Những máy không tạo ra xung đột sẽ không phải chờ.
		- Sau khi các thời gian định thời là hết, máy gửi có thể bắt đầu một lần nữa với bước 1.