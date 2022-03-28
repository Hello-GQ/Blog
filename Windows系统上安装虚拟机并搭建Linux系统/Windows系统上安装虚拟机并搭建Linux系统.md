# Windows系统上安装虚拟机并搭建Linux系统

## 1 虚拟机是什么

虚拟机是一款软件，通过它可以在实体计算机上模拟出一台或多台虚拟的计算机。这些虚拟的计算机可以使用实体计算机的硬件资源，拥有实体计算机的绝大多数功能。我们可以在虚拟机中安装虚拟机所支持的操作系统，比如Linux系统或者Windows系统。
> 本段摘自：<http://c.biancheng.net/view/6448.html>
> 虚拟机（Virtual Machine）就是允许我们在当前操作系统中运行其他操作系统的软件，本质上和VS、QQ这些应用程序一样。只要我们在计算机上安装好虚拟机软件，就可以模拟出若干个相互独立的虚拟的计算机，每一个都如同一台真实的计算机，在此基础上，我们给每个虚拟计算机安装指定的操作系统，这样就可以实现在一台计算机上同时运行多个操作系统。

## 2 安装虚拟机

> 本段摘自：<http://c.biancheng.net/view/714.html>
> 许多新手连 Windows 系统的安装都不太熟悉，更别提 Linux 系统的安装了；即使安装成功，也有可能会破坏现有的 Windows 系统，比如导致硬盘数据丢失、Windows 无法开机等。所以一直以来，安装 Linux 系统都是初学者的噩梦。然而，通过虚拟机技术可以很容易地冲破这种困境。由于虚拟机安装 Linux 系统所有的操作（例如硬盘分区、删除或修改数据等）都是在虚拟硬盘中进行，因此不会对现有的数据和系统造成任何损失，即使安装失败了也无所谓。所谓虚拟机（virtual machine），就是通过软件技术虚拟出来的一台计算机，它在使用层面和真实的计算机并没有什么区别。常见的虚拟机软件有 VMware Workstation（简称 VMware）、VirtualBox、Microsoft Virtual PC 等，其中 VMware较为常用，所以这里介绍在VMware上安装Linux系统。

