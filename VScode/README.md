##### vscode扩展之根据Vue模板自动生成Scss结构 -- AutoScssStruct4Vue

* 安装： AutoScssStruct4Vue ， vscode直接搜索安装
* 修改源码： cd ~/.vscode/extensions/kq.autoscssstruct4vue-0.1.2
* 找到scssManage.js  ,有两个这个文件，里面的函数 rnIndent， 然后把空格改为四个
* 把软件整个关掉，再重新打开；就ok了
   
* 使用：点到<template>里面，获取焦点；
* 右键autoScssStruct

#### Plugins如下

1. View In Browser # 浏览器里面打开文件
2. AutoScssStruct4Vue #根据Vue模板自动生成Scss结构
3. vue # Syntax Highlight for Vue.js

#### 主题插件

[atomiks.moonlight](https://github.com/atomiks/moonlight-vscode-theme)

#### VSCode 不显示在程序坞中

```s
killall Dock
```
