# CodeBlock安装、配置编译器、创建项目、Debug（CodeBlocks安装包不带编译器需要自己安装编译器，当然有的装包自带编译器）

## 一、Code Blocks安装编译器
CodeBlocks：V -17.2 提前安装好（不带有编译器）
**（1）下面进行MinGW编译器安装**
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190817201838957.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190716205450128.png)**instsllation》apply changes**

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190716210003714.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NjI3NDc1,size_16,color_FFFFFF,t_70)
**随后看到可以在命令行下进行c或c++源程序的编译**
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190716210223328.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NjI3NDc1,size_16,color_FFFFFF,t_70)**（2）下面在CodeBlocks中配置编译器**

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190716210724385.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NjI3NDc1,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190716211409246.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NjI3NDc1,size_16,color_FFFFFF,t_70)
**可以看到已经可以使用CodeBlocks中编译程序**
## 二、使用CodeBlocks创建项目进行Debug并且运行
**前提条件：** 创建project

**侧边栏（资源管理器）**：view>manager

**（1）创建项目**
 start here> Creat new peoject>console application>c
工程名字可以使用汉字
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190817195534799.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NjI3NDc1,size_16,color_FFFFFF,t_70)
**(2)、编写程序代码**
在sources中的main.c中编写程序代码
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190817202736726.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NjI3NDc1,size_16,color_FFFFFF,t_70)
**(3)、在程序中添加断点**
某一行鼠标右击并且Toggle breakpoint，该行行号处出现小红点
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190818090528608.png)

**(4) 、开始debug**
**注意一：**
如果自己安装的是没有编译器的CodeBlocks那么你需要手动配置gcc编译器和dgb才可以进行debug，我本人初次配置时没有在CodeBlocks或是单独安装的MinGW编译器中找到gdb，于是借用了Dev C++里面的gdb进行debug，也就是失败的尝试：`单独安装的CodeBlocks编译器(E:\C\CodeBlocks)、单独安装的MinGw编译器(C:\MinGW)、借用的Dev C++的gdb（E:\C\Dev-Cpp\MinGW64\bin\gdb.exe），`而后发现，可以正常编译运行，但不能正常degub，google后得知可能是编译器与gdb不匹配，故强烈建议初学者直接安装带有编译器与gdb的CodeBlocks
**注意二：**
如果安装了带有编译器的CodeBlocks，其gdb的目录为：`E:\C\CodeBlocks\MinGW\bin\gdb.exe`,如不能正常debug，可以在setting-->debugger-->default--->Executable path 里面进行配置；此外发现由于之前在c盘安装过MinGW编译器，因此即使我新安装的CodeBlocks里面有MinGW编译器，CodeBlocks在检测时直接用了原来C盘下的MInGW编译器，所幸可以正常编译和debug；
以下是debug过程：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190818093735536.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NjI3NDc1,size_16,color_FFFFFF,t_70)