VMware的官方网站是<https://www.vmware.com/>，打开之后，如图1所示，首先点击【Workspace】，再点击右下角的【Workstation Player】，VMware分专业版和免费版，我们下载的是免费版，如果下载专业版，那就点击【Workstation Pro】。
![图1](https://gitee.com/guige317/blog-img_1/raw/master/Windows%E7%B3%BB%E7%BB%9F%E4%B8%8A%E5%AE%89%E8%A3%85%E8%99%9A%E6%8B%9F%E6%9C%BA%E5%B9%B6%E6%90%AD%E5%BB%BALinux%E7%B3%BB%E7%BB%9F/%E5%9B%BE1.PNG)

<center> 图1</center>

进入之后，如图2所示，点击【DOWNLOAD FOR FREE】。

![图2](https://gitee.com/guige317/blog-img_1/raw/master/Windows%E7%B3%BB%E7%BB%9F%E4%B8%8A%E5%AE%89%E8%A3%85%E8%99%9A%E6%8B%9F%E6%9C%BA%E5%B9%B6%E6%90%AD%E5%BB%BALinux%E7%B3%BB%E7%BB%9F/%E5%9B%BE2.PNG)

<center>图2</center>

进入之后，如图3所示，点击【GO TO DOWNLOADS】。

![图3](https://gitee.com/guige317/blog-img_1/raw/master/Windows%E7%B3%BB%E7%BB%9F%E4%B8%8A%E5%AE%89%E8%A3%85%E8%99%9A%E6%8B%9F%E6%9C%BA%E5%B9%B6%E6%90%AD%E5%BB%BALinux%E7%B3%BB%E7%BB%9F/%E5%9B%BE3.PNG)

<center>图3</center>

进入之后，如图4所示，点击【DOWNLOAD NOW】。

![图4](https://gitee.com/guige317/blog-img_1/raw/master/Windows%E7%B3%BB%E7%BB%9F%E4%B8%8A%E5%AE%89%E8%A3%85%E8%99%9A%E6%8B%9F%E6%9C%BA%E5%B9%B6%E6%90%AD%E5%BB%BALinux%E7%B3%BB%E7%BB%9F/%E5%9B%BE4.PNG)

<center>图4</center>

双击运行下载好的**VMware-player-full-16.2.3-19376536.exe**，安装过程比较简单，一直下一步即可。安装完成后，打开VMware，如图5所示，到这里，VMware就安装好了。

![图5](https://gitee.com/guige317/blog-img_1/raw/master/Windows%E7%B3%BB%E7%BB%9F%E4%B8%8A%E5%AE%89%E8%A3%85%E8%99%9A%E6%8B%9F%E6%9C%BA%E5%B9%B6%E6%90%AD%E5%BB%BALinux%E7%B3%BB%E7%BB%9F/%E5%9B%BE5.PNG)

<center>图5</center>

## 3 安装Linux系统

我们安装的Linux系统是Ubuntu，官网地址为<https://ubuntu.com/>。打开之后，如图6所示。

![图6](https://gitee.com/guige317/blog-img_1/raw/master/Windows%E7%B3%BB%E7%BB%9F%E4%B8%8A%E5%AE%89%E8%A3%85%E8%99%9A%E6%8B%9F%E6%9C%BA%E5%B9%B6%E6%90%AD%E5%BB%BALinux%E7%B3%BB%E7%BB%9F/%E5%9B%BE6.PNG)

<center>图6</center>

点击【Download】，如图7所示，可以看到**Ubuntu Desktop**，其下有两个版本，分别是20.04 LTS和21.10，前者"LTS"表示长时间支持（Long Time Support），下载这个版本即可，点击【20.04 LTS】。

![图7](https://gitee.com/guige317/blog-img_1/raw/master/Windows%E7%B3%BB%E7%BB%9F%E4%B8%8A%E5%AE%89%E8%A3%85%E8%99%9A%E6%8B%9F%E6%9C%BA%E5%B9%B6%E6%90%AD%E5%BB%BALinux%E7%B3%BB%E7%BB%9F/%E5%9B%BE7.PNG)

<center>图7</center>

下载完成之后，可以看到一个名为**ubuntu-20.04.4-desktop-amd64.iso**的压缩包，这是Ubuntu20.04的镜像文件。然后，再回到图5的VMware界面上来，点击【创建新虚拟机】，将弹出新建虚拟机向导，选择安装程序光盘映像文件（iso），添加刚刚下载好的ubuntu-20.04.4-desktop-amd64.iso，如图8所示。

![图8](https://gitee.com/guige317/blog-img_1/raw/master/Windows%E7%B3%BB%E7%BB%9F%E4%B8%8A%E5%AE%89%E8%A3%85%E8%99%9A%E6%8B%9F%E6%9C%BA%E5%B9%B6%E6%90%AD%E5%BB%BALinux%E7%B3%BB%E7%BB%9F/%E5%9B%BE8.PNG)

<center>图8</center>

点击【下一步】，在弹出的窗口中填写全名、用户名、密码和确认等信息，如图9所示。

![图9](https://gitee.com/guige317/blog-img_1/raw/master/Windows%E7%B3%BB%E7%BB%9F%E4%B8%8A%E5%AE%89%E8%A3%85%E8%99%9A%E6%8B%9F%E6%9C%BA%E5%B9%B6%E6%90%AD%E5%BB%BALinux%E7%B3%BB%E7%BB%9F/%E5%9B%BE9.PNG)

<center>图9</center>

点击【下一步】，然后填写虚拟机名称和位置，再点击【下一步】，如图10所示，指定虚拟机所占用的最大磁盘容量，默认使用20GB，可以根据主机的物理磁盘来调整其值的大小。

![图10](https://gitee.com/guige317/blog-img_1/raw/master/Windows%E7%B3%BB%E7%BB%9F%E4%B8%8A%E5%AE%89%E8%A3%85%E8%99%9A%E6%8B%9F%E6%9C%BA%E5%B9%B6%E6%90%AD%E5%BB%BALinux%E7%B3%BB%E7%BB%9F/%E5%9B%BE10.PNG)

<center>图10</center>

点击【下一步】，如图11所示，确认虚拟机的配置。

![图11](https://gitee.com/guige317/blog-img_1/raw/master/Windows%E7%B3%BB%E7%BB%9F%E4%B8%8A%E5%AE%89%E8%A3%85%E8%99%9A%E6%8B%9F%E6%9C%BA%E5%B9%B6%E6%90%AD%E5%BB%BALinux%E7%B3%BB%E7%BB%9F/%E5%9B%BE11.PNG)

<center>图11</center>

点击【完成】，虚拟机将开始安装Ubuntu，如图12所示，等待即可，时间可能有点长。

![图12](https://gitee.com/guige317/blog-img_1/raw/master/Windows%E7%B3%BB%E7%BB%9F%E4%B8%8A%E5%AE%89%E8%A3%85%E8%99%9A%E6%8B%9F%E6%9C%BA%E5%B9%B6%E6%90%AD%E5%BB%BALinux%E7%B3%BB%E7%BB%9F/%E5%9B%BE12.PNG)

<center>图12<center>

安装完成，如图13所示，点击账号名称，输入密码，即可进入你的Linux系统。

![图13](https://gitee.com/guige317/blog-img_1/raw/master/Windows%E7%B3%BB%E7%BB%9F%E4%B8%8A%E5%AE%89%E8%A3%85%E8%99%9A%E6%8B%9F%E6%9C%BA%E5%B9%B6%E6%90%AD%E5%BB%BALinux%E7%B3%BB%E7%BB%9F/%E5%9B%BE13.PNG)

<center>图13</center>

总的来说，安装过程还是比较简单的，这里记录一下，防止以后忘记。
