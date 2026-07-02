Mở kali services rồi chạy

```
adb remount
adb shell
echo "/data/data/com.offsec.nethunter/scripts/bootkali" > kali
chmod +x kali
./kali
```

Đẩy file vào kali trong điện thoại:

```
adb push [Đường_dẫn_file_trên_PC] /tmp/tên_file
adb shell
su
mv /tmp/tên_file /data/local/nhsystem/kali-arm64/usr/bin/
chmod 755 /data/local/nhsystem/kali-arm64/usr/bin/tên_file
```

####VNC####

set password với 
```
vncpasswd
```

sau đó dùng lệnh này để bật giao diện đồ họa
```
vncserver :1 -geometry 1920x1080 -depth 24 -localhost no
```

oneliner:

```
echo "alias startvnc='vncserver :1 -geometry 1920x1080 -depth 24 -localhost no'" >> ~/.bashrc
source ~/.bashrc
```
