```
pm uninstall -k --user 0 com.miui.analytics
pm uninstall -k --user 0 com.xiaomi.joyose
pm uninstall -k --user 0 com.miui.daemon
```

```
# Bộ sậu quảng cáo, phân tích hành vi của Xiaomi & Black Shark
pm uninstall -k --user 0 com.miui.systemAdSolution
pm uninstall -k --user 0 com.blackshark.analytics
pm uninstall -k --user 0 com.mfashiongallery.emag
pm uninstall -k --user 0 com.xiaomi.discover

# Chuyên thu thập dữ liệu sử dụng phần cứng, log lỗi ngầm
pm uninstall -k --user 0 com.blackshark.zsappusagecollector
pm uninstall -k --user 0 com.miui.hybrid
pm uninstall -k --user 0 com.miui.hybrid.accessory
pm uninstall -k --user 0 com.miui.vsimcore
pm uninstall -k --user 0 com.miui.virtualsim

# App diễn đàn và cửa hàng riêng của Black Shark (rất thừa nếu không dùng)
pm uninstall -k --user 0 com.blackshark.forum
pm uninstall -k --user 0 com.blackshark.store
pm uninstall -k --user 0 com.xiaomi.gamecenter
```

```
pm uninstall -k --user 0 com.android.fileexplorer
pm uninstall -k --user 0 com.android.browser
pm uninstall -k --user 0 com.xp.browser
pm uninstall -k --user 0 cn.wps.moffice_eng.xiaomi.lite
```

```
echo ">>> BAT DAU DON DEP HE THONG (DEBLOAT) <<<"

echo "1. Xoa dich vu thu thap du lieu va quang cao..."
pm uninstall -k --user 0 com.blackshark.analytics
pm uninstall -k --user 0 com.miui.systemAdSolution
pm uninstall -k --user 0 com.miui.contentcatcher
pm uninstall -k --user 0 com.miui.catcherpatch
pm uninstall -k --user 0 com.tencent.cmocmna
pm uninstall -k --user 0 com.blackshark.zsappusagecollector

echo "2. Xoa cac cho ung dung va cong thanh toan noi dia..."
pm uninstall -k --user 0 com.xiaomi.market
pm uninstall -k --user 0 com.xiaomi.payment
pm uninstall -k --user 0 com.blackshark.store
pm uninstall -k --user 0 com.blackshark.pay
pm uninstall -k --user 0 com.blackshark.payment
pm uninstall -k --user 0 com.tencent.egame
pm uninstall -k --user 0 com.xiaomi.gamecenter
pm uninstall -k --user 0 com.xiaomi.gamecenter.sdk.service

echo "3. Xoa dich vu Cloud cua Xiaomi..."
pm uninstall -k --user 0 com.miui.cloudservice
pm uninstall -k --user 0 com.miui.cloudbackup
pm uninstall -k --user 0 com.miui.micloudsync
pm uninstall -k --user 0 com.xiaomi.micloud.sdk
pm uninstall -k --user 0 com.miui.vsimcore
pm uninstall -k --user 0 com.miui.virtualsim

echo "4. Xoa cac ung dung rac khong can thiet..."
pm uninstall -k --user 0 com.android.browser
pm uninstall -k --user 0 com.miui.video
pm uninstall -k --user 0 com.miui.player
pm uninstall -k --user 0 com.miui.yellowpage
pm uninstall -k --user 0 cn.wps.moffice_eng.xiaomi.lite
pm uninstall -k --user 0 com.baidu.input_heisha

echo ">>> HOAN THANH DON DEP! <<<"
```
Nếu bạn không quan tâm đến thông báo từ các app Trung Quốc, bạn có thể chạy thêm lệnh:
```
pm uninstall -k --user 0 com.xiaomi.xmsf.
```
