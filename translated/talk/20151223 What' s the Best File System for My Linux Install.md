
我的Linux系统应该安装的最好的文件系统是什么？
================================================================================
![](https://www.maketecheasier.com/assets/uploads/2015/05/file-systems-feature-image.jpg)

文件系统: 它们不是世界上最激动人心的技术，但是仍然很重要。本文我们将细数那些流行的Linux文件系统 - 它们是什么，它们能够做什么，以及它们的目标用户。

### Ext4 ###

![file-systems-ext4](https://www.maketecheasier.com/assets/uploads/2015/05/file-systems-ext4.png)

如果你曾经安装过Linux，你可能在安装过程中看到过"Ext4"字样。关于这个有一个不错的理由: 它是当前每个可用Linux发行版所选择的文件系统。当然，还有其他的一些选择，但是不可否认的是，Ext4(Extended 4)几乎是所有Linux用户都会选择的文件系统。

#### 它能做什么？ ####

Ext4拥有你预期的曾经的文件系统(Ext2/Ext3)的所有优点， 同时还带来了一些改进。还有很多内容可以发掘，这里列举出Ext4为你带来的最好的部分:

- 文件系统日志
- 日志校验
- 多重块文件的分配
- 对Ext2 && Ext3向后兼容
- 持续的预分配空闲空间
- 改进的文件系统校验(相比于之前的版本)
- 当然，同时支持更大的文件

#### 目标用户 ####

Ext4针对那些寻找超级可靠的构建环境或者那些仅仅需要可用环境的用户。这个文件系统不会对你的系统做快照；它甚至没有最好的SSD支持，但是如果你的要求不是太过严格的话，你会觉得它也还不错。

### BtrFS ###

![file-systems-btrFS](https://www.maketecheasier.com/assets/uploads/2015/05/file-systems-btrFS-e1450065697580.png)

B树(B-tree)文件系统 (也被认为是butterFS，黄油文件系统) 是Oracle为Linux研发的一款文件系统。它是一个全新的文件系统，而且正处于重度开发阶段。Linux社区认为其目前使用上还有些不稳定。BtrFS的核心原则是基于写时复制(copy-on-write). **写时复制**基本上意味着在写入数据前，这份数据的每一比特都有单独的一份副本。当数据写入完毕后，它相应的副本也随之生成。

#### 它能做什么 ####

除了支持写时复制之外，BtrFS也能够胜任许多其他的事务 - 事实上，如此多的事务支持以致于它能永久列出一切(数据)。这里列举最值得一提的特性：支持只读快照，文件克隆，子卷，透明压缩，离线文件系统校验，无缝地从ext3&&4转换到BtrFS，在线碎片整理，还支持RAID 0, RAID 1, RAID 5, RAID 6 and RAID 10。

#### 目标用户 ####

BtrFS的开发者门许诺过，该文件系统是当前其他文件系统的新一代替代者。非常正确，虽然目前其处于开发中。它有很多杀手级的特性面向高级用户，也包括基本用户 (包括SSDs上面的表现)。这个文件系统针对那些想要从文件系统中获取更多(特性)，以及那些想尝试用写时复制机制做一些事情的用户。

### XFS ###

![file-systems-xfs](https://www.maketecheasier.com/assets/uploads/2015/05/file-systems-xfs.jpg)

由Silicon Graphics公司创造开发，XFS是一个高端文件系统，定位于速度和性能。对于性能方面的专注，使得在并行输入输出方面，XFS表现的尤其出色。XFS文件系统能够处理数量庞大的数据，事实上某些XFS用户的数据接近300+TB。

#### 它能做什么 ####

XFS是一个经历良好测试的数据存储文件系统，它是为了高性能操作而诞生的。其特性包括：

- RAID阵列的条纹(striped)模式分配
- 文件系统日志
- 多种块大小
- 直接I/O
- 指定速率(guaranteed-rate)I/O
- 快照
- 在线碎片整理
- 在线调整大小

#### 目标用户 ####

XFS针对那些想要一个坚如磐石的文件系统方案的用户。它起源于1993年，并且随着时间的变迁它变得越来越好。如果你有一台家庭服务器，而且你苦恼于如何部署存储环境，那么可以考虑下XFS。它拥有的众多特性(比如快照)能够协助你的文件存储系统。尽管如此，它不局限于服务器端。如果你是一个相对高级一点的用户或者你对BtrFS所承诺的很多特性感兴趣的话，尝试一下XFS。它实现了很多与BtrFS相似的特性，并且没有稳定性方面的问题。

### Reiser4 ###

![file-system-riser4](https://www.maketecheasier.com/assets/uploads/2015/05/file-system-riser4.gif)

Reiser4，ReiserFS的继任者，由Namesys公司创造研发。它的诞生追溯到Linspire工程和DARPA。它与众不同的地方在于众多的事务模式。没有一个单一的方式来写入数据；取而代之的是，有很多方式(来写入)。

#### 它能做什么 ####

Reiser4拥有着使用多种不同事务模式的独特能力。它能够使用写时复制模式 (像BtrFS)，任意位置写入(write-anywhere)，日志，以及超级事务模式。它在ReiserFS的基础上做了许多的改进，包括更好的基于漫游日志的文件系统日志，对更小的文件较好的支持，以及更快速的目录处理。Reiser4提供了许多功能特性。还有更多的特性可以探讨，不过简单来讲，相比于ReiserFS它对众多新增特性做了非常大的改进。

#### 目标用户 ####

Resier4适合那些想要将一个文件系统应用到多中场景下的用户。可能你想在一台机器上使用copy-on-write机制，在另一台机器上使用write-anywhere机制，还会在另一台机器上使用超级事务，而你又不希望使用多种不同类型的文件系统来完成这项任务。Reiser4是适合这种情况的完美方案。

### 结论 ###

Linux上有许多可用的文件系统。每个文件系统都有其特定的用途，以便于特定用户解决不同的问题。本文的焦点集中在平台上文件系统的主流的选择。毫无疑问，其它的场景下还有一些别的选择。

你在Linux上最喜欢的文件系统是什么？在下面(的评论区)告诉我们吧！
--------------------------------------------------------------------------------

via: https://www.maketecheasier.com/best-file-system-linux/

作者：[Derrik Diener][a]
译者：[icecoobe](https://github.com/icecoobe)
校对：[校对者ID](https://github.com/校对者ID)

本文由 [LCTT](https://github.com/LCTT/TranslateProject) 原创编译，[Linux中国](https://linux.cn/) 荣誉推出

[a]:https://www.maketecheasier.com/author/derrikdiener/
