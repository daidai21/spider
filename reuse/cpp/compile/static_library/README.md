# 静态库

步骤：

1. 将代码文件编译成目标文件.o `g++ -c say.cpp`
2. 通过ar工具将目标文件打包成.a静态库文件 `ar -crv libsay.a say.o`
3. 使用库`g++ main.cpp -L./ -lsay` -L表示要连接的库所在目录;-l指定链接时需要的动态库，编译器查找动态连接库时有隐含的命名规则，即在给出的名字前面加上lib，后面加上.a或.so来确定库的名称。
