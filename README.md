# 前言
生物信息学入门指南，写给每一个想要入门生信的学子。 

生物信息学是一个庞杂的学科，利用应用数学、信息学、统计学和计算机科学的方法研究生物学的问题。我喜欢把生物信息学看作一个工具，一个服务于我们研究主题的工具。也因为它的工具属性，生信的内容是繁杂的，多学科的，多用途的。我们并不需要全盘掌握，而应该带有目的性的学习。

我想要尽量写出一份普适的生物信息学入门指南，但是不可避免会带有我所从事的研究领域--微生物生态学的影子。希望学习者能带有目的性的选择和自己研究相关的内容进行学习，如果能有一点帮助，这份指南的存在就是有意义的。

## 为什么写这本书
如今计算机已经渗透在了生物学的研究中，无论你想分析某次实验的数据，或者用代码做出漂亮的图片。计算机在生物学研究中的广泛应用让很多人都萌发了想要学习生物信息学的念头。但是很难有系统的课程去告诉你怎么学习生物信息学，传统课堂的生物信息学分析集中在BLAST等话题上，但这是生物信息学的全部吗？又符合你对生物信息学的期望吗？

也许你也可以从学习某一门编程语言开始，比如学习用python编程。但是现有的很多课程，更多是面对cs的学生开设的，学完这门课程和实际运用到生物学相关的研究中，仍然存在一定的距离，需要我们自己去填补，而初学者常为此感到困惑。

