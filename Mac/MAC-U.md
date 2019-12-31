###### Mac 制作U盘启动盘

首先，格式化u盘
上网自己查
cd 到 Downloads目录
cd ~/Downloads
输入命令，转换成mac可用模式
hdiutil convert -format UDRW -o ubuntu.iso ubuntu-18.04-desktop-amd64.iso


把dmg的拓展名去掉
ubuntu.iso.dmg ubuntu.iso
查看u盘挂载点
diskutil list

将U盘从系统中卸载掉
diskutil unmountDisk /dev/disk2

dd 镜像到U盘
sudo dd if=ubuntu.iso of=/dev/rdisk2 bs=1m
OK ，拔出u盘即可