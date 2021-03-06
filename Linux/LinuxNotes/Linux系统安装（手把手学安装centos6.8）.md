# Linux系列教程（二）——Linux系统安装（手把手学安装centos6.8）


Linux有非常多的发行版本，从性质上划分，大体分为由商业公司维护的商业版本与由开源社区维护的免费发行版本。商业版本以Redhat为代表，开源社区版本则以debian为代表。下面是三个典型的发行版：

　　CentOS是从redhat源代码编译重新发布版。**CentOS去除很多与服务器功能无关的应用**，系统简单但非常稳定，命令行操作可以方便管理系统和应用，并且有帮助文档和社区的支持。一般新手入门比较好。

　　Ubuntu有亮丽的用户界面，完善的包管理系统，强大的软件源支持，丰富的技术社区，并且Ubuntu对计算机硬件的支持好于CentOS和Debian，兼容性强，Ubuntu应用非常多。但是我们需要注意的是图形界面占用的内存非常大。

　　**Debian也非常适合做服务器操作系统**，与Ubuntu比较，它没有太多的花哨，稳定压倒一切，对于服务器系统来说是一条不变的真理，Debian这个linux系统，底层非常稳定，内核和内存的占用都非常小。

　　我们虽然选择学习的是CentOS,但是大家也不要在意，基本上学会一个系统的命令后，其余的系统都大同小异。我们是将CentOS安装在虚拟 PC，这里模拟虚拟PC的软件选择 **VMware，**所以这里安装的步骤分为两步：

　　第一步：安装虚拟软件**VMware；**

百度云盘下载链接：[https://pan.baidu.com/s/1l3Eqk_qWbDyfTMd-ZNQI-g](https://pan.baidu.com/s/1l3Eqk_qWbDyfTMd-ZNQI-g) 提取码: cmii 

第二步：安装虚拟机** CentOS 6.8；**

百度云盘下载地址：[https://pan.baidu.com/s/1MXTWPhpF7b2AzxqGVniy9A](https://pan.baidu.com/s/1MXTWPhpF7b2AzxqGVniy9A) 提取码: xftk

[回到顶部](https://www.cnblogs.com/ysocean/p/7689146.html#_labelTop)

### 1、安装 VMware

　　VMware 是一个虚拟 PC 的软件，可以在现有的操作系统上虚拟出一个新的硬件环境，相当于模拟出一台新的 PC，我们可以在上面构造出一个或多个别的系统，以此来实现在一台机器上真正同时运行多个独立的操作系统。VMware 下载链接上面给出了，安装过程都是默认下一步，下一步即可。这里就不给出安装的图示了，安装完成后，双击打开如下：

　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019223114287-986036161.png)

[回到顶部](https://www.cnblogs.com/ysocean/p/7689146.html#_labelTop)

### 2、在 VMware 上安装 CentOS

#### 　　第 1 步：打开 VMware，点击创建新的虚拟机

　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019224124818-1948063429.png)

#### 　　第 2 步：选择典型，点击下一步。出现如下界面，然后选择第三个选项：稍后安装操作系统，点击下一步

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019224149990-1342210220.png)**

#### 　　第 3 步：客户机安装操作系统选择 Linux,版本根据自己下载的 Linux 镜像文件来选择，这里我们选择 CentOS 64 位。然后点击 下一步

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019224225412-356907601.png)**

#### 　　第 4 步：给虚拟机命名，以及选择虚拟机安装的位置，最好是非中文不含空格的地址。然后点击下一步

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019224248162-1546947099.png)**

#### 　　第 5 步：默认，磁盘大小 20 GB足够。然后点击下一步

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019224308021-1284794279.png)**

#### 　　第  6 步：点击完成按钮

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019224336427-113477845.png)**

　　点击完成之后，我们会在 VMware 主界面发现我们刚刚创建的 虚拟机 Node2：

　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019224453068-2044704271.png)

#### 　　第 7 步：右键 虚拟机名称 Node2,选择设置

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019224513381-563958144.png)**

　　弹出如下界面：

　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019224531865-1716320009.png)

#### 　　第 8 步：进行虚拟机的各项硬件配置

　　①、首先调整内存大小，一般来讲，内存最低不能小于 628 m，最大不能超过 真实物理机内存的 一半。我们可以默认选择 1024M内存大小就够了

　　②、其次我们可以对处理器进行调整，对硬盘大小也可以进行调整，但是这里我们都选择默认就行了，直接跳到 CD/DVD(IDE) 选项，选择 我们下载的 CentOS 镜像文件，然后点击确定

　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019224732287-1871833803.png)

　　**注意：我们这里下载的 CentOS 6.8 有两个ISO 文件，我们选择第一个，第一个包含 CentOS 系统的主体信息，而第二个 ISO 文件只是一些不常用的软件信息**

　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019224757537-483046235.png)

