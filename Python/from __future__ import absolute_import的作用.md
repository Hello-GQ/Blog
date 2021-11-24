本文转载自[https://blog.csdn.net/caiqiiqi/article/details/51050800](https://blog.csdn.net/caiqiiqi/article/details/51050800)

&emsp;&emsp;关于这句`from __future__ import absolute_import`的作用，直观地看就是“从`__future__`中引入`absolute_import`”，即引入“绝对引入”。说到“绝对引入”，当然就会想起“相对引入”。那么什么是“相对引入”呢？比如说，你的文件结构如下：
&emsp;&emsp;| pkg/\n
&emsp;&emsp;&emsp;| init.py\n
&emsp;&emsp;&emsp;| main.py\n
&emsp;&emsp;&emsp;| string.py\n
&emsp;&emsp;如果你在main.py中写到`import string`，那么在python2.4或之前，python会先查找当前目录下有没有string.py，若找到了，则引入该模块，然后你在main.py中就可以直接使用string了。如果你是真的想使用当前目录下的string.py，那就没事，但是如果你是想使用系统自带的标准string.py呢？那其实没有什么好的方式可以忽略当前目录下的string.py而引入系统自带的标准string.py。此时你就需要使用`from __future__ import absolute_import`这句话了，这样你便可以使用`import string`来引入系统自带的标准string.py而使用`from pkg import string`来引入当前目录下的string.py了。

&emsp;&emsp;直白地说就是：如果你的代码是在python2.4（或之前）的环境下运行，你使用`import string`，那么只能引入当前目录下的string.py，而无法引入系统自带的string.py。但是如果你想使用`import string`来引入系统自带的string.py，那该怎么办呢？那就要从`__future__`中引入`absolute_import`，即使用`from __future__ import absolute_import`这句话，这时你可以使用`import string`来引入系统自带的string.py，使用`from pkg import string`来引入当前目录下的string.py。如果你的代码是在python2.4之后的环境下运行，那就不必加`from __future__ import absolute_import`这句话了。

