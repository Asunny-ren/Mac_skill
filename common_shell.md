# Mac common shell (Mac上面实用的一些命令)

> 修改按键，切换长键盘来输入重音字符或非英文字符
  ``` code
    // 重复按键
    defaults write -g ApplePressAndHoldEnabled -bool FALSE

    // 长键盘来输入重音字符或非英文字符
    defaults delete -g ApplePressAndHoldEnabled
  ```
