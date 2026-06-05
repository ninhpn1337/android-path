# magisk

Check adb root sudo
<img width="1080" height="600" alt="image" src="https://github.com/user-attachments/assets/21c20e4d-35da-4d68-9dc7-9112505cfeca" />

<img width="1108" height="123" alt="cmd_xFajr4UTlz" src="https://github.com/user-attachments/assets/a53d6597-87c9-401d-a3d5-14c9769e7fdf" />

ls cái đống boot ra, có boot a và boot b 

<img width="1095" height="97" alt="image" src="https://github.com/user-attachments/assets/c40aaa63-7a5b-4534-9b11-15b12f3f0f4c" />

reboot về bootloader  

<img width="1085" height="75" alt="image" src="https://github.com/user-attachments/assets/21f11aaa-8876-4053-b333-8aa155c13381" />

chạy getvar all để ra thông tin: 

<img width="1093" height="497" alt="image" src="https://github.com/user-attachments/assets/905864d1-1fc5-4a3d-bdf0-ca7ed8d7330d" />

Coppy và tim, có phần current slot là a 

<img width="1103" height="599" alt="image" src="https://github.com/user-attachments/assets/73f56158-7c9a-420c-b9cc-9d79f224aa2f" />

Chạy dd ra boot_a.img

<img width="1099" height="219" alt="cmd_OrWmhwWZjt" src="https://github.com/user-attachments/assets/f4507903-9bbe-44fb-b3d8-8e3013e20ced" />

sau đó vào magisk patch lại img rồi cài magisk là xong

```
adb reboot bootloader

fastboot boot C:\Users\admin\Downloads\magisk_patched_boot_a.img
```
