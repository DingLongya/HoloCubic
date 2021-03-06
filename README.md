# HoloCubic

* 参考稚晖君项目地址：https://github.com/peng-zhihui/HoloCubic.git
* 参考ClimbSnail项目地址：https://github.com/ClimbSnail/HoloCubic_AIO
* 参考教程 UP：一叶知秋君莫笑我 https://www.bilibili.com/video/BV11h41147iJ

## 简介

### 写在前面

最近在B站看到了稚晖君的 HoloCubic 小电视，感觉很酷，正好自己刚刚结束完工训，对于 PCB 板子的贴片，焊接，组装有了一定的了解，所以自己打算学习稚晖君的 HoloCubic 项目，将它成功的复制出来。当然，希望在这个过程中学到一些知识，也算是自己在 github 上的第一个项目吧！！！

### 成品展示

![](/images/y_1.jpg)

## 硬件部分

硬件部分需要的软件有 Altium Designer ，这是一个将原理图设计、电路仿真、PCB 绘制编辑、拓扑逻辑自动布线、信号完整性分析和设计输出等技术的完美融合，为设计者提供了全新的设计解决方案，使设计者可以轻松进行设计，熟练使用这一软件使电路设计的质量和效率大大提高。

### HoloCubic 项目的下载

首先需要在 github 上下载稚晖君的HoloCubic项目，从 github 上下载项目需要用到 git ，这里需要学习一些 git 命令，可以直接去 https://git-scm.com/download/win 下载安装。

![](/images/git_1.png)

安装完成后，新建一个文件夹，在文件夹中打开 git （git 的打开可以鼠标右键，选择Git Bash Here）,会弹出下面这样一个窗口 。

![](/images/git_2.png)

下面就是输入命令下载项目了，找到源项目的 github 地址，进入进去点击 Code 会发现有一个 ssh 地址，将它复制出来。

![](/images/github_1.png)

然后返回到桌面刚刚打开的 git 中，输入命令进行下载，下载的速度可能还会有一点的慢，我用了 VPN 所以可能稍微快一些。

```git
git clone https://github.com/peng-zhihui/HoloCubic.git
```

这个命令是将远程仓库 HoloCubic 下载到当前目录下，在给 git 中复制项目地址的时候，使用原来的粘贴是不可以的，会用到 `Shift+Insert`将地址复制到 git 中，然后等待下载完成就可以了。

![](/images/3.png)

等待下载，下载完的这个文件夹就是项目的所有文件了，可以用相应的软件将它打开使用了。

### 元件的购买

首先我们使用 Altium Designer 来打开硬件的第一个文件夹，文件路径应该是 ~\HoloCubic\1.Hardware\Naive Version\HoloCubic-Assembled ，后面的一部分地址是相同的。

![](/images/4.png)

打开后点击 `Projects`就能看到工程文件了，然后需要输出元件表，点击`ExtendBoard.PcbDoc`就可以看到板子的 PCB 图，按下 `3`就会显示这个板子的三维图片，在三维模式下，按住鼠标右键拖拽，`鼠标右键+Shift`可以翻转查看，`Ctrl+鼠标滚轮`可以放大和缩小，同理，在 `2`模式下，除了翻转，其他都一样。在二维模式下，按下`Reports`中的`Bill of Materials`输出元件表。

![](/images/6.png)

点击`Reports`中的`Bill of Materials`后，最后点击`Export`保存到指定位置就可以查看了。

![](/images/7.png)

同理，输出 MainBoard.PcbDoc 的元件也是同样的操作。

![](/images/8.png)

至此，我们已经能找到两个板子的 PCB 图，能够找到所要购买的元件表。元件的购买可以去日常网购软件，也可以去嘉立创去买，下面是我总结的元件表，以及在嘉立创购买的价格，仅供参考。

![](/images/1.png)

![](/images/9.png)

### PCB 板的打印

PCB 板的打印我选择的是嘉立创，PCB 在线下单，也是通过朋友推荐的，因为以前没有打印过 PCB 板。嘉立创对新手好像有几次的免费打印，嘿嘿，主要是想白嫖啦！哈~ 只需要按照要求提交 2 个 PCB 板的电路图（我已经打包好了**2.打板提交的Gerber **），分别提交就可以了。

![](/images/2.png)

这个网站感觉好高级，可以看到制作的实时进度，而且在公众号可以看到生产车间的直播，第一次打板子，感觉会很好玩，可能是刚接触硬件吧！

![](/images/10.png)

