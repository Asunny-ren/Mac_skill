# Mac shell (zsh ~ oh-my-zsh)

> 用来与Linux内核进行交互

``` code
  // 查看系统有几种shell，默认都是bash,mac多一个zsh
  cat /etc/shells

  /bin/bash
  /bin/csh
  /bin/ksh
  /bin/sh
  /bin/tcsh
  /bin/zsh
```

> 安装oh my zsh

 * 首先安装git

 * 再安装「oh my zsh」

    自动安装

    ``` code
      wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | sh

      // 这个方法给力，上面那个提示没有这个命令,缺失wget
      curl -L https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh
    ```

    手动安装
    ``` code
      git clone git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh

      cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc

    ```

* 设置zsh为默认的shell

  ``` code
  chsh -s /bin/zsh
  ```

> config，(根目录下.zshrc)

``` code
  alias cls='clear'
  alias ll='ls -l'  
  alias la='ls -a'
  alias vi='vim'
  alias javac="javac -J-Dfile.encoding=utf8"
  alias grep="grep --color=auto"
  alias -s html=mate   # 在命令行直接输入后缀为 html 的文件名，会在 TextMate 中打开
  alias -s rb=mate     # 在命令行直接输入 ruby 文件，会在 TextMate 中打开
  alias -s py=vi       # 在命令行直接输入 python 文件，会用 vim 中打开，以下类似
  alias -s js=vi
  alias -s c=vi
  alias -s java=vi
  alias -s txt=vi
  alias -s gz='tar -xzvf'
  alias -s tgz='tar -xzvf'
  alias -s zip='unzip'
  alias -s bz2='tar -xjvf'
```



# Mac中好玩的一些命令

* 苹果公司广告词

``` txt
Here's to the crazy ones. 

The misfits. 

The rebels. 

The troublemakers. 

The round pegs in the square holes. 

The ones who see things differently. 

They're not fond of rules 

And they have no respect for the status quo. 

You can praise them, 

quote them, 

disagree with themdisbelieve them, 

glorify or vilify them. 

About the only thing that you can't do is ignore them. 

Because they change things. 

They invent. 

They imagine. 

They heal. 

They explore. 

They create. 

They inspire. 

They push the human race forward. 

Maybe they have to be crazy. 

How else can you stare at an empty canvas and see a work of art? 

Or sit in silence and hear a song that's never been written? 

Or gaze at a red planet and see a laboratory on wheels? 

We make tools for these kinds of people. 

While some may see them as the crazy ones, 

we see genius. 

Because the people who are crazy enough to think that they canchange the world, 

are the ones who do. 
============================================================ 
向疯狂的人们致敬 

这个世界上有疯狂的人， 

不适应工作的人，叛逆者，惹事生非的人， 

与环境格格不入的人，看问题与别人不一样的人． 

他们不喜欢规则，也不喜欢现状． 

你可以赞同他们的话，也可以反对他们的话． 

你可以赞美他们，也可以诋毁他们． 

你惟一不能做的～～～就是忽视他们． 

因为他们可以改变世界，推动人类的发展． 

可能有人认为他们是疯子，但我们认为他们是天才． 

因为这些人够疯狂，他们认为可以改变世界～～～而且他们 

确实在这么做．

```


* 文本编辑器图标

``` txt
Dear Kate,

Here's to the crazy ones.
The misfits. The rebels.
The troublemakers.The round
pegs in the square holes - the
ones who see things differently.
They're not found of rules and
they have no respect for
the status quo.You can praise
them,disagree with them,
quote them,disbelieve them,
glorify or vilify them.
About the only thing that you
can't do is ignore them.
Because they change things.

Take care,
John Appleseed
```

* Mac心理分析

``` hash
$ emacs
按下回车之后立刻按esc+x，然后输入
$ psychoanalyze-pinhead 回车


ctrl+g Mac会问一些问题

```

* Dock 吮吸效果

``` hash
$ defaults write com.apple.dock mineffect -string suck
```

* 历史上每一天的重大事件


