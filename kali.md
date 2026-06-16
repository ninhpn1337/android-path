Mở kali services rồi chạy

```
adb remount
adb shell
echo "/data/data/com.offsec.nethunter/scripts/bootkali" > kali
chmod +x kali
./kali
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
