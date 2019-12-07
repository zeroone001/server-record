1. 解决git status 不显示中文？

`git config --global core.quotepath false`

2. push an existing repository from the command line

```s
git remote add origin https://github.com/zeroone001/book-collection.git

git push -u origin master
```

3. git alias 命令的别名
   
> [自定义Git命令](https://www.kawabangga.com/posts/2177)

`vim ~/.gitconfig`

```
[alias]
    s = status
```
