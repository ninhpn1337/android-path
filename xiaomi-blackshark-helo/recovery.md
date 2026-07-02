
[Hovatek] Qualcomm Auto TWRP Recovery Porter V1.4 by Team Hovatek: https://github.com/Rprop/Auto-TWRP-recovery-porter/releases

Kiểm tra lúc đang ở adb shell (Máy đang bật)
Ngay trong cửa sổ dòng lệnh có dấu # (sau khi gõ su), ông gõ lệnh này để hỏi thẳng hệ điều hành xem nó đang boot từ đâu:

```
getprop ro.boot.slot_suffix
```
Nếu nó nhả ra chữ _a -> Máy đang chạy slot A. Lệnh dump vbmeta_a của ông hoàn toàn chính xác.
```
dd if=/dev/block/bootdevice/by-name/vbmeta_a of=/sdcard/vbmeta_goc.img
```
Nếu nó nhả ra chữ _b -> Máy đang chạy slot B. Ông phải sửa cái lệnh dd lại một chút thành:
```
dd if=/dev/block/bootdevice/by-name/vbmeta_b of=/sdcard/vbmeta_goc.img
```

Cách 2: Kiểm tra lúc đang ở chế độ Fastboot
Nếu ông lỡ tắt máy và đang đứng ở màn hình Bootloader/Fastboot, mở CMD trên máy tính và gõ:

```
fastboot getvar current-slot
```

Giết Lớp khiên bảo vệ tính toàn vẹn của hệ thống (AVB) - vbmeta để boot recovery

```
fastboot --disable-verity --disable-verification flash vbmeta vbmeta_goc.img
```

Nếu nó báo kiểu này là ok: 
```
Rewriting vbmeta struct at offset: 0

Sending 'vbmeta' (64 KB)                           OKAY [  0.003s]

Writing 'vbmeta'                                   OKAY [  0.003s]
```

Run cho nó cẩn thận, tuy nhiên có thể không chạy được: 

```
fastboot boot twrp_recovert_da_port.img
```

Flash: 

```
fastboot flash boot_a twrp_recovert_da_port.img
fastboot reboot
```

Nếu hỏng: lấy boot_a_goc.img ra và chạy 
```
fastboot flash boot_a boot_a_goc.img
```
