# Linux 学习笔记

## Linux 简介

`Linux` 内核最初只是由芬兰人**林纳斯·托瓦兹（Linus Torvalds）**在赫尔辛基大学上学时出于个人爱好而编写的。

`Linux` 是一套免费使用和自由传播的类 `Unix` 操作系统，是一个基于 POSIX 和 UNIX 的多用户、多任务、支持多线程和多 CPU 的操作系统。

`Linux` 能运行主要的 `UNIX` 工具软件、应用程序和网络协议。它支持 32 位和 64 位硬件。`Linux` 继承了 `Unix` 以网络为核心的设计思想，是一个性能稳定的多用户网络操作系统。

### Linux 的发行版

`Linux` 的发行版说简单点就是将 `Linux` 内核与应用软件做一个打包。

![img](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/1511849829609658.jpg)

------

目前市面上较知名的发行版有：`Ubuntu`、`RedHat`、`CentOS`、`Debian`、`Fedora`、`SuSE`、`OpenSUSE`、`Arch Linux`、`SolusOS` 等。

![img](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/wKioL1bvVPWAu7hqAAEyirVUn3c446.jpg-wh_651x-s_3197843091.jpg)

### Linux 应用领域

今天各种场合都有使用各种 `Linux` 发行版，从嵌入式设备到超级计算机，并且在服务器领域确定了地位，通常服务器使用 `LAMP`（Linux + Apache + MySQL + PHP）或 `LNMP`（Linux + Nginx+ MySQL + PHP）组合。

目前 `Linux` 不仅在家庭与企业中使用，并且在政府中也很受欢迎。

- 巴西联邦政府由于支持 `Linux` 而世界闻名。
- 有新闻报道俄罗斯军队自己制造的 `Linux` 发布版的，做为 G.H.ost 项目已经取得成果。
- 印度的 Kerala 联邦计划在向全联邦的高中推广使用 `Linux`。
- 中华人民共和国为取得技术独立，在龙芯处理器中排他性地使用 `Linux`。
- 在西班牙的一些地区开发了自己的 Linux 发布版，并且在政府与教育领域广泛使用，如 Extremadura 地区的 gnuLinEx 和 Andalusia 地区的 Guadalinex。
- 葡萄牙同样使用自己的 `Linux` 发布版 Caixa Mágica，用于 Magalh?es 笔记本电脑和 e-escola 政府软件。
- 法国和德国同样开始逐步采用 `Linux`。

### Linux vs Windows

目前国内 Linux 更多的是应用于服务器上，而桌面操作系统更多使用的是 Windows。主要区别如下：

<table class="reference">
<tbody><tr>
<th>比较</th>
<th>Windows</th>
<th>Linux</th>
</tr>
<tr>
<td>界面</td>
<td>界面统一，外壳程序固定所有 Windows 程序菜单几乎一致，快捷键也几乎相同</td>
<td>图形界面风格依发布版不同而不同，可能互不兼容。GNU/Linux 的终端机是从 UNIX 传承下来，基本命令和操作方法也几乎一致。</td>
</tr>
<tr>
<td>驱动程序</td>
<td>驱动程序丰富，版本更新频繁。默认安装程序里面一般包含有该版本发布时流行的硬件驱动程序，之后所出的新硬件驱动依赖于硬件厂商提供。对于一些老硬件，如果没有了原配的驱动有时很难支持。另外，有时硬件厂商未提供所需版本的 Windows 下的驱动，也会比较头痛。</td>
<td>由志愿者开发，由 Linux 核心开发小组发布，很多硬件厂商基于版权考虑并未提供驱动程序，尽管多数无需手动安装，但是涉及安装则相对复杂，使得新用户面对驱动程序问题（是否存在和安装方法）会一筹莫展。但是在开源开发模式下，许多老硬件尽管在Windows下很难支持的也容易找到驱动。HP、Intel、AMD 等硬件厂商逐步不同程度支持开源驱动，问题正在得到缓解。</td>
</tr>
<tr>
<td>使用</td>
<td>使用比较简单，容易入门。图形化界面对没有计算机背景知识的用户使用十分有利。</td>
<td>图形界面使用简单，容易入门。文字界面，需要学习才能掌握。</td>
</tr>
<tr>
<td>学习</td>
<td>系统构造复杂、变化频繁，且知识、技能淘汰快，深入学习困难。</td>
<td>系统构造简单、稳定，且知识、技能传承性好，深入学习相对容易。</td>
</tr>
<tr>
<td>软件</td>
<td>每一种特定功能可能都需要商业软件的支持，需要购买相应的授权。</td>
<td>大部分软件都可以自由获取，同样功能的软件选择较少。</td>
</tr>
</tbody></table>

