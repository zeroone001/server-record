##### VPS 一键安装谷歌 BBR 加速

1. `wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh && chmod +x bbr.sh && ./bbr.sh` 安装BBR

2. `sysctl net.ipv4.tcp_congestion_control net.core.default_qdisc` 检查BBR是否安装成功
