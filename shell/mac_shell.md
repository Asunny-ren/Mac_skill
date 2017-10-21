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
