# Các câu lệnh linux kèm mô tả
## Cấu trúc thư mục
```text
/
├── /bin     #User binari
├── /sbin    #System binari
├── /etc     #Configuration files
├── /dev     #Device files
├── /var     #Variable Files
├── /home    #Home Directory
├── /proc    #Process information: Chứa các tệp có thông tin liên quan đến process đang chạy và tài nguyên phần cứng
├── /mnt     #Mount Directory
├── /media   #Removable Devices
├── /srv     #Service Data
├── /sys     #System Libraries: Lưu trữ thông tin thiết bị và dữ liệu Kernel liên quan đến phần cứng
├── /usr     #User Programs
├── /lib     #System Libraries
├── /tmp     #Temporary File
├── /boot    #Boot loader file
├── /opt     #Optional add-on Apps
```
**man** lệnh dùng để xem hướng dẫn chi tiết của các lệnh bao gồm syntax, option, chức năng,

# Các lệnh Linux cơ bản

## 1. Lệnh liên quan đến hệ thống
- `exit`: Thoát khỏi cửa sổ dòng lệnh.  
- `logout`: Tương tự `exit`.  
- `reboot`: Khởi động lại hệ thống.  
- `halt`: Tắt máy.  
- `startx`: Khởi động chế độ xwindows từ cửa sổ terminal.  
- `mount`: Gắn hệ thống tập tin từ thiết bị lưu trữ vào cây thư mục chính.  
- `unmount`: Ngược với lệnh `mount`.  

## 2. Các lệnh kiểm tra thông tin hệ thống
- `cat /proc/cpuinfo`: Kiểm tra thông tin CPU (số core).  
- `cat /proc/meminfo`: Kiểm tra thông tin RAM đang sử dụng.  
- `cat /proc/version`: Kiểm tra phiên bản Kernel.  
- `cat /proc/ioports`: Xem thông tin port I/O.  
- `cat /etc/os`: Kiểm tra phiên bản.  
- `uname -a`: Kiểm tra thông tin Kernel.
- `lsblk`: liệt kê toàn bộ thông tin về thiết bị lưu trữ
- `lscpu`: Hiển thị thông tin chi tiết về cpu
- `lspci`: Xem thông tin mainboard.  
- `free -m`: Kiểm tra dung lượng RAM còn trống.  
- `init 0`: Tắt máy (tương đương `shutdown -h now`).  
- `df -h`: Hiển thị dung lượng ổ đĩa và phân vùng.  
- `du -sh`: Kiểm tra dung lượng thư mục hiện tại.  
- `du -ah`: Hiển thị dung lượng từng file/thư mục con.  
- `du -h --max-depth=1`: Hiển thị dung lượng các thư mục con cấp 1.  
- `/sbin/ifconfig`: Xem địa chỉ IP.  
- `hostname`: Xem tên máy.    
- `arch`: Kiểm tra kiến trúc CPU.  
- `cat /proc/swaps`: Kiểm tra thông tin SWAP.  
- `last reboot`: Xem lịch sử reboot máy.  
---

## 2. Lệnh thao tác trên tập tin
- `ls`: Liệt kê tất cả các file và thư mục trong thư mục hiện hành.  
- `pwd`: Hiển thị đường dẫn thư mục hiện tại.  
- `cd`: Thay đổi thư mục làm việc.  
- `mkdir`: Tạo thư mục mới.  
- `rmdir`: Xoá thư mục rỗng.  
- `cp`: Sao chép tập tin hoặc thư mục.  
- `mv`: Di chuyển hoặc đổi tên tập tin/thư mục.  
- `rm`: Xóa tập tin.  
- `wc`: Đếm dòng, ký tự trong tập tin.  
- `touch`: Tạo tập tin mới.  
- `cat`: Xem nội dung tập tin.  
- `vi`: Mở trình soạn thảo `vi`.  
- `df`: Kiểm tra dung lượng đĩa.  
- `du`: Kiểm tra dung lượng sử dụng của tập tin/thư mục.  
- `nano`: Trình soạn thảo văn bản `nano`.  
- `less`: Xem nội dung tập tin theo dòng.  
- `tail`: Xem 10 dòng cuối của file (`tail -100 filename` xem 100 dòng cuối).  
- `more`: Xem nội dung file theo trang.  
- `head`: Xem 10 dòng đầu của file (`head -100 filename` xem 100 dòng đầu).  

---

## 3. Lệnh khi làm việc trên terminal
- `clear`: Xoá trắng màn hình terminal.  
- `date`: Xem ngày, giờ hệ thống.  
- `cal`: Xem lịch hệ thống.  

---

## 4. Lệnh quản lý hệ thống
- `rpm`: Cài đặt, kiểm tra, hoặc gỡ bỏ gói `.rpm`.  
- `ps`: Kiểm tra tiến trình đang chạy.  
- `kill`: Dừng tiến trình (cần quyền super-user để dừng tất cả tiến trình).  
- `top`: Hiển thị tiến trình và tài nguyên sử dụng.  
- `pstree`: Hiển thị cây tiến trình.  
- `sleep`: Tạm dừng hệ thống trong một khoảng thời gian.  
- `useradd`: Tạo user mới.  
- `groupadd`: Tạo nhóm người dùng mới.  
- `passwd`: Đổi mật khẩu.  
- `userdel`: Xoá user.  
- `groupdel`: Xoá nhóm.  
- `gpasswd`: Đổi mật khẩu nhóm.  
- `su`: Đăng nhập với user khác.  
- `groups`: Hiển thị nhóm của user hiện tại.  
- `who`: Hiển thị ai đang đăng nhập.  
- `w`: Giống `who`, chi tiết hơn.  
- `man`: Xem hướng dẫn chi tiết của lệnh.  

