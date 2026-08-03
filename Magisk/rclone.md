tải cái này về 

```
https://github.com/NewFuture/rclone-fuse3-magisk/releases/tag/v1.75.0
```

config: chạy

```
vi /data/adb/modules/rclone/system/vendor/bin/rclone-mount
```

Trong đoạn script trên, bạn hãy tìm đến dòng số 13 (ngay dưới chữ mkdir -p "$MNT_DIR"):

```
nice -n 1 rclone mount "$NAME:" "$MNT_DIR" "$@"
```

sửa thành

```
nice -n 1 rclone mount "$NAME:" "$MNT_DIR" --dir-cache-time 10s --vfs-cache-mode writes --daemon "$@"
```

rồi lưu lại
