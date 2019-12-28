#### centos install nginx
```s
# install
yum install nginx -y

systemctl enable nginx # 设置开机启动
systemctl start nginx # 启动软件

systemctl restart nginx  # 
systemctl reload nginx # 一般重新配置之后，不希望重启服务，这时可以使用重新加载。
# 查看status
systemctl status nginx
# 主配置文件
cd /etc/nginx/nginx.conf

# nginx 服务配置文件存放地点, 这个目录下存放
# 必须以.conf结尾，可以创建多个独立的配置文件
# 独立的配置文件，建议遵循以下命名约定，比如你的域名是 kaifazhinan.com，那么你的配置文件的应该是这样的 /etc/nginx/conf.d/kaifazhinan.com.conf，如果你在一个服务器中部署多个服务，当然你也可以在文件名中加上 Nginx 转发的端口号，比如 kaifazhinan.com.3000.conf，这样做看起来会更加友好
cd /etc/nginx/conf.d

# 如果你的配置中有很多重复的代码，那么建议你创建一个 /etc/nginx/snippets 文件夹，在这里面存放所有会被复用的代码块，然后在各个需要用到的 Nginx 的配置文件中引用进去，这样可以更方便管理和修改
```

#### SetUp

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
            proxy_pass http://127.0.0.1:3000;  # 添上这一行（端口号写你nodejs运行的端口号）
        }

        error_page 404 /404.html;
            location = /40x.html {
        }

        error_page 500 502 503 504 /50x.html;
            location = /50x.html {
        }
    }
```

#### 参考网站

[How To Set Up Nginx Server Blocks on CentOS 7](https://linuxize.com/post/how-to-set-up-nginx-server-blocks-on-centos-7/)