在我大二的时候，朋友向我分享了一个链接[CS自学指南](https://csdiy.wiki/)，这是我系统接触计算机科学的开端。我一边感叹着计算机科学内容的高深，一边不知所措--这份指南的内容太庞杂，全盘学习恐怕是不现实的，如果只选择能够服务于我的科研方向，我又该如何抉择？对于想要学习生物信息学的人，是否也能拥有这样的一份指南？（我强烈推荐大家也认真阅读这份指南，如果这份指南有任何一点内容能帮助到你，我的分享就是有意义的）

现在我是瓦格宁根大学的一名生物信息学硕士；在本科的最后两年，我很幸运的在中科院进行了系统的微生物生态学的学习。我希望能将我这些年的上课/自学经验整理出来，为有兴趣自学生物信息学的人提供一份参考。

## 写给可能正在迷茫的人
如果你刚刚进入大学，还在为学校讲述的内容与自己感兴趣的方向不一致而感到苦恼，欢迎你来到自学的世界。未来研究主题的多样性可能注定没有学校的课程能完全满足你的爱好与好奇，但是互联网为我们提供了无限的可能。但是自学不是一件容易的事情，没有ddl与同伴，自学是一件需要很强目标感和需要享受孤独的事情。希望你能找到属于自己的方式来享受自学，把自学看作自己与自己的游戏，每一份学习到的知识都是从游戏中获得的奖励。

## ChatGPT
在这个时代学习生信是幸运又不幸的，幸运在于chatgpt能帮你解决绝大多数问题，不幸在于你难免会怀疑有了chatgpt我学生信还是有意义的吗。在这里不做过多讨论，需要读者自己寻找答案。需要记住的是，无论什么时候，你有什么问题，都可以向chatgpt进行询问，它永远不会嘲笑你问的问题很“弱智”。但是也要保持警惕，它可能只能给你“答案”，但这个“答案”是否符合我们的预期，是否是我们想要解决问题的最优解，需要我们自己找到答案。

## 怎么使用这本书
我想在这本书中涵盖尽量多的内容：基础性的计算机科学/高等数学/统计学/生物学，应用性的科研作图/多组学分析。但是至少现在还只是一个构想，能写到多深入我不清楚，我的写作速度能否赶上技术的发展速度也未可知。但我会尽力在每一个内容的开始介绍清楚作为一个生信er掌握这项技能对你有什么帮助，让你可以更好地选择性地学习。

## 如果你也想加入到贡献者的行列
一个人的力量终究是有限的，难免有不够完善之处。加之本人是做微生物生态研究出身的，很多内容服务于多组学分析。如果有大佬想在其他领域分享自己的自学经历与资源，可以直接在项目中发起Pull Request，也欢迎和我邮件联系（zhiyi1.zhao@wur.nl）

# Getting start with
想要开始进行生物信息学的学习？但是你了解这个学习旅程中最重要的朋友————计算机么？

在课程开始之前，强烈向大家推荐一个科普向的视频[Crash Course Computer Science](https://www.bilibili.com/video/BV1EW411u7th/)这门课用非常生动的语言配合动画讲解了计算机的组成等话题，能够让你拥有一个非常框架性的对计算机的认知。

做一个不完全恰当的比喻：对计算机专业的人，他们的大学课程类似于一个花瓶，上面的花纹精美，描绘花纹的技法精妙无比，当把每一门课学完，你会觉得，这花纹真是纷繁复杂啊，但是这花纹是画在哪的呢？这系列课告诉你，哦，这花纹是画在一个花瓶上的。而我们感兴趣的话题是生物信息学，我们知道这是一个花瓶就已经足够了，怎么用这个花瓶装花才是我们真正感兴趣的话题。

# 工具
工欲善其事，必先利其器。好用的工具往往能让我们的研究事半功倍
## 英语
在当下，虽然我很不情愿，但也不得不承认，在计算机/生物信息学，很多优质的文档、论坛、网站、课程都是英文居多。

绝大多数生信工具的帮助文档也是英文的——帮助文档常常是最权威、最系统的资料来源。网络上教程、博客、知乎回答、B站视频很多，但容易过时、教程往往省略细节、有的甚至参数解释错误。而帮助文档和官方手册是开发者直接维护的，阅读文档可有效避免“二手知识陷阱”。

养成英文阅读/听课的习惯，无论对于自学这个领域还是未来的科研交流，还是有一定好处的。所以不要害怕英文，其实在日常课程/文档中的英文比文献中的简单多了，没有那么多高级的句式，只用掌握反复出现的专业名词，你会惊喜发现其实你能理解绝大多数内容。
## 文档阅读工具
生物信息学的研究中常常会遇到很多不同格式的文件，一方面是常见的文件格式，比如.xlsx,.docx在信息上往往相当冗余，在储存时不仅包含了你的文字内容，也包含了格式信息，这些信息在生物信息学研究中是不需要的；一方面是统一化的文件格式便于研究的开源与交流。生物信息学中有一个FAIR数据的概念，可发现（Findable）、可访问（Accessible）、可互操作（Interoperable）和可重用（Reusable）

生物信息学常见的格式，比如用于储存核酸或者蛋白质序列的FASTA/FASTQ，用于储存一代测序结果的SEQ和AB1文件，用于储存文字信息的txt文件等。但是这样繁多的也为文档的阅读和修改带来了麻烦，常见的文件处理软件已经没办法满足我们的需求了，下面向大家介绍几款工具

### ⭐⭐⭐**VScode**⭐⭐⭐
Visual Studio Code（简称VSCode）是微软开发的一款免费、跨平台的代码编辑器，可以在Windows、macOS和Linux上使用。它既轻量又功能强大，启动速度快，占用资源少，却能提供接近大型IDE的开发体验。VSCode支持丰富的插件生态，几乎所有编程语言（如Python、R、C++、HTML、LaTeX等)都可以通过插件扩展，同时还集成了Git版本控制、调试工具和智能代码补全功能，能够帮助开发者更高效地编写、调试和管理代码。此外，它还支持远程开发，用户可以通过Remote SSH插件连接服务器或集群，在本地环境中直接操作远程文件。VSCode 的界面简洁、可高度定制，主题、字体、快捷键和布局都能自由调整，因而成为目前最受程序员和生信研究者欢迎的开发环境之一。是一个功能强大的**All-in-one**的工具
[VScode下载链接](https://code.visualstudio.com/)
[VSCode中文帮助文档](https://vscode.js.cn/docs)
VScode也能用于打开多种类型的文件，包括常见的生物信息学文件类型，是一款轻量级但功能强大的文字处理工具。

具体插件安装等内容见后续相关内容。先介绍部分插件：

- github theme 一键还原github经典皮肤
- vscode-icons vscode官方出品的图标库
- copilot AI辅助编程工具

### Notepad
[Notepad下载链接](https://notepad-plus-plus.org/downloads/)

Notepad++ 是一种轻量级的免费的源代码编辑器和记事本替代品，支持多种编程语言及文件。

在下载好Notepad后建议打开**显示所有字符**，CRLF是换行符，向左的箭头是Tab键。

## Linux

许多生物信息学的软件（比如Bowtie2,qiime2,vsearch等）都主要在Linux上发布和维护。在执行大型计算任务的时候，计算平台也是Linux，如果不会Linux没有办法完成任务。但是大学或者研究机构的计算平台往往不随意开放，除非有必须使用计算资源的情况。这个时候有几种方法能够帮助我们使用Linux。

### Linux练习方式：VScode/虚拟机（针对Windows电脑）/云计算平台
- VS Code\
  包含一个功能齐全的[集成终端](https://vscode.js.cn/docs/terminal/basics)，它从工作区的根目录启动。它与编辑器集成，支持链接和错误检测等功能。集成终端可以像独立的终端一样运行mkdir和git等命令。建议初学者设立单独的文件夹进行练习，以免在不熟悉的情况下对文件进行误操作。
- 安装虚拟机\
[VM Virtualbox安装教程](https://blog.csdn.net/logic1001/article/details/147259511)
安装好虚拟机后可以在虚拟机中随便安装/删除软件，即使虚拟机崩溃也不会影响主系统，出问题了可以直接重置虚拟环境。
  
- 租用云计算服务平台
 例如阿里云，腾讯云等。对入门级别的生物信息学练习，只用租用最基本的类型就能满足需求。商用的云平台往往已经配置好了常用软件等，省去自己配置环境的麻烦。一些面向生物信息学计算的云平台还会提前配置常用数据库。

### SSH客户端
SSH（Secure Shell）是一种安全的网络通信协议，可以理解为一条加密的“秘密通道”，让用户能够从自己的电脑远程登录到另一台服务器或计算机上进行操作。它的主要作用是实现远程控制、命令执行和文件传输，同时通过加密保证数据和密码的安全性。在生信分析和科研计算中，SSH是连接服务器的基础工具。\
我们可以通过以下方式进行连接：
- [vscode](https://vscode.js.cn/docs/remote/ssh)链接服务器: 安装remote-ssh插件
- [Xterminal](https://www.xterminal.cn/): 这个工具不仅有强大的SSH连接功能，还有多个管理功能，可以高度个性化定制布局、主题。灵活的连接界面布局，让你根据自己的喜好随意拖拽和布局各个子窗口，满足你个性化的工作需求。界面美观，也可以进行灵活的上传与下载
- [xshell + xftp](https://zhuanlan.zhihu.com/p/659224032): 可以灵活的进行本地文件和服务器文件的传输

## 排版
### Markdown

markdown编译器的安装：
- vscode:markdown all in one, 好处是在vscode中，但是实时预览需要分屏操作。
- typora:这是一款即时渲染，所见即所得的编译器。界面简洁无干扰。
- notion:也是实时渲染，并且拥有强大的团队协作能力，但是部分markdown功能被阉割，且依赖网络，必须联网使用

Markdown 是一种轻量级标记语言，它允许人们使用易读易写的纯文本格式编写文档。也支持在文档中插入丰富的网页链接，或者以醒目的方式标注出代码块及其语言。Markdown在github，notion等中广泛使用。

Markdown 的核心特点包括：
- 简洁性：使用直观的符号来表示格式，比如用 # 表示标题，用 * 表示列表项。这些符号在视觉上就能传达其含义，即使不进行渲染也具有良好的可读性。
- 可读性：即使是纯文本形式的 Markdown 文档，也能清晰地展现文档的结构和层次。读者无需专门的软件就能理解内容的组织方式。
- 便携性：Markdown 文件是纯文本格式，可以在任何文本编辑器中打开和编辑，不依赖特定的软件或操作系统。
- 转换性：可以轻松转换为 HTML、PDF、Word 文档等多种格式，满足不同的发布需求。
(比如你现在正在阅读的文字也是用markdown写的)

Markdown 并不是 HTML 的替代品，而是 HTML 的简化版本。实际上，Markdown 的最终目标就是转换为 HTML。两者的关系可以这样理解：
Markdown 源码 → 解析器 → HTML 输出 → 浏览器渲染

[Typora官方的Markdown语言使用教程](https://support.typoraio.cn/zh/Markdown-Reference/)

[菜鸟Markdown语言使用教程](https://www.runoob.com/markdown/md-tutorial.html)


教程的内容很丰富，也许你记不住这么多内容，但是别担心，会最简单的标题，代码块，图片插入，链接插入等就可以放心使用了。在遇到一些特定场景，比如渲染高级的数学公式的时候，再哪里不会点哪里就行。

### Latex
LaTeX是一种“非所见即所得”的排版系统，用户需要输入特定的代码，保存在后缀为.tex的文件中，通过编译得到所需的pdf文件.

做个简单的对比：Word的界面就是一张纸，输入的时候是什么样子，最后呈现出来就是什么样子。这给了我们极高的自由度，也非常容易上手，但是有如下问题：对于对细节不敏感的用户，Word的排版常常会在细节存在问题，比如两段话之间行间距不同、字体不同、标题样式不同等；而且在论文撰写的过程中，word需要借助插件来完成诸如文献引用，公式插入等功能。相比之下，使用LaTeX进行排版，就像是在铺好的轨道上驾驶火车一样。使用LaTeX没有办法像Word一样非常自由，但是功能齐全且可以保证规范性，这使得LaTeX非常适合用于论文的排版。

Latex具有海量的模板库，很多时候并不需要完全从零开始书写；许多大学也会提供学术会议海报LaTeX模板，正式信件的LaTeX模板，毕业论文LaTeX模板等支持。

不过Latex学习曲线比较陡峭，但是学会后可以做出更加美观的论文、海报、简历等。Berkeley计算机系教授Christos Papadimitriou曾说过一句半开玩笑的话：

Every time I read a LaTeX document, I think, wow, this must be correct!

LaTeX的环境配置是个比较头疼的问题。最开始的时候可以考虑使用[Overleaf](https://www.overleaf.com/)这个在线LaTeX编辑网站。站内不仅有各种各样的LaTeX模版供你选择，还免去了环境配置的难题。但是如果Latex使用频率较高，可能需要付费才能满足使用需求，这个时候可以考虑用其他的工具，比如xxx

[一份其实很短的LaTeX入门文档](https://liam.page/2014/09/08/latex-introduction/)

[一份不太短的LaTeX文档](https://github.com/CTeX-org/lshort-zh-cn)

## 信息工作流
### Notion
[什么是Notion及Notion快速入门指南](https://www.bilibili.com/video/BV1YT4y1Q7xx/?spm_id_from=333.337.search-card.all.click&vd_source=25fa2c7552988fb2d3d6b74b9ba5eaca)
[Notion官方帮助文档](https://www.notion.com/zh-cn/help)

安装[notion](https://www.notion.com/)

我们甚至能够用notion制作一份个人学术网站：[为什么科研工作者需要个人网站？以及，怎样花很少时间做一个？](https://mp.weixin.qq.com/s/snYbVFAP7ERhNvaFDORrXw)


相信大家或多或少有着排版公众号的经验，想象这个工作流程：拖动一些元素进行大概的布置，在文字框内写上相关内容。但是如果现在你用相似的方式就能轻松制作一个美观的个人网站，不需要任何计算机编程基础，还能开源到互联网中，这是不是一件非常酷的事情呢。
### 文献管理———Notero
Notero是一款用于将项目和笔记同步到 Notion 的 Zotero 插件。通过它，我们可以**动态**地管理文档。我们可以使用 Zotero 添加文档和其他功能。添加的文档会自动将一些信息（例如摘要和作者信息）同步到注释页面。在注释页面中，您可以对文档进行笔记，为文档添加不同的类别，总结所使用的方法，并概括文档中的观点。欢迎使用以任何喜欢的方式进行扩展！

Notero的安装：
- 步骤 1：安装[notion](https://www.notion.com/)

- 步骤 2：安装[notero](https://github.com/dvanoni/notero?tab=readme-ov-file#installation-and-setup)

- 步骤 3：个性化生成自己的文献管理空间吧！

## 其他工具
### 数据备份
非常非常非常非常重要！！！！按照自己喜好进行即可，最好云平台和实体硬盘都存一份

# 学科基础

## 数学基础
### 线性代数

### 统计学

## 计算机基础
### R语言
### Python
https://wiki.python.org/moin/BeginnersGuide/Programmers

### Perl
### Linux
作为一名生物信息学研究者，你并不需要像系统管理员那样精通Linux的底层原理，但你确实需要**熟练掌握命令行操作**，能够独立完成生信分析流程中的各个关键步骤。下面是对需要掌握内容的简单总结，可供读者进行能力自查：
1. 文件与目录操作
   * `ls`, `cd`, `pwd`, `cp`, `mv`, `rm`, `mkdir`, `rmdir`, `find`
   * 会区分绝对路径与相对路径
   * 能快速在复杂目录中找到文件
2. 文件内容查看与处理
   * `cat`, `less`, `head`, `tail`, `grep`, `cut`, `awk`, `sort`, `uniq`, `wc`
   * 能从 FASTA、FASTQ、GFF、TSV 文件中提取和统计内容
3. 压缩与打包
   * `tar`, `gzip`, `gunzip`, `zip`, `unzip`
4. 权限与环境管理
   * `chmod`, `chown`, `export`, `.bashrc`, `PATH`
   * 知道如何配置软件路径、环境变量
5. 软件安装与包管理
   * 熟悉 `conda`, `apt`, `pip`
   * 能创建独立环境并在其中安装工具（如 fastp、vsearch、kraken2 等）
   * 知道如何导出、分享 `conda` 环境或镜像
6. 任务管理与监控
   * `top`, `htop`, `ps`, `kill`, `df`, `du`,`nohup`等
   * 会查看内存、CPU占用和任务状态
7. 远程连接与文件传输
   * `ssh`, `scp`, `rsync`, `screen`, `tmux`
   * 能连接远程服务器并在断开连接后继续运行程序，能实现文件的上传与下载
8. 脚本编写与自动化处理
   * 能编写简单的 `bash`、`awk`，或在Linux环境中使用`perl` 或 `python` 脚本批量处理数据
   * 理解循环 (`for`, `while`)、变量、管道符 (`|`) 和重定向 (`>`, `>>`)
9. 日志与错误排查
   * 能看懂生信工具输出信息，定位错误来源（输入格式、路径、依赖包等）

想要入门Linux，可以查看：\
[Linux入门教程](https://biobooks.readthedocs.io/zh-cn/latest/4-linux/index.html)（文档内容不仅是Linux，也是一份很好的生物信息学入门资料）\
[Terminus](https://www.mprat.org/Terminus/),是一款基于文本的冒险游戏，旨在用游戏化的方式教用户如何使用终端命令，是初学者探索Linux的良好开端\
一份由中科大编写的[Linux拓展教程]([https://www.runoob.com/linux/linux-tutorial.html](https://101.lug.ustc.edu.cn/)),供希望对Linux有更深入了解的读者学习。
### conda

### Vim
Vim是很多服务器自带的命令行编辑器，很多时候我们在服务器上工作，没有图形界面、也不能用鼠标打开文件，但有对代码进行简单改动的需求，这时Vim就是很方便的命令行文本编辑器。省去了我们在频繁在本地和服务器传送文件的麻烦。\
但是Vim的学习曲线非常陡峭，不过作为生物信息学者，我们只需要掌握最简单的几个指令：

你可以在终端上完成下面这个简单的练习，并恭喜你打开Vim的大门：

- vim HelloWorld.txt·
- 键入 ·i·
- 编辑 输入任意信息，如Hello World
- 键入 [ESC]
- 键入:wq 保存退出

这时候再用ls查看目前目录下的文件，就多出了一个HelloWorld.txt

下面是稍详细的讲解：

![Vim模式示意图](https://image-static.segmentfault.com/805/181/805181512-5d724407de0cc)

正常模式 (Normal Mode)
插入模式 (Insert Mode)
可视模式 (Visual Mode)
命令模式 (Command Mode)
①. 正常模式 (Normal Mode)
正常模式主要用来浏览和修改文本内容的。一般的，打开 Vim 都是正常模式。在任何模式下，只要按下 Esc 键就可以返回正常模式。
②. 插入模式 (Insert Mode)
插入模式则用来向文本中添加内容的，我自己常用的是i和o。i 在光标所在字符前开始输入文字并进入插入模式；o (字母 o) 在光标所在行的下面单独开一新行来输入文字并进入插入模式。

③. 可视模式 (Visual Mode)
可视模式相当于高亮选取文本后的普通模式。可视模式具有子模式，以行为单位进行选取的可视行模式，使用 “V” 键进入（也就是 Shift+v）；和以块为单位进行选取的可视块模式，使用 “Ctrl+v” 键进入。
④. 命令模式 (Command Mode)
命令模式则多用于操作文本文件（而不是操作文本文件的内容），例如保存文件；或者用来改变编辑器本身的状态，例如设定多栏窗口、标签或者退出编辑器。

如果你想很炫酷的像电影里的黑客一样，双手不离键盘。那你可以深入学习Vim，不可否认Vim有着非常多的优点：方便的文件切换，宏操作可以批量化处理重复操作，异常丰富的插件生态etc.

想要深入学习Vim可以参考以下资料：
- [MIT Editors(Vim)](https://missing.csail.mit.edu/2020/editors/)
- [一份中文入门教程](https://www.cnblogs.com/jichun29/p/18728459)

### Shell脚本编程
[1](https://www.shellscript.sh/philosophy.html)




## 生物学基础
### 生物化学
蛋白质1-4级结构
RNA
DNA
### 测序技术
#### 一代测序

#### 二代测序
生物信息学研究者需要系统地了解二代测序（NGS）的原理，只有理解数据是如何产生的，才能正确地处理和解释结果。了解测序原理可以帮助我们区分真实信号与技术噪音，理解为什么需要进行质量控制（如去除低质量碱基和接头序列），并根据不同的测序策略（如单端、双端、不同片段长度）设计合适的分析流程。此外，掌握测序原理还能帮助我们判断数据质量、发现异常、更好的设计实验等。\
关于Illumina测序原理的[动画](https://www.youtube.com/watch?v=fCd6B5HRaZ8&t=49s)，建议反复观看，直到理解每一个细节
[Next-Generation Sequencing(NGS)](https://www.thermofisher.com/nl/en/home/life-science/sequencing/sequencing-learning-center/next-generation-sequencing-information/ngs-basics/what-is-next-generation-sequencing.html)简介
更全面的二代测序技术[笔记](https://mercury-02.github.io/2024/02/21/%E6%B7%B1%E5%BA%A6%E6%B5%8B%E5%BA%8F%E6%95%B0%E6%8D%AE%E5%88%86%E6%9E%90%E7%AC%94%E8%AE%B0/#%E4%BA%8C%E3%80%81SoLiD%E6%B5%8B%E5%BA%8F)，包含了SoLiD测序技术和Roche454测序技术

#### 蛋白质测序
#### 蛋白质结构
### 进化生物学

## 生物信息学常用网站
### GALAXY平台
[生信百宝箱](https://zhuanlan.zhihu.com/p/700750865)


# 生物信息学进阶
## 常见文件格式
- FASTA
  FASTA 格式是一种基于文本的格式，用于表示核苷酸序列或氨基酸（蛋白质）序列，其中核苷酸或氨基酸使用单字母代码表示。
  序列以大于号（“>”）开头，后跟序列描述（所有内容均位于一行中）。描述行之后的行是序列表示，每个氨基酸或核酸对应一个字母。
  示例：
  \>MCHU - Calmodulin - Human, rabbit, bovine, rat, and chicken
  MADQLTEEQIAEFKEAFSLFDKDGDGTITTKELGTVMRSLGQNPTEAELQDMINEVDADGNGTID
  FPEFLTMMARKMKDTDSEEEIREAFRVFDKDGNGYISAAELRHVMTNLGEKLTDEEVDEMIREA
  DIDGDGQVNYEEFVQMMTAK
- FASTQ
  FASTQ 文件每个序列包含四个以行分隔的字段：字段 1 以“@”字符开头，后跟序列标识符和可选的描述（类似于 FASTA 标题行）。字段 2 是原始序列字母。字段 3 以“+”字符开头，后跟相同的序列标识符（以及任何描述）。字段 4 编码字段 2 中序列的质量值，并且必须包含与序列中字母数量相同的符号。包含单个序列的 FASTQ 文件可能如下所示：
  @SEQ_ID\
  GATTTGGGGTTCAAAGCAGTATCGATCAAATAGTAAATCCATTTGTTCAACTCACAGTTT\
  +\
  !''((((+))%%%++)(%%%%).1-+''))**55CCF>>>>>>CCCCCCC65
  它们在格式上有一些区别：FASTA 以“>”开头，FASTQ 以“@”开头。FASTQ 文件使用“+”连接行，并包含质量值信息。FASTA 文件更灵活，允许序列包含多行，而 FASTQ 格式的序列只能包含一行。FASTQ 文件可以提供更多关于序列的信息，它们包含质量记录。因此，在序列长度相同的情况下，FASTQ 文件的大小也更大。
  [FASTQ 和 Illumina测序](https://knowledge.illumina.com/software/general/software-general-reference_material-list/000002211)
  [FASTQ 和 Q-score（第四行信息）](https://en.wikipedia.org/wiki/FASTQ_format)
  Transfer FASTQ into FASTA or combine FASTA and QUAL into FASTQ -- [GALAXY Platform](https://usegalaxy.org/) : Tools--FASTA/FASTQ

## BLAST
BLAST（Basic Local Alignment Search Tool，基本局部比对搜索工具）是生物信息学中广泛使用的一种序列比对工具。它通过比对生物序列，帮助研究者发现序列之间的相似性，从而推断其功能和进化关系。\
一个关于为什么需要BLAST以及基本的BLAST算法思想的[视频](https://www.youtube.com/watch?v=NwiETShpIDo)

### Blast的基本原理
1. 种子匹配
BLAST首先将查询序列分割成多个短片段，称为种子（seed）。种子匹配是BLAST比对的第一步，它通过比较查询序列的种子与数据库序列中的种子来识别潜在的相似区域。

2. 扩展
一旦种子匹配成功(序列匹配得分高于某个阈值)，BLAST将利用动态规划算法对匹配区域进行扩展。这个过程会计算每个可能匹配区域的得分，并进行扩展。\


4. 评估
在扩展过程中，BLAST会使用E-value（期望值）来评估匹配的显著性。E-value越小，表示匹配越有可能是一个真实的相似性，而非随机事件。

Blast的分类
1. BLASTN
用于核酸序列比对，常用于基因序列或全基因组序列比对。

2. BLASTP
用于蛋白质序列比对，适用于蛋白质家族和结构域研究。

3. BLASTX
用于核苷酸序列与蛋白质序列的比对，将核酸序列翻译成蛋白质序列后进行比对。



As others have said BLAST is really outdated. There was a very similar tool to blast but faster and quite popular (usearch) but it is closed source. Vsearch is similar to usearch but open source. there are tons more since then: blat, bowtie, diamond. Generally they are split between kmer based approaches and burrow-wheeler based (BWA).



## 计算生物学
[英文版计算生物学](https://github.com/Zhiyi-Zhao/Computational-biology),中文版正在路上
## R语言绘图
## 机器学习
## 深度学习
## 软件工程
## sbatch
## 统计学进阶

## 微生物生态
对这个话题感兴趣的朋友可以转向...

# 计算机进阶
## HMTL语言
## Github
GitHub 是一种基于云的平台，可在其中存储、共享并与他人一起编写代码。

通过将代码存储在 GitHub 上的“存储库”中，你可以：
- “展示或共享”你的工作。
- 持续“跟踪和管理”对代码的更改。
- 让其他人“审查”你的代码，并提出改进建议。
在共享的项目中开展“协作”，无需担心这些更改会在准备好集成更改之前影响协作者的工作。
协作式工作是 GitHub 最基本的功能之一，该功能由开源软件 Git 实现，而 GitHub 是以该软件为基础进行构建的。

[Github入门](https://docs.github.com/zh/get-started)

