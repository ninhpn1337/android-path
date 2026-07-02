```
sm forget all
```
Quên hết thẻ nhớ 

check list thẻ nhớ có thể làm được
```
sm list-disks adoptable
```
nó sẽ hiện kiểu disk: phẩy gì gì đó.

Add force sử dụng
```
sm set-force-adoptable true
```
Bind thẻ nhớ vào sử dụng:

```
sm partition disk:179,0 private
```
