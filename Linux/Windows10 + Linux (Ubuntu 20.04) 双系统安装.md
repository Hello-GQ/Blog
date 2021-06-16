## Windows10 + Linux (Ubuntu 20.04) 双系统安装

我的笔记本上已有Windows10操作系统，需要再安装Linux操作系统，以实现双系统，所选的Linux发行版本是Ubuntu 20.04。

> 注：本教程仅适用于BIOS模式为`UEFI`的电脑

### 0.1 如何查看电脑的BIOS模式

打开Windows10，按下`Win + R`，输入`msinfo32`，如图1所示。

<div align=center><img src="http://m.qpic.cn/psc?/V53ntrZ22HgRCj3fswUG2rvUw23a8CHK/TmEUgtj9EK6.7V8ajmQrENr7O*rlCLtAmB2ij0gsOLZuC6RFg.W8r5D*yBKKx6Hyfg3OXOtC0Xgl6uCt0cJyuEGkx53goFJb8aEVGQAJ*ho!/b&bo=*AELAQAAAAADF8U!&rf=viewer_4"></div>

<div align=center>图1</div>


点击【确定】之后，可以在系统信息中看到电脑的BIOS模式为`UEFI`。

### 0.2 对BIOS模式的简要介绍 ^[1][2]^

> 要介绍BIOS模式，首先需要介绍什么是BIOS

BIOS，即Basic Input Output System，从字面上称为“基本输入输出系统”。它本质上是一段程序，包括计算机最重要的基本输入输出程序、开机后自检程序以及系统自启动程序。BIOS存储在计算机主板上一块特定的ROM芯片中。BIOS是开启计算机后CPU要处理的第一个“可执行程序”，它将带领CPU识别并加载主板上的重要硬件和集成元件，如硬盘、显卡、声卡以及各种接口等，然后按照预设的顺序读取存储器上操作系统的引导文件，通过设置的**启动模式**找到引导分区并装载操作系统，如Windows、Linux等，顺利引导操作系统之后，BIOS功成身退，隐于后台。

> 在上文中提到的启动模式即是BIOS模式















### 参考文献

[1] https://zhuanlan.zhihu.com/p/89058949

































