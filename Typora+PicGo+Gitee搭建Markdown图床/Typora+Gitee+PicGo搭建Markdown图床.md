# Typora+PicGo+Gitee搭建Markdown图床

在准备搭建Markdown图床之前，对比了常用的一些搭建方法，最终选择采用Typora+PicGo+Gitee的方式来搭建Markdown图床。类似的文章在网上可以找到很多，也是在这些文章的帮助下我才将搭建过程搞明白。在这里我将我的搭建过程记录下来，以防以后忘记。如果存在错误之处，欢迎指正。<br>

首先，下载Typora，下载地址为<https://typoraio.cn/>。根据你所使用的操作系统选择对应的下载，这里我使用的是Windows系统（64位），因此点击红框处的【64位】，如图1所示。<br>

<div>			
    <center><!--将图片和文字居中-->
    <img src="https://gitee.com/guige317/blog-img_1/raw/master/Typora+Gitee+PicGo%E6%90%AD%E5%BB%BAMarkdown%E5%9B%BE%E5%BA%8A/1.PNG"
         alt="图1"
         style="zoom:这里写图片的缩放百分比"/>
    <br><!--换行-->
    图1<!--标题-->
    </center>
</div>


双击运行下载好的**typora-setup-x64.exe**，安装过程比较简单。<br>

安装完成之后，打开Typora。这里下载的版本是1.1.5，Typora在1.0之后就开始收费了，89元，不讨论收费问题，我购买了激活码，填入之后，重新打开Typora。依次点击【文件】→【偏好设置】→【图像】，按照图2选择对应的设置。<br>

<div>
	<center>
	<img src="https://gitee.com/guige317/blog-img_1/raw/master/Typora+Gitee+PicGo%E6%90%AD%E5%BB%BAMarkdown%E5%9B%BE%E5%BA%8A/2.PNG"
		 alt="图2"
         style="zoom:"/>
	<br>
	图2
	</center>
</div>


在图2的右下角可以看到【下载PicGo (app)】，点击进入PicGo官网。<br>

PicGo是一款比较好用的图片上传工具。进入官网之后，如图3所示，点击【免费下载】。<br>

<div>
    <center>
        <img src="https://gitee.com/guige317/blog-img_1/raw/master/Typora+Gitee+PicGo%E6%90%AD%E5%BB%BAMarkdown%E5%9B%BE%E5%BA%8A/3.PNG"
             alt="图3"
             style="zoom:"/>
        <br>
        图3
    </center>
</div>


然后我们会进入PicGo的github仓库，要下载的版本是2.3.0（最新版），这里我们可以看到2.3.0的新增特性以及修复了哪些bug，在**Assets**中，选择下载**PicGo-Setup-2.3.0-x64.exe**，如图4所示。<br>

<div>
    <center>
        <img src="https://gitee.com/guige317/blog-img_1/raw/master/Typora+Gitee+PicGo%E6%90%AD%E5%BB%BAMarkdown%E5%9B%BE%E5%BA%8A/4.PNG"
             alt="图4"
             style="zoom:"/>
        <br>
        图4
    </center>
</div>


双击运行下载好的**PicGo-Setup-2.3.0-x64.exe**，安装过程比较简单。启动PicGo后，图标会在任务栏的右下角显示，单击图标打开详细窗口，如图5所示。<br>

<div>
    <center>
        <img src="https://gitee.com/guige317/blog-img_1/raw/master/Typora+Gitee+PicGo%E6%90%AD%E5%BB%BAMarkdown%E5%9B%BE%E5%BA%8A/5.PNG"
             alt="图5"
             style="zoom:"/>
        <br>
        图5
    </center>
</div>

【上传区】：可以通过拖拽或点击的方式上传单张或多张图片，上传图片转化的链接格式也在此界面中设置。<br>

【相册】：支持对单张或多张图片进行复制、删除等操作，支持对图片的Url进行修改，可以设置复制图片链接的格式。<br>

【图床设置】：这里选择要使用的图床，目前可供选择的图床有SM.MS图床、腾讯云COS、GitHub图床、七牛图床、Imgur图床、阿里云OSS、又拍云图床。这里没有我们要使用的Gitee图床，先不必着急。<br>

【PicGo设置】：这里对PicGo进行配置。在配置**设置日志文件**时，日志记录等级可以仅保留错误-Error和提醒-Warn；在**选择显示的图床**时，因为这些图床都不是我们要使用的图床，因此全部取消勾选，这时你会发现【图床设置】中提供的图床也相应地消失了。至于其他配置项目，保持默认即可。<br>

【插件设置】：因为PicGo提供的图床中没有我们要使用的Gitee图床，因此我们需要安装gitee插件。在搜索栏中输入**gitee**，如图6所示，这里我选择的插件是**gitee-uploader 1.1.2**。<br>

