Đường dẫn data: /data/local/nhsystem/kali-arm64/podman

```
mkdir -p /podman/storage
mkdir -p /podman/tmp
nano /etc/containers/storage.conf
```

```
driver = "vfs"

runroot = "/run/containers/storage"
graphroot = "/podman/storage"
```

```
export TMPDIR=/podman/tmp
echo "export TMPDIR=/podman/tmp" >> ~/.bashrc
```
```
podman info | grep -E "graphRoot|tmp"
```

Nếu nó trả về đường dẫn /podman/storage nghĩa là cấu hình chuẩn bài.

 Dọn dẹp cache lưu trữ cũ của overlay
```
rm -rf /podman/storage/*
```
# 2. Khởi chạy lại lệnh run Acunetix
```
podman run -d -p 3443:3443 -v acunetix_data:/home/acunetix/.acunetix --restart=unless-stopped --name=acunetix_web quay.io/hiepnv/acunetix
```

Chạy natport: 
```
podman run -d --name test-web --network my-net -p 0.0.0.0:8080:80 nginx
```

Firewall: 
```
New-NetFirewallRule -DisplayName "Mở Port 8080 Podman" -Direction Inbound -LocalPort 8080 -Protocol TCP -Action Allow
netsh interface portproxy add v4tov4 listenport=8080 listenaddress=0.0.0.0 connectport=8080 connectaddress=127.0.0.1
```

dọn dẹp 

```
netsh interface portproxy delete v4tov4 listenport=8080 listenaddress=0.0.0.0
Remove-NetFirewallRule -DisplayName "Mở Port 8080 Podman"
```
