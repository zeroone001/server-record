#### centos 安装 Git

```s
    yum install git
    
    git config --global user.name 'zeroone001'
    git config --global user.email 'ilylys@163.com'

    git config --list

```
1. 解决git status 不显示中文？

`git config --global core.quotepath false`

2. push an existing repository from the command line

```s
git remote add origin https://github.com/zeroone001/book-collection.git

git push -u origin master
```

3. submodule Git

指定文件目录

`git submodule add https://github.com/chaconinc/someSubmodul src/lib`

用来初始化本地配置文件

`git submodule init`
 从该项目中抓取所有数据并检出父项目中列出的合适的提交(指定的提交)
 
`git submodule update`


4. git alias 命令的别名
   
> [自定义Git命令](https://www.kawabangga.com/posts/2177)

`vim ~/.gitconfig`

```
[alias]
    s = status
```
5. permission denied, open '/Users/smzdm/.npm/

```
sudo chown -R $USER:$GROUP ~/.npm
sudo chown -R $USER:$GROUP ~/.config
sudo npm cache clean -f
```
#### Mac 安装Git

> [下载链接](https://sourceforge.net/projects/git-osx-installer/)
