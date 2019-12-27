```s
# install
yum install nginx -y

systemctl enable nginx # 设置开机启动
systemctl start nginx # 启动软件

systemctl restart nginx  # 
systemctl reload nginx # 一般重新配置之后，不希望重启服务，这时可以使用重新加载。
# 查看status
systemctl status nginx
# 配置文件
cd /etc/nginx/nginx.conf
```