## Linux 安装

这里使用 `VMware Workstation Pro` 工具安装 `Linux` 虚拟机。

首先前往[CentOS官网](https://www.centos.org/download/)或者[阿里云开源镜像站](http://mirrors.aliyun.com/centos/7.9.2009/isos/x86_64/)下载 `CentOS 7` （官方不在维护 `CentOS 8`，也不会有 `CentOS 9`，最好选择安装 `CentOS 7`），下面演示如何下载。

如果选择到阿里云开源镜像站下载，会进入如下页面：

![image-20220715000851672](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/image-20220715000851672.png)

一般来说，选择大小为 4.4GB 的那个文件下载即可。

下载好了之后开始安装。

点击左上角`文件`，然后点击`新建虚拟机`，会看到如下界面：

![image-20220717111905967](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/image-20220717111905967.png)

选择`典型`即可，点击下一步：

![image-20220717112007689](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/image-20220717112007689.png)

选择**稍后安装操作系统**，点击下一步：

![image-20220717112055178](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/image-20220717112055178.png)

客户机操作系统选择 `Linux`，版本选择 `Red Hat Enterprise Linux 7 64位`，点击下一步：

![image-20220717112215545](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/image-20220717112215545.png)

这里可以给虚拟机起个名字，并选择虚拟机文件存储位置，建议放在 C 盘以外的地方，点击下一步：

![image-20220717112349359](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/image-20220717112349359.png)

磁盘大小 20GB 即可，选择**将虚拟磁盘拆分多个文件**，点击下一步：

![image-20220717112515317](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/image-20220717112515317.png)

点击完成。然后在刚刚创建的虚拟机上右击，点击设置，会看到如下界面：

![image-20220717112625973](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20220717112625973.png)

点击 **CD/DVD**，然后点击**使用 ISO 映像文件**，点击浏览，选择刚刚下载好的映像文件，点击确定即可。

![image-20220717112655893](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/image-20220717112655893.png)

到了这里，就可以开机了。点击开启此虚拟机，然后等待：

![image-20220717112945352](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/image-20220717112945352.png)

光标选择第一个（Install CentOS 7），等待，会进入如下界面：

![image-20220717113151646](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/image-20220717113151646.png)

选择中文，点击<kbd>继续</kbd>：

![image-20220717113301654](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/image-20220717113301654.png)

点击**软件选择**，会看到如下界面，视情况选择**最小安装**或者**GNOME桌面**，对于初学者来说选择**GNOME桌面**好一点。然后点击完成。

![image-20220717113406705](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/image-20220717113406705.png)

点击完成之后需要一定时间的加载，请耐心等待，不要乱动。然后点击**安装位置**

![image-20220717113704339](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/image-20220717113704339.png)

会看到如下界面：

![image-20220717113852468](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/image-20220717113852468.png)

选择我要配置分区，然后点击完成，会进入如下界面：

![image-20220717113931254](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/image-20220717113931254.png)

点击 `+` 号，选择挂载点为 `/boot` 期望容量为 1G，然后点击添加挂载点

![image-20220717114053793](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/8919/image-20220717114053793.png)

## VM（VIM）和 Linux 目录结构

## 远程登录

## 开机、重启和用户登陆注销

## 用户管理

## 实用指令

## 组管理和权限管理

## 定时任务调度

## Linux 磁盘分区、挂载

## 网络配置

## 进程管理

## RPM 与 YUM

## 搭建 JavaEE 环境

## Shell 编程

## 日志管理