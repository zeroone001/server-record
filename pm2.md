```s
# install
npm install -g pm2 

# 检查是否装好

pm2 --version

# Usage
pm2 start server.js
pm2 restart ID
pm2 stop all
pm2 stop 0 # 停止 id为 0的指定应用程序 
pm2 delete 0 # 删除指定应用 id 0

pm2 list # 列表 PM2 启动的所有的应用程序
pm2 logs [app-name] # 显示指定应用程序的日志
pm2 monit # 显示每个程序的CPU和内存的占用情况
# Nuxtjs
pm2 start npm --name "xxx" -- run build

```
#### pm2 运行node服务

因为node是单进程的，进程被杀掉后，整个服务就跪了

#### Feature

* 内建负载均衡（使用Node cluster 集群模块）
* 后台运行
* 0秒停机重载(维护升级的时候不需要停机).
* 具有Ubuntu和CentOS 的启动脚本
* 停止不稳定的进程（避免无限循环）
* 控制台检测
* 提供 HTTP API
* 远程控制和实时的接口API ( Nodejs 模块,允许和PM2进程管理器交互 )

#### npm 运行

`pm2 start npm --name test -- start`

#### Cluster and Fork mode difference in PM2

