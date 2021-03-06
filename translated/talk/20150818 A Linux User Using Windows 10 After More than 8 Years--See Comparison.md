对比Windows 10与Linux:Linux用户已经使用'Windows 10'超过8年
==============================================================================================================================================================
Windows 10 是2015年7月29日上市的最新一代Windows NT系列系统,Windows 8.1 的继任者.Windows 10 支持Intel 32位平台,AMD64以及ARM v7处理器.

![Windows 10 and Linux Comparison](http://www.tecmint.com/wp-content/uploads/2015/08/Windows-10-vs-Linux.jpg)

对比:Windows 10与Linux

作为一个连续使用linux超过8年的用户,我想要去测试Windows 10 ,因为它最近制造了很多新闻.这篇文章是我观察力的一个重大突破.我将从一个linux用户的角度去看待一切,所以这篇文章可能会有些偏向于linux.尽管如此,本文也应该不会有任何错误信息.

1. 用谷歌搜索"download Windows 10" 并且点击第一个链接.

![Search Windows 10](http://www.tecmint.com/wp-content/uploads/2015/08/Search-Windows-10.jpg)

搜索Windows 10

你也可以直接打开: [https://www.microsoft.com/en_us/software-download/Windows10[1]

2. 微软要求我从Windows 10, Windows 10 KN, Windows 10 N 和Windows 10 单语言版中选择一个版本

![Select Windows 10 Edition](http://www.tecmint.com/wp-content/uploads/2015/08/Select-Windows-10-Edition.jpg)

选择版本

以下是各个版本的简略信息:

- Windows 10 - 包含微软提供给我们的所有软件
- Windows 10N - 此版本不包含媒体播放器
- Windows 10KN - 此版本没有媒体播放能力
- Windows 10单语言版 - 仅预装一种语言

3. 我选择了第一个选项 " Windows 10"并且单击"确认".之后我要选择语言,我选择了"英语"

微软给我提供了两个下载链接.一个是32位版,另一个是64位版.我单击了64位版--这与我的电脑架构相同. 

![Download Windows 10](http://www.tecmint.com/wp-content/uploads/2015/08/Download-Windows-10.jpg)

下载Windows 10

我的带宽是15M的,下载了整整3个小时.不幸的是微软没有提供系统的种子文件,否则整个过程会更加舒畅.镜像大小为 3.8 GB(译者注:就我的10M小水管,我使用迅雷下载用时50分钟).

我找不到更小的镜像,微软并没有为Windows提供网络安装镜像.我也没有办法在下载完成后去校验哈希值.

我十分惊讶,Windows在这样的问题上居然如此漫不经心.为了验证这个镜像是否正确下载,我需要把它刻到光盘上或者复制到我的U盘上然后启动它,一直静静的看着它安装直到安装完成.

首先,我用dd命令将win10的iso镜像刻录到U盘上

    # dd if=/home/avi/Downloads/Win10_English_x64.iso of=/dev/sdb1 bs=512M; sync

这需要一点时间.在此之后我重启系统并在UEFI(BIOS)设置中选择从我的U盘启动.

#### 系统要求 ####

升级

- 仅支持从Windows 7 SP1或者Windows 8.1升级

重新安装

- 处理器: 1GHz 以上
- 内存: 1GB以上(32位),2GB以上(64位)
- 硬盘: 16GB以上(32位),20GB以上(64位)
- 显卡: 支持DirectX 9或更新  + WDDM 1.0 驱动

###Windows 10 安装过程###

1. Windows 10启动成功了.他们又换了logo,但是仍然没有信息提示我它正在做什么.

![Windows 10 Logo](http://www.tecmint.com/wp-content/uploads/2015/08/Windows-10-Logo.jpg)

Windows 10 Logo

2. 选择安装语言,时区,键盘,输入法,点击下一步

![Select Language and Time](http://www.tecmint.com/wp-content/uploads/2015/08/Select-Language-and-Time.jpg)

选择语言和时区

3. 点击'现在安装'

![Install Windows 10](http://www.tecmint.com/wp-content/uploads/2015/08/Install-Windows-10.jpg)

安装Ｗindows 10

4. 下一步是输入密钥,我点击了跳过

![Windows 10 Product Key](http://www.tecmint.com/wp-content/uploads/2015/08/Windows-10-Product-Key.jpg)

Windows 10 产品密钥

5. 从列表中选择一个系统版本.我选择了Windows 10专业版

![Select Install Operating System](http://www.tecmint.com/wp-content/uploads/2015/08/Select-Install-Operating-System.jpg)

选择系统版本

6. 到了协议部分,选中"我接受"然后点击下一步

![Accept License](http://www.tecmint.com/wp-content/uploads/2015/08/Accept-License.jpg)

同意协议

7. 下一步是选择(从Windows的老版本)升级到Windows 10或者安装Ｗindows.我搞不懂为什么微软要让我自己选择:"安装Ｗindows"被微软建议为"高级"选项.但是我还是选择了"安装Windows".

![Select Installation Type](http://www.tecmint.com/wp-content/uploads/2015/08/Select-Installation-Type.jpg)

选择安装类型

8. 选择驱动器,点击"下一步"

![Select Install Drive](http://www.tecmint.com/wp-content/uploads/2015/08/Select-Install-Drive.jpg)

选择安装盘

9. 安装程序开始复制文件,准备文件,安装更新,之后进行收尾.（如果安装程序能在安装时输出一堆字符来表示他在做什么就更好了）

![Installing Windows](http://www.tecmint.com/wp-content/uploads/2015/08/Installing-Windows.jpg)

安装 Windows

10. 在此之后Windows重启了.他们说为了继续,我们需要重启

![Windows Installation Process](http://www.tecmint.com/wp-content/uploads/2015/08/Windows-Installation-Process.jpg)

安装进程

11. 我看到了一个写着"正在准备Windows"的界面.它停了整整五分多钟,仍然没有说明它正在做什么.没有输出.

![Windows Getting Ready](http://www.tecmint.com/wp-content/uploads/2015/08/Windows-Getting-Ready.jpg)

正在准备Windows

12. 又到了输入产品密钥的时间.我点击了"以后再说",并使用快速设置

![Enter Product Key](http://www.tecmint.com/wp-content/uploads/2015/08/Enter-Product-Key.jpg)

输入产品密钥

![Select Express Settings](http://www.tecmint.com/wp-content/uploads/2015/08/Select-Express-Settings.jpg)

使用快速设置


13. 又出现了三个界面,作为Linux用户我认为此处应有信息来告诉我安装程序在做什么,但是我想多了
![Loading Windows](http://www.tecmint.com/wp-content/uploads/2015/08/Loading-Windows.jpg)

载入 Windows

![Getting Updates](http://www.tecmint.com/wp-content/uploads/2015/08/Getting-Updates.jpg)

获取更新

![Still Loading Windows](http://www.tecmint.com/wp-content/uploads/2015/08/Still-Loading-Windows.jpg)

还是载入 Ｗindows

14. 安装程序想要知道谁拥有这台机器,"我的组织"或者我自己

![Select Organization](http://www.tecmint.com/wp-content/uploads/2015/08/Select-Organization.jpg)

选择组织

15. 安装程序提示我加入"Aruze Ad"或者"加入域".在单击继续之前,我选择了后者.

![Connect Windows](http://www.tecmint.com/wp-content/uploads/2015/08/Connect-Windows.jpg)

连接网络

16. 安装程序让我新建一个账户.所以我输入了 "user_name"并点击下一步,我觉得我会收到一个要求我必须输入密码的信息.

![Create Account](http://www.tecmint.com/wp-content/uploads/2015/08/Create-Account.jpg)

新建账户

17. 让我惊讶的是Windows甚至都没有警告/发现我必须创建密码.真粗心.不管怎样,现在我可以体验系统了.

![Windows 10 Desktop](http://www.tecmint.com/wp-content/uploads/2015/08/Windows-10-Desktop.jpg)

Windows 10的桌面环境

#### Linux用户(我)直到现在的体验 ####

- 没有网络安装镜像
- 镜像文件太臃肿了
- 没有验证iso是否为正确的方法(官方没有提供哈希值)
- 启动与安装方式仍然与XP,Win 7,Win 8相同(可能吧...)
- 和以前一样,安装程序没有输出他正在干什么 - 正在复制什么和正在安装什么软件包
- 安装程序比Linux发行版的更加直白和简单

####测试 Windows####

18. 默认桌面很干净,上面只有一个回收站图标.我们可以直接从桌面搜索网络.底部的快捷方式分别是任务预览,网络,微软应用商店.和以前的版本一样,消息栏在右下角.

![ ](http://www.tecmint.com/wp-content/uploads/2015/08/Deskop-Shortcut-icons.jpg)

桌面图标

19. IE浏览器被换成了Edge浏览器.微软把他们的老IE换成了Edge(斯巴达计划)

![Microsoft Edge Browser](http://www.tecmint.com/wp-content/uploads/2015/08/Edge-browser.jpg)

Edge浏览器

这个浏览器至少比IE要快.他们有相同的用户界面.它的主页包含新的更新.它还有一个标题是"下一步怎么走".由于它全面的性能提升,它的加载速度非常快.Edge的内存占用看起来一般般.

![Windows Performance](http://www.tecmint.com/wp-content/uploads/2015/08/Windows-Performance.jpg)

性能

Edge也有小娜加成 -- 智能个人助理.支持笔记(在浏览网页时记笔记),分享(在本TAB分享而不必打开其他TAB)

#### Linux用户(我)此时体验 ####

20. 微软确实提升了网页浏览体验.我们要看的就是他的稳定性和质量.现在它并不落后.

21. 对我来说,Edge的内存占用不算太大.但是有很多用户抱怨他的内存占用.

22. 很难说目前Edge已经准备好了与火狐或Chrome竞争.让我们静观其变.

#### 更多的视觉体验 ####

23. 重新设计的开始菜单 -- 看起来很简洁高效.Merto磁贴大部分都会动.预先放置了最通用的应用.

![Windows Look and Feel](http://www.tecmint.com/wp-content/uploads/2015/08/Windows-Look.jpg)

Windows

在Linux的Gnome桌面环境下.我仅仅需要按下Win键并输入应用名就可以搜索应用.

![Search Within Desktop](http://www.tecmint.com/wp-content/uploads/2015/08/Search-Within-Desktop.jpg)

桌面内进行搜索

24. 文件浏览器 -- 设计的很简洁.左边是进入文件夹的快捷方式.

![Windows File Explorer](http://www.tecmint.com/wp-content/uploads/2015/08/Windows-File-Explorer.jpg)

Windows资源管理器

我们的Gnome下的文件管理也同样的简洁高效.

![File Browser on Gnome](http://www.tecmint.com/wp-content/uploads/2015/08/File-Browser.jpg)

Gnome 的文件管理

25. 设置 -- 尽管Windows 10的设置有点精炼,但是我们还是可以把它与linux的设置进行对比.

**Windows 的设置**

![Windows 10 Settings](http://www.tecmint.com/wp-content/uploads/2015/08/Windows-10-Settings.jpg)

Windows 10 设置

**Linux Gnome 上的设置**

![Gnome Settings](http://www.tecmint.com/wp-content/uploads/2015/08/Gnome-Settings.jpg)

Gnome 的设置

26. 应用列表 -- 目前,Linux上的应用列表比之前的版本要好一些

**Windows 的应用列表**

![Application List on Windows 10](http://www.tecmint.com/wp-content/uploads/2015/08/Application-List-on-Windows-10.jpg)

Windows 10 的应用列表

**Gnome3 的应用列表**

![Gnome Application List on Linux](http://www.tecmint.com/wp-content/uploads/2015/08/Gnome-Application-List-on-Linux.jpg)

Gnome3 的应用列表

27. 虚拟桌面 -- Windows 10 上的虚拟桌面是近来被提及最多的特性之一

这是Windows 10 上的虚拟桌面.

![Windows Virtual Desktop](http://www.tecmint.com/wp-content/uploads/2015/08/Windows-Virtual-Desktop.jpg)

Windows的虚拟桌面

这是我们Linux用户使用了超过20年的虚拟桌面.

![Virtual Desktop on Linux](http://www.tecmint.com/wp-content/uploads/2015/08/Virtual-Desktop-on-Linux.jpg)

Linux的虚拟桌面

#### Windows 10 的其他新特性 ####

28. Windows 10 自带wifi感知.它会把你的wifi密码分享给他人.任何在你wifi范围内并且曾经通过Skype, Outlook, Hotmail 或 Facebook与你联系的人都能够获得你的网络接入权.这个特性的本意是让用户可以省时省力的连接网络.

在微软对于 Tecmint 的问题的回答中,他们说道 -- 用户需要在每次到一个新的网络环境时自己去同意打开wifi感知.如果我们考虑到网络安全这将是很不安全的一件事.微软的说法并没有说服我.

29. 从Windows 7 和 Windows 8.1升级可以省下买新版的花费.(家庭版$119 专业版$199 )

30. 微软发布了第一个累积更新,这个更新在一小部分设备上会让系统一直重启.Windows可能不知道这个问题或者不知道它发生的原因.

31. 微软内建的禁用/隐藏我不想要的更新的功能在我这不起作用.这意味着一旦更新开始推送,你没有方法去禁用/隐藏他们.对不住啦,Windows 用户.

#### Windows 10 包含的来源于Linux的功能 ####

Windows 10有很多直接取自Linux的功能.如果Linux不已GPL发布的话,以下下这些功能永远不会出现在Windows上.

32. 包管理器 -- 是的,你没有听错!Windows 10内建了一个包管理器.它只在Power Shell下工作.OneGet是Windows的官方包管理器.

![Windows 10 Package Manager](http://www.tecmint.com/wp-content/uploads/2015/08/Windows-10-Package-Manager.jpg)
 
 Windows 10的包管理器

- 无国界的Windows
- 扁平化图标
- 虚拟桌面
- 离线/在线搜索一体化
- 手机/桌面系统一体化

### 总体印象###

- 响应速度提升
- 动画很好看
- 资源占用少
- 电池续航提升
- Edge浏览器坚如磐石
- 支持树莓派 2
- Windows 10好的原因是Windows 8/8.1没有达到公众预期并且坏的可以
- 旧瓶装新酒:Windows 10基本上就是以前的那一套换上新的图标

测试后我对Windows 10的评价是:Windows 10 在视觉和感觉上做了一些更新(就如同Windows经常做的那样).我要为斯巴达计划,虚拟桌面,命令行包管理器,整合在线/离线搜索的搜索栏点赞.这确实是一个更新后的产品 ,但是认为Windows 10将是Linux的最后一个棺材钉的人错了.

Linux走在Windows前面.它们的做事方法并不相同.在以后的一段时间里Windows不会站到Linux这一旁.Linux用户也不必去使用Windows 10.

这就是我要说的.希望你喜欢本文.如果你们喜欢本篇文章我会再写一些你们喜欢读的有趣的文章.在下方留下你的有价值的评论.

--------------------------------------------------------------------------------

via: http://www.tecmint.com/a-linux-user-using-Windows-10-after-more-than-8-years-see-comparison/

作者：[vishek Kumar][a]
译者：[name1e5s](https://github.com/name1e5s)
校对：[校对者ID](https://github.com/校对者ID)

本文由 [LCTT](https://github.com/LCTT/TranslateProject) 原创翻译,[Linux中国](https://linux.cn/) 荣誉推出

[a]:http://www.tecmint.com/author/avishek/
[1]:https://www.microsoft.com/en-us/software-download/Windows10ISO