打板的时候提交的是 PCB，也可以提交 Gerber ,可以将一些不知道的错误降到最低风险，也有效的解决了因为软件版本不同，所带来的兼容性问题，下面是提交打板所生成的板子图片 ，这里一共是两块板子。

<img src="/images/实物仿真图.png" style="zoom:50%;" />

<img src="/images/实物仿真图_2.png" style="zoom:50%;" />

### 焊接工具的购买

因为以前自己没有焊过电路板，所以没有这些工具，简单的购买了一些必要的东西，大家可以参考一下。

![](/images/5.png)

## 软件部分

### 编译 ESP32 的固件

打开 VS Code 将稚晖君的 ESP32 固件成功的编译一下，选择 PIO Home 的新建工程，按照下图选择新建。

![](/images/ESP_1.png)

第一次新建固件工程会很慢，由于 PIO Home 的服务器在外国，所以需要翻墙 ，等待安装相关的配置环境。

![](/images/Q_2.png)

成功打开以后，点击左下角的的对号，我们编译一下，如果成功的编译显示了 SUCCESS 表示环境成功的安装了，可以进行下一步的操作。

![](/images/ESP_2.png)

前几步的操作完成后，我们打开稚晖君的过程项目，选择右上角的文件，打开文件夹，打开相关工程的地址，打开的过程中选择是，我们信任。

![](/images/ESP_3.png)

然后，找到工程的主函数，编译一下，至于下载`Upload`到板子，等板子焊接完成后在进行下载。

![](/images/ESP_4.png)

### 用 VS Code 仿真 LVGL

安装这个仿真环境的好处在于不用每时每刻都往板子里面下载程序，看运行情况，有了这个仿真，就可以在电脑上进行调试了，调试完以后，在往板子上面下载，回很方便，第一步就是需要下载 MSYS2 配置环境，MSYS2 的下载地址：https://www.msys2.org/ ，直接下一步下一步安装就可以了。

![](/images/ESYS2.png)

安装完以后，在 ESYS2 软件中执行命令`pacman -S mingw-w64-x86_64-gcc mingw-w64-x86_64-SDL2`选择 Y 等待配置完毕。

![](/images/ESYS.png)

接下来配置 ESYS2 的环境变量，电脑搜索打开到编辑系统环境变量，选择系统变量中的 Path ，点击新建，输入         C:\msys64\mingw64\bin，输入完点击确认。

![](/images/ESYS_2.png)

紧接着去https://github.com/Sakulaczx/platfrmioSimLvgl 下载 **2_2.platfrmioSimLvgl** 工程，下载完以后，选择打开文件夹就可以了。

![](/images/PIO_ESYS_1.png)

点击VS Code 左下角对号进行编译，编译成功后直接 Upload 下载，运行成功了。

![](/images/LV_2.png)

修改源码 demo.c 中，恢复 90~140 行的代码，注释掉 88 行的代码，就可以显示下图了。

![](/images/LV_3.png)

到这里用 VS Code 仿真 LVGL 就算是成功了。

### 用 Fusion 360 打开 3D 模型

可以在官网下载好 Fusion 360 学生的话有免费的教育优惠体验，下载以后就可以点击右上角文件。

![](/images/F_1.png)

然后在指定为位置打开 3D 文件，如下图。

![](/images/F_2.png)

打开以后按下鼠标中间滚轮可以移动模型位置，滑动滚轮可以放大缩小，按下 `Shift + 中间滚轮` 可以 3D 翻转查看。

![](/images/F_3.png)

### 练习

#### 用 AD 画一个 ExtandBoard

在等待元件的过程中，可以学习画 AD ，使用 Altium Designer 来仿照稚晖君的电路板的绘画出原理图和 PCB 图，在这个过程中，可以学到  Altium Designer 的简单使用，原理图和 PCB 图的绘画。相关的参考步骤可以去 CSDN https://blog.csdn.net/qq_45459526/category_11536027.html?spm=1001.2014.3001.5482 查看 。

#### 用 Fusion 360 画一个零部件

CSDN https://blog.csdn.net/qq_45459526/article/details/121959702?spm=1001.2014.3001.5501 查看。

## 焊接

焊接的过程需要细心，因为元件很小很小。

![](/images/H1.jpg)

![](/images/H3.jpg)

![](/images/H2.jpg)

![](/images/H4.jpg)

## 组装

![](/images/p_2.jpg)

![](/images/p_1.jpg)

ps:外壳需要螺丝，但是最后没办法，我直接用 uv 胶水固化了，也是可以的。

## 作品演示

演示视频可以去：https://b23.tv/eteRlfE





