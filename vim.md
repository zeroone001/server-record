 > [vim](https://blog.csdn.net/houqd2012/article/details/8111738)
 确认一下你的VIM是否已经安装 `rpm -qa|grep vim`

 vim编辑器需要安装三个包：
```
   vim-enhanced-7.0.109-7.el5
   vim-minimal-7.0.109-7.el5
   vim-common-7.0.109-7.el5
```

##### 高亮

1. `cp /usr/share/vim/vimrc ~/.vimrc`
2. `vi ~/.vimrc`
3. ```
set nocompatible "去掉有关vi一致性模式，避免以前版本的bug和局限

set nu! "显示行号

filetype on "检测文件的类型

set history=1000 "记录历史的行数

set background=dark "背景使用黑色

syntax on "语法高亮度显示

set autoindent "vim使用自动对齐，也就是把当前行的对齐格式应用到下一行(自动缩进）

set cindent "（cindent是特别针对 C语言语法自动缩进）

set smartindent "依据上面的对齐格式，智能的选择对齐方式，对于类似C语言编写上有用

set tabstop=4 "设置tab键为4个空格，

set shiftwidth =4 "设置当行之间交错时使用4个空格

set ai! " 设置自动缩进

set showmatch "设置匹配模式，类似当输入一个左括号时会匹配相应的右括号

set guioptions-=T "去除vim的GUI版本中得toolbar

set vb t_vb= "当vim进行编辑时，如果命令错误，会发出警报，该设置去掉警报

set ruler "在编辑过程中，在右下角显示光标位置的状态行

set nohls "默认情况下，寻找匹配是高亮度显示，该设置关闭高亮显示

```