事先声明：此代码仅供学习！

正文：
这些程序只支持windows系统。
Server是服务端，放在你的电脑上打开，
Client是客户端，放在你要操控的电脑上打开。

Server功能：
    
    1. CMD控制
        输入一个CMD命令，被控制的电脑会执行这个命令。
        CMD命令最好不要是"cmd"等打开其它程序的命令，因为这样会退出原本的Client程序，进入到cmd程序里去，会脱离控制。
    
    2. 对话框提示
        按照程序提示输入后，客户端会弹出一个对应的对话框。
    
    3. 勒索病毒
        谨慎使用！会把整个D盘加密，可以用虚拟机测试。
        执行一次加密，再执行一次解密（xor加密）
        注意：此功能我还只是做了一些实验，具体是否存在bug尚不明确，请谨慎使用！
    
    4.  整蛊恶搞
        运行Client的电脑会播放Client文件夹中的 电脑死机之歌，
        Client程序生成完后只复制Client.exe，不把 电脑死机之歌.wav 复制过去也能能够正常运行。
    
    5.  控制鼠标
        其实就是将对方鼠标固定住。
    
    6. 退出控制
        和Client断开连接。

编译程序我使用的是VS2022，要安装好MFC，使用多字节。

程序缺点：
    1. 一个Server同时只能控制一个Client。
    2. 一个Client程序同时只能有一个Server在连接。

 **我的 CSDN：Lo问我为什么看星星
转载请说明出处！** 

都看到这了，就给作者一颗小星星吧~

作者邮箱：534086753@qq.com