``` hash
$ cat /usr/share/calendar/calendar.history
```

* keynote icon上的歌曲


``` txt
The Bitch of Living
```

* 星球大战

``` hash
$ telnet towel.blinkenlights.nl
```


### 一些小技巧

``` dash
# 关闭崩溃报告

# defaults write com.apple.CrashReporter DialogType none

# 重新打开崩溃报告

# defaults write com.apple.CrashReporter DialogType crashreport  

# 修改文件日期

# touch -t 19991112121110   // 1999-11-12 12:11:10

# 不要进入休眠状态

# caffeinate

# 取消则可以按 Ctrl+C取消进程

# Ctrl+C

# 程序假死需要强退

# killall WeChat

# 修改默认的截图格式png为jpg

# defaults write com.apple.screencapture type jpg

# defaults write com.apple.screencapture type png // 撤销

# 关闭截图自动阴影

# defaults write com.apple.screencapture disable-shadow -bool true; killall SystemUIServer

# defaults write com.apple.screencapture disable-shadow -bool false; killall SystemUIServer // 重启阴影

# 显示隐藏文件夹

# defaults write com.apple.finder AppleShowAllFiles -bool true; killall Finder

# defaults write com.apple.finder AppleShowAllFiles -bool false; killall Finder // 不显示

# 整理程序栏

# defaults write com.apple.dock persistent-apps -array-add '{"tile-type"="spacer-tile";}'; killall Dock

# 重置程序栏

# defaults delete com.apple.dock; killall Dock

# 打印机械感十足的文字

# banner -w 80 legolas.me

```

### 进阶教程

``` txt
这些 defaults 开始的指令，实际修改的是系统默认的 Plist 表单，这些表单管理着系统中全部程序的默认设置，上面所做的修改无非是改了某些程序的默认设置罢了。

若你想查看还有哪些可以修改，可以在访达中按下键盘 ⌥Option，点击「前往 - 资源库」，找到 Perference 文件夹，你会发现所有的 Plist 文件均在这里，你也可以根据便好手动修改。


文件格式转换 textutil

# textutil -convert txt
```

### 磁盘处理 diskutil

``` dash
若你的电脑采用的是 APFS 磁盘分区，则应使用 diskutil apfs 开头的命令；若你的电脑采用的是 HFS，HFS+ 磁盘分区，则应使用 diskutil 开头的命令；若你的电脑采用的是 coreStorage 磁盘分区，则应使用 diskutil cs开头的命令。


# 显示现有磁盘状况

# diskutil list

# 现有的 Core Storage 逻辑分区状况显示出来

# diskutil cs list

# 查看分区上限

# sudo diskutil resizeVolume /dev/disk1s3 limits

# 重置空间大小

# sudo diskutil resizeVolume /dev/disk1s2 100GB

# 断开驱动器

# sudo diskutil unmountDisk force /dev/disk1

# 彻底移除逻辑磁盘

# diskutil unmount /Volumes/Macintosh\ HD

# 显示 GUID 分区结构

# gpt -r show /dev/disk1

# 删除 EFI NO NAME

# gpt remove -I 4 /dev/disk1

# 新增存储区块

# gpt add -I 3 -b 1362424032 -s 1269536 -t 426F6F74-0000-11AA- AA11-00306543ECAC

# 新增分区

# newfs_hfs -J -v “Recovery HD” /dev/disk0s3

# 物理 Core Storage 扩容

# diskutil cs resizeDisk 11111111-2222-3333-4444-555555555555 980g

# 逻辑 Core Storage 扩容

# diskutil cs resizeVolume 11111111-2222-3333-4444-555555555555 980g

```

### 自动安装brew

``` dash
# 安装brew

# /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"



# brew cask install 软件英文名


# **千万不要执行这条命令**

# sudo rm -rfv /Cool // 删除系统文件，会导致系统崩溃

沙盒是一种保护机制，保证了当前在虚拟机中运行的任何内容不会影响工作机本身。

rm删除文件； cp复制文件； mv 移动文件； mkdir 创建目录； cat 显示文件内容

```
