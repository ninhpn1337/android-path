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
