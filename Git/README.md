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

#### submodule Git

指定文件目录

`git submodule add https://github.com/chaconinc/someSubmodul src/lib`

用来初始化本地配置文件

`git submodule init`

从该项目中抓取所有数据并检出父项目中列出的合适的提交(指定的提交)
 
`git submodule update`

##### submodule 删除子模块

1. git rm --cached [path]

根据路径删除子模块的记录

2. 编辑“.gitmodules”文件，将子模块的相关配置节点删除掉

清理子模块配置

3. 编辑“ .git/config”文件，将子模块的相关配置节点删除掉, vim config 删除里面的配置, cd modules/lib 删除里面的子模块

清理子模块配置

4) 手动删除子模块残留的目录

清理脏文件


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

#### Git 文件名大小写敏感

```s
git config core.ignorecase false
```

5. 回退撤销的相关操作

```s
# 撤销add
git reset HEAD <filename>
# 撤销commit
git reset --hard <commitID>
git push --force
```

#### Git 强制切分支

```s
git checkout -f branchName
```

#### Git怎样撤销一次分支的合并Merge

```s
git reset --hard 【merge前的版本号】
```

## subtree

#### 设置公共仓库remote
该步骤意在简化subtree命令，设置pc_global仓库remote：

```shell
git remote add -f pcglobal https://gitlab-team.xxxx.com/xx/xxxx.git
```

#### 在本仓库中新增公共仓库
该步骤用于拉取公共资源／组件到`lib`文件夹，**仅在仓库项目搭建时使用：**

```shell
git subtree add --prefix=lib pcglobal master
```

#### 从公共仓库拉取更新
该步骤在公共仓库代码 **有更新** 时使用，拉取最新的公共资源／组件：

```shell
git subtree pull --prefix=lib pcglobal master
```

#### 推送修改到公共仓库
该步骤在开发过程中修改了公共资源／组件时使用，请在 **确保不影响其他事业部页面** 的情况下推送：

```shell
git subtree push --prefix=lib pcglobal master
```