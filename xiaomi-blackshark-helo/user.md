# Hướng dẫn quản lý Multi-User trên Android (ADB Shell)

*Lưu ý: Các lệnh dưới đây được tối ưu để chạy trực tiếp bên trong môi trường shell của thiết bị. Hãy đảm bảo bạn đã chạy `adb shell` trước khi copy/paste các lệnh này.*

## 1. Xem danh sách người dùng
Để xem thiết bị đang có những user nào và lấy **USER_ID** của họ:
```bash
pm list users
```
*Ghi chú:* `User 0` luôn là người dùng gốc (Owner/System). Các user tạo thêm thường có ID từ `10` trở lên.

## 2. Tạo người dùng mới
Tạo một không gian người dùng mới hoàn toàn:
```bash
pm create-user "Ten_Nguoi_Dung"
```
Hệ thống sẽ trả về kết quả kèm theo ID của user mới (ví dụ: `Success: created user id 10`).

Nếu muốn tạo **Guest user** (người dùng khách):
```bash
pm create-user --guest "Khach"
```

## 3. Chuyển đổi người dùng (Switch User)
Để chuyển màn hình điện thoại sang không gian của user khác (ví dụ user ID `10`):
```bash
am switch-user 10
```

## 4. Bắt đầu hoặc Dừng một user
Khởi động user chạy ngầm (không chuyển đổi giao diện, dùng để nhận thông báo, service...):
```bash
am start-user 10
```

Dừng hẳn không gian của user đó để giải phóng RAM:
```bash
am stop-user 10
```

## 5. Quản lý ứng dụng cho User cụ thể
*   **Cài đặt file APK (file đã được copy vào bộ nhớ máy) cho user 10:**
    ```bash
    pm install --user 10 /sdcard/duong_dan_toi_file.apk
    ```
*   **Gỡ cài đặt ứng dụng của user 10:**
    ```bash
    pm uninstall --user 10 ten.goi.ung.dung
    ```
*   **Xóa toàn bộ dữ liệu ứng dụng của user 10 (Clear data):**
    ```bash
    pm clear --user 10 ten.goi.ung.dung
    ```

## 6. Xóa người dùng
Xóa hoàn toàn không gian của user (bao gồm tất cả ứng dụng và dữ liệu cá nhân của user đó):
```bash
pm remove-user 10
```

## 7. Mẹo bật tính năng nếu bị nhà sản xuất ẩn
Nếu thiết bị không có sẵn tùy chọn multi-user trong Cài đặt, bạn có thể thử bật lên bằng các lệnh sau (có thể yêu cầu quyền root và khởi động lại máy):
```bash
setprop fw.max_users 3
setprop fw.show_multiuserui 1
```


Để khởi chạy một ứng dụng cụ thể dưới một không gian user nhất định (ví dụ user 10), bạn có thể sử dụng công cụ Activity Manager (am) hoặc Monkey.

Copy ứng dụng cho user khác: 
Cách 1: Sử dụng lệnh install-existing (Khuyên dùng)
Đây là cách nhanh nhất và chuẩn nhất trên các thiết bị Android hiện đại để cài một ứng dụng đã có sẵn sang một user khác (ví dụ cài cho User 10).

```
pm install-existing --user 10 ten.goi.ung.dung
```
Ví dụ với game Riot bạn vừa thao tác:

```
pm install-existing --user 10 com.riot.FFGSSea
```
