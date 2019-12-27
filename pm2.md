```s
// install
npm install -g pm2 
// Usage
pm2 start server.js
pm2 restart ID
pm2 stop all
pm2 stop 0 # 停止 id为 0的指定应用程序 
pm2 delete 0 # 删除指定应用 id 0

pm2 list # 列表 PM2 启动的所有的应用程序
pm2 logs [app-name] # 显示指定应用程序的日志
pm2 monit # 显示每个程序的CPU和内存的占用情况
// Nuxtjs
pm2 start npm --name "xxx" -- run build

```