> **Lưu ý:** Dùng `man <tên_lệnh>` để xem hướng dẫn chi tiết về cú pháp, tham số, ví dụ...

---
---

## . Các lệnh shutdown, restart…
- `logout`: Kết thúc session hiện tại.  
- `reboot`: Khởi động lại máy.  
- `shutdown -r now`: Khởi động lại máy.  
- `shutdown -h now`: Tắt máy ngay.  
- `shutdown -h 9:30`: Hẹn giờ tắt máy (24h).  
- `shutdown -c`: Hủy bỏ các lệnh tắt máy đã lên lịch.  
- `telinit 0`: Tắt máy.  
- `init 0`: Tắt máy.  
- `exit`: Thoát terminal.  
- `halt`: Tắt máy.  
- `sleep`: Cho hệ thống ngủ tạm thời.  

---

## . Lệnh quản lý user
- `passwd`: Đổi mật khẩu user (root có thể đổi của tất cả user).  
- `pwck`: Kiểm tra cú pháp file `/etc/passwd`.  
- `useradd`: Tạo user mới, ví dụ `useradd -c "test user 1" -g group1`.  
- `userdel`: Xóa user.  
- `usermod`: Thay đổi thông tin user.  
- `groupadd`: Tạo nhóm mới.  
- `groupdel`: Xóa nhóm.  
- `groupmod`: Thay đổi thông tin nhóm.  
- `who`, `w`: Hiển thị user đang đăng nhập.  
- `uname`: Hiển thị tên hệ thống.  
- `id`: Hiển thị ID của user.  
- `logname`: Hiển thị tên user hiện đang đăng nhập.  
- `su`: Đăng nhập với tên user khác.  
- `groups`: Hiển thị nhóm của user hiện tại.  
- `vi /etc/passwd`: Xem danh sách user.  
- `vi /etc/group`: Xem danh sách nhóm.  
- `chmod [file]`: Thay đổi quyền truy cập file/thư mục.  
- `chown user [file]`: Thay đổi chủ sở hữu file/thư mục.  
- `chgrp group [file]`: Thay đổi nhóm sở hữu file/thư mục.  

---

## 8. Lệnh quản lý services và process
- `top`: Hiển thị tiến trình đang chạy.  
- `ps -u username`: Kiểm tra process theo user.  
- `ps -U root`: Kiểm tra process root.  
- `ps -A`: Hiển thị tất cả process.  
- `ss`: Kiểm tra socket đang kết nối.
- `netstat`: Hiển thị các socket đang mở.
- `ss -l`: Hiển thị các cổng đang mở.  
- `w username`: Xem process của user cụ thể.  
- `vmstat 3`: Giám sát tài nguyên hệ thống.  
- `ps`: Liệt kê chương trình đang chạy.  
- `uptime`: Hiển thị thời gian hoạt động của hệ thống.  
- `apt/yum/rehl/dnf`: Quản lý gói ``.   
- `wget`: Tải ứng dụng từ web.  
- `sh`: Chạy file `.sh`.  
- `service mysql stop/start/restart`: Dừng/khởi động service.  
- `kill`: Dừng process.  
- `kill PID` hoặc `kill %job`: Ngừng process theo PID hoặc job ID.  
- `pstree`: Hiển thị process dạng cây.  
- `service --status-all`: Kiểm tra tất cả service và trạng thái.  
- `whereis mysql`: Tìm vị trí cài đặt.  
- `service --status-all | grep abc`: Kiểm tra service cụ thể.  
- `kill -9 PID`: Buộc dừng process.  
- `kill -1 PID`: Dừng và reload process.  

---

## 9. Một số lệnh hữu ích khác
- `clear`: Xoá trắng terminal.  
- `hwclock`: Cập nhật đồng hồ BIOS.  
- `cal`: Xem lịch hệ thống.  
- `date`: Xem ngày giờ hệ thống.  
- `date -s "1 JAN 2018 15:29:00"`: Đặt ngày giờ hệ thống.  
- `date +%Y%m%d -s "20180101"`: Đặt ngày.  
- `date +%T -s "00:29:00"`: Đặt giờ.  

---

## 10. Lệnh xem thông tin file và thư mục
- `ls`: Liệt kê file và thư mục.  
- `ls tenthumuc`: Liệt kê nội dung trong thư mục chỉ định.  
- `ls -l`: Liệt kê chi tiết file (kích thước, quyền, ngày cập nhật).  
- `ls -a`: Hiển thị cả file ẩn.  
- `pwd`: Hiển thị đường dẫn hiện tại.  
- `cd`: Di chuyển thư mục.  
- `df`: Kiểm tra dung lượng ổ đĩa.  

---

## 11. Lệnh nén và giải nén
- `tar -cvf`: Nén file/thư mục sang định dạng `.tar`.  
- `tar -xvf`: Giải nén file `.tar`.  
- `gzip`: Nén `.tar` thành `.tar.gz`.  
- `gunzip`: Giải nén `.tar.gz`.  
- `tar -xzf`: Giải nén `.tar.gz`.  
- `tar -jxvf`: Giải nén `.tar.bz2`.  
- `unzip`: Giải nén file `.zip`.  

---

## 12. Lệnh sao lưu và phục hồi database
- `mysqldump -u root -p[dbpass] [databasename] > [database.sql]`: Sao lưu database ra file `.sql`.  
- `mysqldump -u root -p[dbpass] [databasename] | gzip -9 > [backupfile].sql.gz`: Sao lưu và nén database.  
- `mysql -u username -p[dbpass] [databasename] < [database].sql`: Khôi phục database.  


- timedatectl kiểm soát hệ thống ngày giờ
