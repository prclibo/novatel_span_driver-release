# シリアル対応化作業用メモ
### 通信用インスタンス
通信のインスタンスは全部bridge.pyのsockを利用
これをシリアル用のインスタンスに条件分岐させれば良さそう
ただしport.pyで「except socket.timeout:」が利用されている
#### メソッドの変更
socket.recv() -> serial.read()
socket.send() -> serial.write()
