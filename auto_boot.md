Đưa điện thoại vào chế độ Fastboot (adb reboot bootloader).

Mở terminal trên máy tính và chạy lệnh sau tùy thuộc vào dòng chip của máy:

Đối với hầu hết các máy (bao gồm cả Xiaomi/Black Shark):

```
fastboot oem off-mode-charge 0
```
Nếu lệnh trên báo lỗi, hãy thử lệnh này:


```
fastboot oem charging auto-boot 1
```
