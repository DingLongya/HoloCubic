

# 这里将会记录在整个项目过程中软硬件出现的一些问题

1. 在安装 PIO Home 插件以后，打不开这个插件，显示一直 Loading……，并伴随着左侧的错误输出，错误如下图

![](/images/Q_1.png)

解决方法：这种情况下多数是网络问题造成的，所以重启 VS Code 是不行的，必须重启电脑，可能还需要翻墙。



2.在 VS Code 下载了 PIO Home 插件以后，新建工程打开慢，一般情况下会很慢，往往需要睡一觉起来就好了，但是我的 2 天了，还没有好，如下图

![](/images/Q_2.png)

解决方法：网络的问题，需要翻墙，因为要下载安装一些东西，服务器在外国，所以很慢，建议翻墙多试试几次。



3.在使用 VS Code 打开 platfrmioSimLvgl 的过程中，出现错误的情况，如下图

![](/images/LV_1.png)

解决方法：需要配置 C/C++环境，可以看教程https://blog.csdn.net/qq_29339467/article/details/104096661?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522163936862216780366512016%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=163936862216780366512016&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-2-104096661.pc_search_result_control_group&utm_term=vscode%E9%85%8D%E7%BD%AEc%2B%2B%E7%8E%AF%E5%A2%83&spm=1018.2226.3001.4187来就可以了，我配置完以后就可以正常编译这个工程文件了，但是我自己建立的 .cpp 文件还是不可以，可能建立的有问题。 



4.焊接完以后，电脑不识别板子

解决方法：芯片虚焊，重新焊接。

5.焊接是个大问题

解决方法：买一个放大镜，细心一些。
