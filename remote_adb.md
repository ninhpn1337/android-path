Usb và wifi thì dùng cái này: https://github.com/barry-ran/QtScrcpy

reset mọi thứ về gốc: 

```
adb shell wm size reset
adb shell wm density reset
adb shell svc power stayon false
adb shell settings put system screen_brightness_mode 1
adb shell settings put system screen_brightness 500
```

resize màn thì dùng 


```
adb shell wm size 1080x1920
```

Ép máy không bao giờ ngủ: 

```
adb shell svc power stayon true
```

Tắt độ sáng tự động và ép sáng về 0:

```
adb shell settings put system screen_brightness_mode 0
adb shell settings put system screen_brightness 0
```

Tăng điểm ảnh: 

```
adb shell wm density 420
```
Tắt thông báo cắm usb
```
su
settings put global usb_remember_choice 1
```
Đẩy file (với root) - Nếu có arm64 hoặc aarch64 thì có thể đẩy thằng vào /system/bin/ để gọi được nhé 
```
adb remount
adb push [Đường_dẫn_file_trên_PC] [Đường_dẫn_thư_mục_trên_ĐT]
```

Đẩy file vào kali trong điện thoại: 

```
adb push [Đường_dẫn_file_trên_PC] /tmp/tên_file
adb shell
su
mv /tmp/tên_file /data/local/nhsystem/kali-arm64/usr/bin/
chmod 755 /data/local/nhsystem/kali-arm64/usr/bin/tên_file
```
