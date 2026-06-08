Usb và wifi thì dùng cái này: https://github.com/barry-ran/QtScrcpy

resize màn thì dùng 

```
adb shell wm size 1920x1080
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
