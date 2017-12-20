# Mac shell (zsh ~ oh-my-zsh)

> 用来与Linux内核进行交互

``` code
  // 查看系统有几种shell，默认都是bash,mac多一个zsh
  car /etc/shells

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
psychoanalyze-pinhead 回车


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
telnet towel.blinkenlights.nl
```