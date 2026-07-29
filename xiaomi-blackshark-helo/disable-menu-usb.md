Vụt hiển thị menu cài đặt cấu hình USB

```
adb shell
su.
setprop persist.sys.usb.config mtp,adb
```

<img width="750" height="1000" alt="image" src="https://github.com/user-attachments/assets/d99679ce-af89-4053-a647-068be7dd98ea" />

disable activity này

```
su
pm disable com.android.settings/com.android.settings.connecteddevice.usb.UsbModeChooserActivity
```
