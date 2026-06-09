Cách tìm file thì là 
```
find / -name "Game.cfg" 2>/dev/null
```

Sẽ tìm ra 1 file ở 
/data/data/com.riotgames.league.teamfighttacticsvn/no_backup/Config/Game.cfg

<img width="726" height="68" alt="image" src="https://github.com/user-attachments/assets/13862158-dc96-4af4-ab7c-bf2f5409c24f" />

chúng ta vi cái file Game.cfg này 

Sửa từ WaitForVerticalSync=0 thành WaitForVerticalSync=1

nếu nó có ^M thì kệ nó nhé. Chỉ replace từ 0 thành 1

<img width="253" height="262" alt="cmd_ulr05XGQzD" src="https://github.com/user-attachments/assets/eb325e74-9bb0-416a-a534-6c048e80b19d" />

Thế là ok rồi.
