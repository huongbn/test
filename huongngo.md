**Hướng dẫn cài đặt Ubuntu 16.04**

## Mục lục

* [1.Giới thiệu về hệ điều hành Ubuntu sever](#1)
* [2.Hướng dẫn cài đặt](#2)
    * [2.1 Chuẩn bị](#2.1)
    * [2.2 Cài đặt](#2.2)
* [3.Cài đặt SSH để putty](#3)

**1.Giới thiệu hệ điều hành Ubuntu server**

**Ubuntu server 16.04** là hệ điều hành được phát hành 4 năm 2015, chủ yếu dùng cho các server, với giao diện tương tác dòng lệnh, không có hỗ trợ giao diện đồ họa.

**2.Hướng dẫn cài đặt**

**2.1.Chuẩn bị**

* VMWare Workstation 12.0
<<<<<<< HEAD
* Download 'link' cai dặt tu trang http://www.ubuntu.com/download/server


**2.2. Cai dat**
=======
* Download "link" cài dặt từ trang http://www.ubuntu.com/download/server


**2.2. Cài đặt**

Chúng ta tiến hành cấu hình máy ảo như sau


<img src="https://i.imgur.com/XHUhKs7.png">


Tiếp theo là bước thiết lập **username** và **password** để đăng nhập vào máy ảo


<img src="https://i.imgur.com/RAzlc8d.png">


Cứ tiếp tục bấm next và đến đoạn này là chọn dung lượng **RAM** để chạy cho máy ảo.
Ở đây tôi chọn **1GB** dung lượng **RAM** cho máy ảo.


<img src="https://i.imgur.com/dYTYAk9.png">


Tiếp tục bấm **Next** cho đến lúc kết thúc. Ta hiện ra một màn hình cài đặt như sau:


<img src="https://i.imgur.com/QCYeYp0.png">


Tiến trình cài đặt của ta đang chạy tự động.
Hãy chờ đợi và tiếp nhận thành quả =)))

<img src="https://i.imgur.com/ossrg1v.png">


Và đây là thành quả =)))


<img src="https://i.imgur.com/9eBlmDY.png">


**3. Cài đặt SSH để putty**

**Putty** là phần mềm giúp bạn truy cập và điều khiển hệ điều hành *Linux* của bạn qua SSH**

* B1. Chạy lệnh: 
> sudo apt-get update
* B2. Chạy lênh: 
> sudo apt-get install ssh
> sudo apt-get install putty

Sau khi đã cài xong **Putty** ta tiến hành bật ứng dụng lên.
Cửa sổ ứng dụng bật lên, trong đó **Ussername** là **tên đăng nhập của bạn** hoặc **địa chỉ IP máy ảo của bạn**
Muốn kiểm tra địa chỉ **IP** của máy ảo, ta chạy lệnh:
> sudo ifconfig

Sau khi đã điền đúng **username** ta tiến hành điền **username** và **password** là tên đăng nhập của bạn và *mật khẩu* lúc bạn thiết lập ban đầu.

<img src="https://i.imgur.com/No0Tugt.png">

Ta có kết quả như trên :))

>>>>>>> 5b101b538439adbb1f37325db906e0c318e59b17


