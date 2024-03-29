---
layout: post
title: "53期 - 备份策略 - 第1部分"
date: 2012-04-26 20:14
comments: true
categories: issue53 HOW-TO backup-strategy
---

`作者: Allan J.Smithie 翻译: 杨佳 校对: 吴云 顾履冰`

对极客而言，没有什么比丢失数据更坏的事情了，特别是如果他碰巧有积攒了多年的东西。我们身边的一切都冷酷地变得数字化，音乐、照片集、通信；虽然使用起来很方便，但是很容易丢失。

硬盘出错常常让人们觉得很郁闷；跌落、电涌、病毒或者操作失误都会导致数据丢失。这时候我们就需要一个安全网络，一份备份的策略。噢，瞧，我刚好就有一个......

### 什么东西需要备份

不用担心软件。程序的丢失最多只会带来不便，因为程序可以很容易地被替换掉，尤其是开源程序；你也不必为了找许可证或激活码（ License/Activation Keys ）而浪费时间。

<!--more-->

但是如果丢失的是数据就真的悲剧了，因为数据才是真正的无价之宝啊。

### 那么要备份什么样的数据文件呢？

照片、文档、电子表格、日历和电子邮件（邮箱或者个人信息）。如果你和我一样，收藏着从1/4英寸磁带中转录出来的音乐库，那么音乐文件也是宝贝啦。

首先，你得知道这些数据存放在什么地方。这就需要一个详细的存储明细表，能够以文件类型（扩展名）在系统中进行搜索。别以为你亲爱的人也会将文件保存在你希望的位置。进行搜索，看各个地方放的都是些什么东西。然后你进行内务处理并归置好它们。对内容进行合理说明并去掉重复的。你需要知道什么是重要的，什么是最新的。然后清空回收站。记得在明细表中将U盘和外置硬盘也包含进来。

你肯定不想备份系统缓存或临时文件、交换文件或者页面文件，因为你几乎提取不出什么有用东西，而且里面基本上都是垃圾。如果缓存中有你需要的东西，拷贝出来放到一个更安全的地方。

你需要知道一些文件的类型（通常用文件扩展名表示，比如.odt, .pdf, .mpeg, .mp3, .mp4）以便更好对备份进行分类。

数据库（.dbf， .db）一般都有另外的方法来备份上锁或者已经打开的文件、记录和索引。想想你那些重要的俱乐部信息、邮件列表，视频索引；如果备份的时候文件处于锁定（或者编辑）状态，你将会无功而返。备份数据的时候最好将正在使用它的程序关掉。

### 备份的文件和数据在什么地方？

本地（内置）磁盘是数据所在的第一个地方，紧接着是外置硬盘，网络（服务器）驱动器、NAS、SAN以及点对点连接的机器。U盘用于存放最新的“sneaker-net”（译注：sneaker-net是一种人为地用物理移动介质如U盘将文件从一台电脑拷贝到另一台上的方式）拷贝文档是非常合适的，外置USB硬盘和火线硬盘也是不错的选择。我将“暂存数据（temporary）”和中间的数据拷贝文件都复制到了其他的一些设备上（译注:即在几个不同的地方存放同一个文件的几份拷贝）。放在手机和PDA（译注：掌上电脑Pesonal Digital Assistant）、iPhone、iPad上或者同步到Blackberry？为你需要备份的不同种类数据和文件做一个清单。

### 版本控制

你的数据是否具有易失性？高优先级或者很重要的信息可能会经常变化。难道你打算对每个版本都进行备份吗？可能因为审计和检查，公司及政府的数据保留政策，或者只为记录平时的工作过程，你会需要几份不同时期的备份，以便在发生错误时能恢复到之前的版本。那么你应该对保留的份数进行规划以达到空间的最大利用率，因此也就需要考虑备份的频率和保留时间。IT管理中对备份、版本控制和保留策略都有详细的说明，感兴趣的话可以找相关资料看看。

### 备份目的地

最安全的存储计划看起来应该像下面这样： •本机磁盘（原始或主备份） •网络存储磁盘（一般或共享备份） 注意在网络计算广泛应用的今天，这种方式很有可能是你的主要备份方案。即使你用了可靠性更高的RAID（冗余磁盘阵列，Redundant Array of Inexpensive Disk），也不要对其完全信任。数据仍然是以电子位元形式存储于磁盘上的。 •离线存储（offline storage）。一般是磁带，但根据需要也可以是任何东西——磁带，磁盘托，微型磁盘，可写磁盘，或者是挂载的逻辑卷。 •远程存储（off-site storage）。可以是物理介质——几块磁盘组成的镜像，数字磁带或者数据DVD。 •远程云存储（Remote cloud storage），也叫做在线备份（on-line backup）。

要避免丢失数据的危险，你应该保证至少在三个不同地方都有备份：本地、远程和云端。
本地备份不包括你正在使用的那份拷贝。为了方便你可以使用一个外置硬盘。将硬盘放在一个安全的地方，远离电脑。仔细考虑并规划本地备份。

最好将备份放到防火的地方。

远程的意思是不要放在家里或者办公室这些有电脑的地方。如果没别的事情，就交替使用两块外置硬盘，并将其中一块放在你母亲的房间里。你可以和最佳拍档使用刚好相反的安排。我听说有些专业人士甚至在用银行的保管箱。

上面的方法只能提供数据的物理持久性，但是请考虑一下隐私和是否需要对数据进行加密保护。如果你的远程备份被偷走了，这些数据落入他人之手会不会对你造成什么伤害？比如说家人的照片？律师朋友的法律文书？想想就后怕了吧，这就是为什么他要对备份进行加密。这已经能构成另外一个完整的话题了。

### 在生活中习惯备份

这个说法的意思是需要一个管理器或者脚本来触发备份程序将你的数据拷贝到与主备份不同的地方。

### 将外部备份移至远方

如果备份可以免遭火灾、洪水、盗窃、地震和自然损耗等意外，它的有效性就有保证了。一旦备份完成，切记将存储设备移至其他地点。不要放在书架上、冰箱上或桌子下面。那不算是有效的备份。这就是在线或者云存储吸引人的原因了。

在线备份和存储目前对大部分电脑用户来说是很有实用价值的，并且现在也有很多家服务商提供这种服务。由于磁盘空间的廉价性，在带宽允许的条件下它就能自动将你的数据备份到云端。最好的云存储服务甚至还有加密功能。

### 测试

最后：从所有资源中恢复一部分来进行备份恢复测试。原因很简单，有备份并不能代表它就是可用的。磁带和DVD的自然损耗，磁盘错误，软件也不是每次都能保证写的完整性。为了以防万一还是测试一下的好。

因为庞大的数据量和恢复所消耗的时间，数据恢复一直都是一件极具挑战的任务。而且程序还要检查备份数据的完整性。如果你从来没有做过完整的恢复，那么就需要建立起同事们所谓的“可信度（degree of confidence）”。进行部分的数据恢复可以在紧急关头给你信心，否则到时候你就只能猜测了。在生活的其他方面要是靠猜的话，说实话，你的信心有多少？