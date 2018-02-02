**Gioi thiệu ve VmWare Workstation**

#Mục lục

* [1. Giới thiệu về VmWare Workstation](#1)
* [2. Thêm sửa xóa một Vmnet trong VmWare](#2)
* [3. Sửa dải IP của một Vmnet](#3)
* [4. Ba chế độ trong VmWare Workstation](#4)
  * [4.1 Bridge](4.1)
  * [4.2 Host-only](#4.2)
  * [4.3 NAT](#4.3)


<a name="1"></a>
**1. Giới thiệu về VmWare Workstation**


* VMware là phần mềm tạo máy ảo với hiệu năng hoạt động mạnh mẽ cho phép chạy song song nhiều hệ điều hành cùng lúc, rất hữu ích khi bạn chơi game hoặc thử nghiệm các phần mềm.

* VMware là cách đơn giản nhất để bạn tạo máy ảo và chạy song song nhiều hệ điều hành trên cùng một máy tính, rất hữu ích khi người dùng muốn thử nghiệm một hệ điều hành mới, kiểm tra tính tương thích với hệ thống. VMware hỗ trợ những phần cứng mới nhất, cải thiện khả năng kết nối, hiển thị màn hình với độ phân giải cao và có thể chia sẻ dữ liệu trong môi trường an toàn.

* VMware Workstation thực hiện sao chép môi trường máy chủ, desktop, máy tính bảng trong máy ảo, có khả năng chạy các ứng dụng yêu cầu cao trong môi trường ảo, có thể truy cập máy ảo dễ dàng qua môi trường đám mây.

* Cac ban co the Download **link** cai dặt tai trang sau: https://my.vmware.com/web/vmware/info/slug/desktop_end_user_computing/vmware_workstation_pro/12_0

* O đây mình cài đặt bản VmWare Workstaion 12. Ta có giao diện sau khi cài đặt như sau:
<img src="https://i.imgur.com/S7sJPIc.png">

<a name="2"></a>
**2. Thêm, sửa, xóa một Vmnet**

* Mặc định khai cài VmWare sẽ cho ta 2 card mạng:
 * Một card là **bridge**. Card này chính là card mạng thật của máy. Khi sử dụng card này thì máy ảo sẽ kết nối Internet bình thường mà không gặp vấn đề già cả.
 * Card thứ 2 ở chế độ NAT. Oử chế độ này, máy ảo vẫn kết nối ra được Internet nhưng địa chỉ IP của máy ảo sẽ NAT thành địa chỉ *public* để kết nối đi ra ngoài Internet.
 
    `Thêm một Vmnet`
    
Oử màn hình chính của VmWare, ta chọn **Edit** và chọn **Virtual Network Editor**. Một cửa sổ được mở ra và ở đây ta sẽ có các thao tác thêm sửa xóa với một card Vmnet mfa ta mong muốn.
Ta chọn **Change Setting** để có thể thao tác với card Vmnet mà ta mong muốn như sau:


<img src="https://i.imgur.com/zMVJQZf.png">

Tiếp theo ta chọn **Add Network** để thêm card card mà ta mong muốn. Oử đây các bạn có thể thấy tôi thêm 3 card lần lượt là Vmnet1, Vmnet2 và VMnet3 như trong hình vẽ

  `Xóa một Vmnet`
  
Khi một card Vmnet không còn dùng nữa, ta có thể chọn card đó và chọn **Remove Network**. Các thao tác rất đơn giản, các bạn thử một lần là quen ngay.


<a name="3"></a>
**3. Sửa IP của một Vmnet**

Như ở trên, ta có thể thấy rằng khi tạo thêm các card Vmnet thì VmWare sẽ tự sinh ra một địa chỉ mạng cho card đó. những địa chỉ này rất khó nhớ và nhiều khi gặp một bài lab nào đó, ta rất khó có thể nhớ đúng các địa chỉ này

Để tuận tiện cho việc thực hiện các bài lab sau này, ta sẽ chỉnh sửa các địa chỉ này sao cho dễ nhớ nhất:

ở đây ta có 3 card có địa chỉ lần lượt là 192.168.80.0; 192.168.166.0 và 192.168.188.0


 <img src="https://i.imgur.com/zMVJQZf.png">
 

Sau khi chỉnh sửa ta sẽ có thể dễ dàng nhớ địa chỉ mà ta thiết lập cho các Vmnet. Oử đây tôi chỉnh sửa cho card Vmnet 2 với địa chỉ mạng là 10.10.10.0 và subnet là: 255.255.255.0

<img src="https://i.imgur.com/zBRfNrS.png">

Tương tự với Vmnet2 và VMnet3 ta có thể dễ dàng chỉnh sửa theo bất cuwsd dịa chỉ nào mà ta mong muốn.


<a name="4"></a>
**4. Ba chế độ mạng trong VmWare**


<a name="4.1"></a>
  * **4.1 Bridge**
 
 Bridge sẽ được tự động chọn khi bạn chọn **Use Bridge Networking** trong **New Virtual Machine Wizard** 
 Khi chọn chế độ này, thì virtual machine tham gia vào Internet bình thường
 
 
 <img src="https://i.imgur.com/HuZcAQ7.png">
 
 Chế độ này nôm na hiểu như là: máy ảo sẽ đi ra Internet bằng 1 đường dây nối từ chính nó tới card vật lý. Khi ta cắm dây mạng vào card vật lý thì máy ảo sẽ truy cập được Internet.
 
 
 
 <a name="4.2"></a>
  * **4.2 Host-only**
  
Oử chế độ này thì **virtual machine** không kết nối ra Internet được. Chúng ta chỉ có thể thực hiện test trong các bài lab cụ thể nào đó.Muốn kết nối đi Internet, có một cách đó là chia sẻ kết nối từ card thật của máy. Vnấ đề này các bạn có thể tìm hiểu thêm các tài liệu trên google.
  
  <img src="https://i.imgur.com/hZ6uJcw.png">
  
  
  Chế độ này cung cấp kết nối giữa các máy ảo với nhau hoặc giữa máy ảo và máy thật qua **virtual Ethernet Adapter**
  Khi ta chọn chế độ *hót-only* thì mặc nhiên trên máy vật lý của chúng ta sẽ có một card **virtual Ethernet Adapter**
  Để có thể xem **virtual Ethernet Adapter** ta vào `Control Pannel` và tìm mục `Network Connection`.
  
  <img src="https://i.imgur.com/M3RS8g9.png">
  
  Qua ảnh này ta có thể thấy tất cả các card mạng mà đang có trên máy của chúng ta. có thể thấy trên hình Vmnet2, Vmnet3, Vmnet4 lần lượt là 3 card *virtual* mà chúng ta tạo ra.
  
  
  <a name="4.3"></a>
  * **4.3 NAT**
  
  
 <img src="https://i.imgur.com/VFYl0Fl.png">
 
  NAT viết tắt của Network Address Translation. Oử chế độ này thì địa chỉ IP của nó không phải là địa chỉ public thông thường mà là các địa chỉ private. Thiết bị VmWare NAT sẽ chuyển đổi địa chỉ private của máy ảo thành địa chỉ public để máy ảo có thể đi ra ngoài Internet.
  
 NAT device sẽ thực hiện chuyển đổi từ IP private thành IP public của một hoặc nhiều máy ảo để có thể đi ra ngoài Internet.
 NAT device sẽ nhận từng gói tin tương ứng của từng máy ảo và thực hiện chuyển tới địa chỉ đích một cách chính xác nhất.
 
 
 **The end**
 Bài tìm hiểu của mình hết tại đây :))
  
  
  
  
  
  
  
 
 