　　那么经过上面的步骤，我们对于虚拟机的配置已经设置完成，接下来就进行虚拟机的安装。

#### 　　第 9 步：到 VMware 主界面，选择 我们安装的 Node2 虚拟机，点击 开启此虚拟机

　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019224901099-2117724447.png)

#### 　　第 10 步：进入欢迎界面后，选择 第一个选项：Install or upgrade an existing system ，然后 Enter。

**　　　  注意：我们鼠标进入安装界面后，需要按 Ctrl+Alt 才能使得鼠标恢复到自己的主系统。**

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019224923240-1852904690.png)**

　　其余几个选项意思是：

　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019225258756-400134511.png)

#### 　　第 11 步：询问我们是否需要检查光盘，我们按 右箭头，选择 skip 选项（即不用检测），Enter

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019225317974-157620236.png)**

#### 　　第 12 步：点击 next

 　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019225334349-1727643005.png)

#### 　　第 13 步：选择 中文简体，点击 Next

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019225352302-1647524947.png)**

#### 　　第 14 步：键盘选择 美国英语式，然后点击下一步

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019225413646-1845175214.png)**

#### 　　第 15 步：选择 基本存储设备，点击下一步

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019225429021-1844942878.png)**

#### 　　第 16 步：选择第一个，是 忽略所有数据

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019225445224-537399075.png)**

#### 　　第 17 步：给主机命名

 　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019225502849-1752132363.png)

#### 　　第 18 步：选择时区亚洲/伤害，去掉勾选使用UTC时间。然后点击 下一步

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019225623131-1461773132.png)**

#### 　　第 19 步：给根用户设置密码，然后点击 下一步。

**　　注意：如果密码设置的过于简单，系统会弹出您的密码不够安全，但是你可以选择无论如何都使用，然后继续**

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019225652162-1306034598.png)**

#### 　　第 20 步：选择进行哪种类型的安装，我们选择最后一个 创建自定义布局

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019225710631-1838954280.png)**

#### 　　第 21 步：给硬盘分区，如下界面，我们点击 创建

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019225729037-1268937359.png)**

　　为了便于后面的操作，我们这里选择手动分区，顺便给大家普及一下Linux分区的知识：

　　Linux 系统分区：

　　　　必须分区：

　　　　　　①、根分区  /

　　　　　　②、交换分区 swap   (可以理解为虚拟内存，当内存不够时，可以临时使用 swap 分区，内存的两倍，不超过 2GB)

　　　　推荐分区：

　　　　　　③、启动分区 boot 　（保存系统启动时的数据，一般不用太大，200 M足够，防止根分区写满文件之后，系统起不来）

 　  　　　　④、home 分区 ，保存用户的信息

　　**我们在上一步之后选择标准分区，点击创建**

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019225940193-49632121.png)**

　　第一步：创建 boot 分区，大小为 200 m

　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019225955256-651481510.png)

　　第二步：给 swap 分区，大小为 2000 M

　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019230008396-173665244.png)

　　第三步：给 home 分区，大小为 5000 M

　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019230021443-472215511.png)

　　第四步：给 根目录 分区，大小为剩余所用空间

　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019230035974-1562635864.png)

　　那么我们分区完成，点击 下一步：

　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019230050943-1636819744.png)

#### 　　第 22 步：格式化硬盘，选择格式化

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019230358271-1522626700.png)**

#### 　　第 23 步：选择将修改写入磁盘，点击下一步

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019230414756-184781631.png)**

#### 　　第 24步：默认，点击下一步

　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019230428896-1641416187.png)

#### 　　第 25 步：选择安装类型

**　　初学者如果想要图形化界面可以选择 前面两个，但是基本上后面的操作建议都用命令行的形式来学习更好，这里我们建议选择 Basic Server （纯字符界面）点击下一步，然后等待安装完成**

　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019230635193-1177938447.png)

#### 　　第 26 步：安装完成后，我们选择重新引导即可，输入用户名密码登录我们所安装的 Linux 系统

**　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019230800287-606904607.png)**

#### 　　第 27 步：输入用户名、密码登录 Linux 系统

 　　![](https://images2017.cnblogs.com/blog/1120165/201710/1120165-20171019230818677-912043487.png)

[回到顶部](https://www.cnblogs.com/ysocean/p/7689146.html#_labelTop)

### 3、总结

　　整个虚拟机的安装图示和步骤我们都给出来了，由于每一步都有图示所以可能篇幅比较长，但是相信大家跟着图示一步一步操作，肯定是没有任何问题的。那么经过这一篇博客，我们Linux系统也已经安装完成了，下一篇博客我们就开始正式进入Linux的命令学习。