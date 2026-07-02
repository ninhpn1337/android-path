tải và cài

```
wget https://www.tenable.com/downloads/api/v2/pages/nessus/files/Nessus-latest-ubuntu1804_aarch64.deb
chmod +x Nessus-latest-ubuntu1804_aarch64.deb
sudo dpkg -i Nessus-latest-ubuntu1804_aarch64.deb
```
Chạy services
```
sudo /opt/nessus/sbin/nessus-service -D
```
check nessus dã chạy chưa 

```
ps aux | grep nessus
ss -tulpn | grep 8834
```
