##### centos 安装 SS服务器

1. `wget –no-check-certificate https://tangyuecan.com/shadowsocks-go.sh`
2. `chmod +x shadowsocks-go.sh`
3. `./shadowsocks-go.sh 2>&1 | tee shadowsocks-go.log `
4. 接下来就是傻瓜式的配置端口密码
5. 下面是之后的常用命令
6. 重启
```
    start | stop | restart | status
    
    重启
    `/etc/init.d/shadowsocks restart`
```
7. 卸载 `./shadowsocks.sh uninstall`

###### centos 安装 wget

`yum install -y wget`

###### centos 安装NODE

`yum install epel-release`
`yum install nodejs`
`yum install npm`

##### yum

`yum module list`

##### pm2

`npm i pm2 -g`

##### 显示隐藏文件夹

`ls -a`

##### Centos查看端口占用情况和开启端口命令

`netstat -ntlp`