<div>
    <center>
        <img src="https://gitee.com/guige317/blog-img_1/raw/master/Typora+Gitee+PicGo%E6%90%AD%E5%BB%BAMarkdown%E5%9B%BE%E5%BA%8A/6.PNG"
             alt="图6"
             style="zoom:"/>
        <br>
        图6
    </center>
</div>


在点击安装时，可能会弹出如图7所示的错误，说明系统中没有安装node.js环境。<br>

<div>
    <center>
        <img src="https://gitee.com/guige317/blog-img_1/raw/master/Typora+Gitee+PicGo%E6%90%AD%E5%BB%BAMarkdown%E5%9B%BE%E5%BA%8A/7.PNG"
             alt="图7"
             style="zoom:"/>
        <br>
        图7
    </center>
</div>

> 本段引用于参考文献2
>
> PicGo采用Electron-vue开发，虽然运行程序编译成了.exe可执行文件，但是其插件还是依赖于node.js环境，因此如果需要安装插件就必须先安装node.js环境（gitee必须安装插件），若是程序自带的图床接口（SM.MS图床、腾讯云COS、Github图床、七牛图床、Imgur图床、阿里云OSS、又拍云）可不需要安装node.js。

那我们安装一下，Node.js的官网是<https://nodejs.org/en/>，如图8所示。<br>

<div>
    <center>
        <img src="https://gitee.com/guige317/blog-img_1/raw/master/Typora+Gitee+PicGo%E6%90%AD%E5%BB%BAMarkdown%E5%9B%BE%E5%BA%8A/8.PNG"
             alt="图8"
             style="zoom:"/>
        <br>
        图8
    </center>
</div>


点击【16.14.2 LTS】，LTS表示长时间支持（Long Time Support）。双击运行下载好的**node-v16.14.2-x64.msi**，按需修改安装路径，在**Tools for Native Modules**界面不必打勾，一直Next，安装完成。<br>

检验一下Node.js是否安装成功，打开cmd运行命令提示符，分别输入`node -v`和`npm -v`，如果都能正常显示版本号，说明Node.js安装成功。<br>

回到gitee插件的安装，这时我们再次点击安装，就可以成功安装gitee插件了。在【PicGo设置】的**选择显示的图床**中可以看到多出一个选项gitee，打勾；在【图床设置】中可以看到gitee，点击gitee可以看到如图9所示的界面。<br>

<div>
    <center>
        <img src="https://gitee.com/guige317/blog-img_1/raw/master/Typora+Gitee+PicGo%E6%90%AD%E5%BB%BAMarkdown%E5%9B%BE%E5%BA%8A/9.PNG"
             alt="图9"
             style="zoom:"/>
        <br>
        图9
    </center>
</div>

接下来的任务就是填写这些空白项了，我们需要去gitee网站进行一些操作。<br>

gitee官网地址为<https://gitee.com/>，首先需要注册一个账号，登录之后进入如图10所示的界面。<br>

<div>
    <center>
        <img src="https://gitee.com/guige317/blog-img_1/raw/master/Typora+Gitee+PicGo%E6%90%AD%E5%BB%BAMarkdown%E5%9B%BE%E5%BA%8A/10.PNG"
             alt="图10"
             style="zoom:"/>
        <br>
        图10
    </center>
</div>

在右上角点击**+**号，创建一个新的仓库，填入仓库名称，路径也会相应地自动生成，其他的配置可以参照图11所示。注意这里暂时选的是私有仓库，创建成功之后需要更改为开源仓库，否则会无法访问图片。<br>

<div>
    <center>
        <img src="https://gitee.com/guige317/blog-img_1/raw/master/Typora+Gitee+PicGo%E6%90%AD%E5%BB%BAMarkdown%E5%9B%BE%E5%BA%8A/11.PNG"
             alt="图11"
             style="zoom:">
        <br>
        图11
    </center>
</div>

点击【创建】之后，仓库就建好了，再点击右上角的【管理】，在里面将私有更改为开源，三个承诺也勾选上，保存。<br>

这时再看图9，第一个空白项repo也就是你的仓库了，gitee的官网地址加上这个repo就是你的仓库地址，进入你的仓库后查看一下页面的地址栏，如图12所示。<br>

<div>
    <center>
        <img src="https://gitee.com/guige317/blog-img_1/raw/master/Typora+Gitee+PicGo%E6%90%AD%E5%BB%BAMarkdown%E5%9B%BE%E5%BA%8A/12.PNG"
             alt="图12"
             style="zoom:">
        <br>
        图12
    </center>
</div>

在地址栏中，当前地址为gitee.com/guige317/blog-img_1，去掉官网地址，也就是guige317/blog-img_1，将它填入图9的repo空白项中。第二个空白项branch表示要使用的分支，因为仓库当前只有一个主分支master，那就填入master。第三个空白项token，表示你的私人令牌，怎么获取呢？在图12中最右上角有个大写的G，表示你的登录信息，单击，选择【设置】，再单击左侧边栏中【私人令牌】，如图13所示。<br>

