###### linux免密码登录
1. `cat ~/.ssh/id_rsa.pub` 查看sshkey，有的话，直接第三步

2. 如何生成SSH KEY
1. 检查SSH keys是否存在
输入下面的命令，如果有文件id_rsa.pub 或 id_dsa.pub，则直接进入步骤3将SSH key添加到GitHub中，否则进入第二步生成SSH key
ls -al ~/.ssh
# Lists the files in your .ssh directory, if they exist
2. 生成新的ssh key
第一步：生成public/private rsa key pair
在命令行中输入ssh-keygen -t rsa -C "your_email@example.com"
默认会在相应路径下（/your_home_path）生成id_rsa和id_rsa.pub两个文件，如下面代码所示
ssh-keygen -t rsa -C "your_email@example.com"
# Creates a new ssh key using the provided email
Generating public/private rsa key pair.
Enter file in which to save the key (/your_home_path/.ssh/id_rsa):
第二步：输入passphrase（本步骤可以跳过）
设置passphrase后，进行版本控制时，每次与GitHub通信都会要求输入passphrase，以避免某些“失误”
Enter passphrase (empty for no passphrase): [Type a passphrase]
Enter same passphrase again: [Type passphrase again]
在github或者gitlab上输入sshkey，
cat ~/.ssh/id_rsa.pub

3. `ssh-copy-id -i ~/.ssh/id_rsa.pub -p 27518 root@104.160.34.211` 关键