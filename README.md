# HoloCubic

* 参考稚晖君HoloCubic项目地址：https://github.com/peng-zhihui/HoloCubic.git
* 自己的项目地址：https://github.com/DingLongya/HoloCubic.git

## 简介

最近在B站看到了稚晖君的 HoloCubic 小电视，感觉很酷，正好自己刚刚结束完工训，对于 PCB 板子的贴片，焊接，组装有了一定的了解，所以自己打算学习稚晖君的 HoloCubic 项目，将它成功的复制出来。当然，希望在这个过程中学到一些知识，也算是自己在 github 上的第一个项目吧！！！

## 硬件部分

硬件部分需要的软件有 Altium Designer ，这是一个将原理图设计、电路仿真、PCB 绘制编辑、拓扑逻辑自动布线、信号完整性分析和设计输出等技术的完美融合，为设计者提供了全新的设计解决方案，使设计者可以轻松进行设计，熟练使用这一软件使电路设计的质量和效率大大提高。

### HoloCubic 项目的下载

首先在 github 上下载稚晖君HoloCubic项目，从 github 上下载项目需要用到 git ，可以直接去 https://git-scm.com/download/win 下载安装。

<img src="C:\Users\lenono\Desktop\HoloCubic项目\images\git_1.png"  />

安装完成后，新建一个文件夹，在文件夹中打开 git （git 的打开可以鼠标右键，选择Git Bash Here）。

![](C:\Users\lenono\Desktop\HoloCubic项目\images\git_2.png)

下面就是输入命令下载项目了，找到源项目的 github 地址，进入进去点击 Code 会发现有一个 ssh 地址，将它复制出来。

![](C:\Users\lenono\Desktop\HoloCubic项目\images\github_1.png)

然后返回到桌面刚刚打开的 git 中，输入命令进行下载，下载的速度可能还会有一点的慢，我用了 VPN 所以可能稍微快一些。

```git
git clone https://github.com/peng-zhihui/HoloCubic.git
```

这个命令是将远程仓库 HoloCubic 下载到当前目录下，在给 git 中复制项目地址的时候，使用原来的粘贴是不可以的，会用到 `Shift+Insert`将地址复制到 git 中，然后等待下载完成就可以了。

![](C:\Users\lenono\Desktop\HoloCubic项目\images\3.png)

下载完的这个文件夹就是项目的所有文件了，可以用相应的软件将它打开来使用了。

### 元件的购买

首先我们使用 Altium Designer 来打开硬件的第一个文件夹，文件路径应该是 ~\HoloCubic\1.Hardware\Naive Version\HoloCubic-Assembled ，后面的一部分地址是相同的。

![](C:\Users\lenono\Desktop\HoloCubic项目\images\4.png)

打开后点击 `Projects`就能看到工程文件了，然后需要输出元件表，点击`ExtendBoard.PcbDoc`就可以看到板子的 PCB 图，按下 `3`就会显示这个板子的三维图片，在三维模式下，按住鼠标右键拖拽，`鼠标右键+Shift`可以翻转查看，`Ctrl+鼠标滚轮`可以放大和缩小，同理，在 `2`模式下，除了翻转，其他都一样。在二维模式下，按下`Reports`中的`Bill of Materials`输出元件表。

![](C:\Users\lenono\Desktop\HoloCubic项目\images\6.png)

点击`Reports`中的`Bill of Materials`后，最后点击`Export`保存到指定位置就可以查看了。

![](C:\Users\lenono\Desktop\HoloCubic项目\images\7.png)

同理，输出 MainBoard.PcbDoc 的元件也是同样的操作。

![](C:\Users\lenono\Desktop\HoloCubic项目\images\8.png)

至此，我们已经能找到两个板子的 PCB 图，能够找到所要购买的元件表。元件的购买可以去日常网购软件，也可以去嘉立创去买，下面是我总结的元件表，以及在嘉立创购买的价格，仅供参考。

![](C:\Users\lenono\Desktop\HoloCubic项目\images\1.png)

![](C:\Users\lenono\Desktop\HoloCubic项目\images\9.png)

### PCB 板的打印

PCB 板的打印我选择的是嘉立创，PCB 在线下单，也是通过朋友推荐的，因为以前没有打印过 PCB 板。嘉立创对新手好像有几次的免费打印，嘿嘿，主要是想白嫖啦！哈~ 只需要按照要求提交 2 个 PCB 板的电路图，就可以了。

![](C:\Users\lenono\Desktop\HoloCubic项目\images\2.png)

这个网站感觉好高级，可以看到制作的实时进度，而且在公众号可以看到生产车间的直播，第一次打板子，感觉好高级的亚子。

![](C:\Users\lenono\Desktop\HoloCubic项目\images\10.png)

### 焊接工具的购买

因为以前自己没有焊过电路板，所以没有这些工具，简单的购买了一些必要的东西，大家可以参考一下。

![](C:\Users\lenono\Desktop\HoloCubic项目\images\5.png)