<div>
    <center>
        <img src="https://gitee.com/guige317/blog-img_1/raw/master/Typora+Gitee+PicGo%E6%90%AD%E5%BB%BAMarkdown%E5%9B%BE%E5%BA%8A/13.PNG"
             alt="图13"
             style="zoom:">
        <br>
        图13
    </center>
</div>

右上角有个**+生成新令牌**，点击。进入私人令牌的生成界面，在填写私人令牌描述时，自定义一个名称，可以随意，或者干脆就写blog-img_1，在请选择将要生成的私人令牌所拥有的权限时，可以仅勾选projects，具体如图14所示。

<div>
    <center>
        <img src="https://gitee.com/guige317/blog-img_1/raw/master/Typora+Gitee+PicGo%E6%90%AD%E5%BB%BAMarkdown%E5%9B%BE%E5%BA%8A/14.PNG"
             alt="图14"
             style="zoom:">
        <br>
        图14
    </center>
</div>

提交之后输入你gitee账号的密码，私人令牌即可成功生成。切记要复制你的私人令牌，因为只会出现这一次，关闭私人令牌生成提示窗口之后，就无法再看到你的私人令牌了。将你的私人令牌填入图9的第三个空白项token中。第四个空白项path，表示要在仓库中所选的分支下创建一个文件夹，用来保存你上传的图片，前面的branch中选择的master就是你当前的分支，这里我们填入这篇文章的名字，即Typora+Gitee+PicGo搭建Markdown图床，我的想法是每篇文章的图片都保存在对应名称的文件夹下，万一哪天gitee设置防盗链，是不是好迁移一些，只是一个想法。也有麻烦之处，就是每次写文章，都要来这里改一下path。剩余两个空白项customPath和customUrl保持默认即可，不需要填写。图9填写完成之后，如图15所示。这里隐藏了一下我的私人令牌。

<div>
    <center>
        <img src="https://gitee.com/guige317/blog-img_1/raw/master/Typora+Gitee+PicGo%E6%90%AD%E5%BB%BAMarkdown%E5%9B%BE%E5%BA%8A/15.PNG"
             alt="图15"
             style="zoom">
        <br>
        图15
    </center>
</div>

点击【设为默认图床】，再点击【确定】，到这里PicGo的配置已经完成了。我们再回到图2中，需要填写一下你的PicGo.exe的路径，将Typora和PicGo关联起来，这样Typora才能调用PicGo完成图片的上传，如图16中红框所示。

<div>
    <center>
        <img src="https://gitee.com/guige317/blog-img_1/raw/master/Typora+Gitee+PicGo%E6%90%AD%E5%BB%BAMarkdown%E5%9B%BE%E5%BA%8A/16.PNG"
             alt="图16"
             style="zoom:">
        <br>
        图16
    </center>
</div>

到这里，所有的配置过程都完成了，我们验证一下是否可以成功上传图片。点击图16中【验证图片上传选项】，如果出现图17中的验证成功的弹窗，表示所有的配置都没有问题，你的图片成功上传到了图床中，然后你会发现在PicGo的相册中可以看到你刚刚上传的图片，你还可以在gitee网站BlogImg_1仓库master分支的对应文件夹下看到你刚刚上传的图片。

<div>
    <center>
        <img src="https://gitee.com/guige317/blog-img_1/raw/master/Typora+Gitee+PicGo%E6%90%AD%E5%BB%BAMarkdown%E5%9B%BE%E5%BA%8A/17.PNG"
             alt="图17"
             style="zoom:">
        <br>
        图17
    </center>
</div>

以后在Typora上插入图片时，只需要将图片拖拽到编辑区，就可以将图片自动上传到你的图床上了。

写这篇文章的目的仅是记录自己的搭建过程。由于文章是在一边操作一边记录的状态下完成的，因此写的可能比较乱，像是记流水账。总结一下，首先下载并安装Typora，再下载并安装PicGo图片上传工具，在Typora中将二者关联起来；由于PicGo默认图床中没有gitee，因此我们需要安装gitee插件，在安装gitee插件时你可能需要安装一下Node.js；我们的图片最终是保存在gitee网站上的仓库中，因此这个仓库就是实际上的图床，需要获取repo和私人令牌等信息将PicGo和仓库关联起来。这样，PicGo像是一座桥梁，连接了你的Typora和gitee网站上的仓库。

参考文献：

[1] https://www.yuque.com/kinvy/b-file/img-bed

[2] https://blog.csdn.net/qq_38768365/article/details/107091900

[3] https://www.bilibili.com/video/BV1NA411F7vo?spm_id_from=333.880.my_history.page.click
