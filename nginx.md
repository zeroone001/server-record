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

```s
# nginx.conf
server {
        listen       80 default_server;
        listen       [::]:80 default_server;
        server_name www.hxvin.com,hxvin.com;   /#修改这一行（写上你绑定的域名）
       root         /usr/share/nginx/html;

        # Load configuration files for the default server block.
        include /etc/nginx/default.d/*.conf;

        location / {
proxy_pass http://127.0.0.1:4000;  # 添上这一行（端口号写你nodejs运行的端口号）
        }

        error_page 404 /404.html;
            location = /40x.html {
        }

        error_page 500 502 503 504 /50x.html;
            location = /50x.html {
        }
    }
```

