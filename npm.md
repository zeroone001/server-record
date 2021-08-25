## 查看依赖的信息

`npm info <name>` 或者 `npm view <name>`

## 安装最新版本

`npm i <name>@latest --save`

## 安装最新的beta版本

`npm i <name>@beta --save`



## npm install 报错，Unhandled rejection Error: EACCES: permission denied



### 背景

电脑里面的前端项目，`npm install` 的时候发生报错，报错如下：

```shell
Unhandled rejection Error: EACCES: permission denied, open '/Users/xxxx/.npm/_cacache/index-v5/c6/f0/527283268706f7919c6eac85bc45e04152001540e94e60084376321fde13'

Unhandled rejection Error: EACCES: permission denied, open '/Users/xxxx/.npm/_cacache/index-v5/36/b8/b70b01973fa417e1e25a825e9d090755a5cb94d65b25d36c7e7e48349e1e'

npm ERR! cb() never called!

npm ERR! This is an error with npm itself. Please report this error at:
npm ERR!     <https://npm.community>

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/xxxx/.npm/_logs/2021-08-24T06_11_00_187Z-debug.log
```



### 解决方案如下

通过对报错的分析，应该是权限方面的问题。

将用户的npm相关文件夹的所有权还到当前用户

```shell
sudo chown -R $USER:$GROUP ~/.npm
sudo chown -R $USER:$GROUP ~/.config
```







