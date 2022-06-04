事先声明：此代码仅供学习，如若因个人原因造成损失，作者不接受任何责任！

正文：
这些程序只支持windows系统！
Server是服务端，放在你的电脑上打开，
Client是客户端，放在你要操控的电脑上打开！

Server功能：
    
    1. CMD控制
        输入一个CMD命令，被控制的电脑会执行这个命令！
        CMD命令不要是"cmd"等，因为这样会退出原本的Client程序，进入到cmd程序里去，会脱离控制。
    
    2. 对话框提示
        按照程序提示输入后，客户端会弹出一个对应的对话框。
    
    3. 勒索病毒
        谨慎使用！会把整个D盘加密，可以用虚拟机测试。
        执行一次加密，再执行一次解密（xor加密）
        注意：此功能我还只是做了一些实验，具体是否存在bug尚不明确，请谨慎使用！
    
    4.  整蛊恶搞
        运行Client的电脑会播放Client文件夹中的 电脑死机之歌，
        Client程序生成完后只复制Client.exe，不把 电脑死机之歌.wav 复制过去也能能够正常运行！
    
    5.  控制鼠标
        其实就是将对方鼠标固定住，但我在虚拟机上测试并不通过，但在物理机上却可以！
    
    6. 退出控制
        和Client断开连接。

编译程序我使用的是VS2022，要安装好MFC，如果出现
C1189 #error: Building MFC application with /MD[d] (CRT dll version) requires MFC shared dll version. Please #define _AFXDLL or do not use /MD[d] Server C:\Program Files\Microsoft Visual Studio\2022\Community\VC\Tools\MSVC\14.32.31326\atlmfc\include\afx.h 24
类似这样的报错，就去修改afx.h，
双击报错信息进入afx.h，
找到
#ifdef _DLL
#ifndef _AFXDLL
#error Building MFC application with /MD[d] (CRT dll version) requires MFC shared dll version. Please #define _AFXDLL or do not use /MD[d]
#endif
#endif
我的是在第22 ~ 26行
然后在他们前面加一行
#define _AFXDLL
就好了！记得先保存，然后再次生成。

程序缺点：
    1. 一台电脑只能运行一个Server。
    2. 一个Server程序同时只能有一个Client在连接，否则可能会出错！

 **我的 CSDN：Lo问我为什么看星星
转载请说明出处！** 

都看到这了，就给我一颗小星星吧~