Update zip: *#*#1027#*#* - ném vào OTA/update.zip

```
fastboot flash boot_a boot_a_4
fastboot flash boot_b boot_b_4
fastboot flash dtbo_a dtbo_a_4
fastboot flash dtbo_b dtbo_b_4
fastboot flash vbmeta_a vbmeta_a_4
fastboot flash vbmeta_b vbmeta_b_4
fastboot flash system_a system_a_0
fastboot flash system_b system_b_0
fastboot flash vendor_a vendor_a_0
fastboot flash vendor_b vendor_b_0

```


```
fastboot flash modem_a modem_a_4
fastboot flash modem_b modem_b_4
fastboot flash dsp_a dsp_a_4
fastboot flash dsp_b dsp_b_4
fastboot flash bluetooth_a bluetooth_a_4
fastboot flash bluetooth_b bluetooth_b_4
```

```
fastboot --set-active=a
fastboot format:ext4 userdata
fastboot reboot
```
