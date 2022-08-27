# -cオブションの付与でhello.oを生成する
$ g++ -c src/hello.cpp  
  
# 下記コマンドでlibhello.a静的ライブラリを生成する
$ ar rc libhello.a hello.o
  
# libhello.aの中身を確認
$ ar t libhello.a  
  
# main.oを作成
$ g++ -c main.cpp

# main.oにlibhello.aを静的リンクする
$ g++ main.o libhello.a

# コンパイルしたファイルを実行する
$ ./a.out