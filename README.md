# ロボットシステム学 課題

0,1でのLED消灯，点灯に加えて2～9でのLED点滅が可能．
数値が大きくなるほど点滅速度が遅くなる．

インストール方法：
Makefile及びmyled.cを同ディレクトリに置き，makeコマンドでコンパイルを行う．
lsコマンドにてMakefile  Module.symvers  modules.order  myled.c  myled.ko  myled.mod.c　myled.mod.o  myled.o　の各ファイルの生成を確認後，sudo insmod myled.ko　にてインストールを行う．

使用方法：
$ sudo mknod /dev/myled0 c 243 0
$ sudo chmod 666 /dev/myled0
以上を行い，echo 1～9　> /dev/myled0 にてLEDの点灯を行う．0は消灯．
出力ピンはGPIO25となる．

点灯パターン：
0 消灯
1 連続点灯
2～9 点滅点灯 （数値が大きくなるほど点滅速度が遅くなる）

