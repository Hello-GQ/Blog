本文节选自[https://www.cnblogs.com/funnything/p/11009852.html](https://www.cnblogs.com/funnything/p/11009852.html)  
&emsp;&emsp;用python写了一个项目，在第一次运行后，目录下生成了一个__ pycache  __ 文件夹，发现里面是各种与py文件同名的以.cpython-36.pyc结尾的文件。  
&emsp;&emsp;要知道__ pycache  __ 文件夹的作用，我们需要先了解python解释器的工作过程。python程序运行时不需要编译成二进制代码，只需直接从源码运行，将源码转换为字节码，然后再执行这些字节码。具体的工作过程包括：  
&emsp;&emsp;1.完成模块的加载和链接；  
&emsp;&emsp;2.将源码转换为PyCodeObject对象（即字节码），写入内存中，供cpu读取；  
&emsp;&emsp;3.从内存中读取并执行这些字节码，结束后将PyCodeObject对象写回至硬盘中，也就是复制到.pyc文件中，以保存当前目录下所有脚本的字节码。  
&emsp;&emsp;之后若再次执行该脚本，会先检查当前目录下是否有该脚本的字节码文件以及该字节码文件的修改时间是否在其源文件之后，如果是，那就直接执行字节码文件，否则就按照上述工作过程处理该脚本。  
&emsp;&emsp;在第一次执行脚本的时候，python解释器会把转换好的字节码放到__ pycache  __ 文件夹中，这样以后再次运行时，如果被调用的模块没有发生改变，那就跳过转换的步骤，直接到__ pycache  __ 文件夹中去运行相关的.pyc文件，大大缩短了脚本运行的准备时间。  

