# 眼不见为净——谈谈我的 Android 文件管理方案

## 前言

一直以来，Android 的权限控制相比 iOS 都要更加开放，用户可以随意的在内部存储器中读写文件，同样的，应用也可以四处创建文件夹。时间一久，当我们再次查看内部存储时，已经被应用流氓们搞得混乱不堪，找起文件来愈发困难。

## 提要

为彻底改变内部存储空间「脏、乱、差」的局面，保护用户隐私，Google 在 Android Q 中引入[分区存储](https://android-developers.googleblog.com/2019/04/android-q-scoped-storage-best-practices.html)特性，为每个应用建立独立的存储沙箱，将文件数据隔离。然而或许是考虑到沙箱机制可能会对大部分不守规矩的应用造成不小的冲击，甚至导致无法正常读取文件，Google 暂缓了该计划以留给开发者时间来做适配工作。所以在正式版本到来之前，不妨让我们先来谈一谈 Android 文件管理方案。

![分区存储](https://ws1.sinaimg.cn/large/006tNc79ly1g2uuyht7r2j318g0d8my1.jpg)

关联阅读：

- [Android Q 存储行为大变化，对用户和应用的影响都有哪些](https://sspai.com/post/53287)

- [让你的 Android 内部存储空间整洁如新：存储重定向上手指南](https://sspai.com/post/54420)

## 介绍

一个优秀的工具可以让日后的使用更加轻松，Android 从来都不缺文件管理器——RE、ES、FC、MT、TC……相信不少 Android 用户肯定眼熟这几个名字。

![Google Play 上的文件管理器](https://ws3.sinaimg.cn/large/006tNc79ly1g2uuygfbzaj313l0u0tei.jpg)

Solid Explorer 作为 Android 老牌文件管理器，仅靠其出众的颜值，便俘获相当多的用户。接下来要介绍的几个实用功能，更是让它成为装机必备的热门应用。

![丰富的主题与配色方案](https://ws4.sinaimg.cn/large/006tNc79ly1g2uuyqrbptj31en0u0n1a.jpg)

### 🗃隐藏文件夹

与其说是「隐藏」，实质上是将不常用的文件夹「收纳」到 Solid Explorer 侧边栏的一隅，对文件夹本身没有做任何的权限修改，虽说是一种「掩耳盗铃」的手段，但效果立竿见影，当你下次再打开 Solid Explorer，便不会迷失于杂乱无章的文件夹中。

### 🔖侧边栏书签

隐藏文件夹的方法是从「减法」的角度出发，而对于目录较深的常用子文件夹，例如 QQ、微信的接收文件，我们可以采用添加「书签」的方式，这一点类似访达中的「个人收藏」。欢迎各位读者在评论区留下常用应用的下载文件夹，比如 Telegram X 接受文件的缓存路径为`/storage/emulated/0/Android/data/org.thunderdog.challegram/files/documents`。

![显眼的书签与角落的隐藏文件夹](https://ws2.sinaimg.cn/large/006tNc79ly1g2uuzwxm96j30xr0u04do.jpg)

### 🏷左右双面板

类似于访达上的「标签页」，Solid Explorer 允许用户在两个面板之前快速切换，横屏后可以使用拖拽手势，操作直观便捷。

![横屏同时展示双面板](https://ws3.sinaimg.cn/large/006tNc79ly1g2uv2a6s72j31hc0u0wkh.jpg)

### ☁️云服务管理

不仅提供本地文件管理功能，Solid Explorer 同样支持网盘及远程服务器。以添加 macOS 远程文件共享为例，Mac 端配置完成后，在 Solid Explorer 中新建云连接，连接类型选择 LAN/SMB，按照提示填写即可，注意路径处不要留空，可填 Macintosh HD，留空不认的🙅～

![macOS 开启文件共享](https://ws1.sinaimg.cn/large/006tNc79ly1g2uv3cjfbkj310x0u0go6.jpg)

使用 Handshaker 无线传输文件到 Android，每次都要在两边打开应用然后配对连接。这时不妨反向操作，在 Solid Explorer 上远程访问 Mac，而不必看到下面这片景象👇

![杂乱无章的 Android 内部存储与秩序井然的访达](https://ws2.sinaimg.cn/large/006tNc79ly1g2uvvodpglj31lg0u0kjl.jpg)

### 📀媒体浏览器

Solid Explorer 提供多种视图选项：列表、网格、画廊、紧凑，以及多种排序方式：名称、日期、大小、类型，并且可选仅应用于某一文件夹。另外在属性里可以快速查看文件类型、大小分布

![紧凑与画廊视图](https://ws4.sinaimg.cn/large/006tNc79ly1g2uv8wf8i2j30xr0u0qap.jpg)

### 🗜️压缩包预览

作为文件管理器标配功能，Solid Explorer 同样支持基本的压缩文件预览及解压，不过会有一定的几率出现乱码😅。

![查看压缩包内文件](https://ws3.sinaimg.cn/large/006tNc79ly1g2uuyfwgomj30xr0u0dme.jpg)
