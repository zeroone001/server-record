#### 没翻墙的客户端安装依赖的方式

`npm --registry https://registry.npm.taobao.org install`

#### Mac 全局安装的依赖的位置

`cd /usr/local/lib/node_modules/`

#### 常用command

```s
npm config ls # 可以查看npm配置的信息
npm config edit # 可以直接配置

```

#### Mac + npm 权限问题
```s
# 将/usr/local 目录的所有者变更为当前的用户
sudo chown -R $(whoami) /usr/local
# 修改目录所有者
sudo chown -R $(whoami) your-project-path
# 修改npm缓存目录的权限问题
sudo chown -R $(whoami) $(npm get cache)
```

#### npm 缓存目录

```s
# ~/.npm
npm get cache

```