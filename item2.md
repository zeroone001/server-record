1. 安装两个插件

```
zsh-autosuggestions
zsh-syntax-highlighting
```

2. 安装

`git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions`
`git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting`

之后编辑 `vim ~/.zshrc` 找到plugins=(git), 然后在git 后面加空格 变成`plugins=(git zsh-autosuggestions zsh-syntax-highlighting)`