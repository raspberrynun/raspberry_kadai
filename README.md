# ロボットシステム学 課題

1,2でのLED消灯，点灯に加えて3～9でのLED点滅が可能．
数値が大きくなるほど点滅速度が遅くなる．

インストール方法：
Makefile及びmyled.cを同ディレクトリに置き，makeコマンドでコンパイルを行う．
lsコマンドにてMakefile  Module.symvers  modules.order  myled.c  myled.ko  myled.mod.c　myled.mod.o  myled.o　の各ファイルの生成を確認後，sudo insmod myled.ko　にてインストールを行う．

使用方法：
