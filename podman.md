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
