#### MAC终端命令行下用sublime、vscode、atom打开文件或目录

`vim ~/.zshrc`
```js
alias atom='/Applications/Atom.app/Contents/MacOS/Atom'
alias subl='/Applications/SublimeText.app/Contents/SharedSupport/bin/subl'
alias code='/Applications/Visual\ Studio\ Code.app/Contents/Resources/app/bin/code'
```

`WwKnDas4aEmE`

1. 安装两个插件

```s
# 自动提示与命令补全
zsh-autosuggestions 
# 语法高亮效果
zsh-syntax-highlighting
```

2. 安装

`git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions`
`git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting`

之后编辑 `vim ~/.zshrc` 找到plugins=(git), 然后在git 后面加空格 变成`plugins=(git zsh-autosuggestions zsh-syntax-highlighting)`

3. 快速唤起编辑器
`vim ~/.zshrc`
```s
alias atom='/Applications/Atom.app/Contents/MacOS/Atom'
alias subl='/Applications/SublimeText.app/Contents/SharedSupport/bin/subl'
alias code='/Applications/Visual\ Studio\ Code.app/Contents/Resources/app/bin/code'
```