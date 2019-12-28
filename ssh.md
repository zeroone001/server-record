#### SSH 免密码登录

##### 如何生成SSH KEY

1. 检查SSH keys是否存在
   
输入下面的命令，如果有文件id_rsa.pub 或 id_dsa.pub，则直接进入步骤3将SSH key添加到GitHub中，否则进入第二步生成SSH key
```s
# Lists the files in your .ssh directory, if they exist
ls -al ~/.ssh
```
2. 生成新的ssh key
   
第一步：生成public/private rsa key pair
在命令行中输入 ssh-keygen -t rsa -C "your_email@example.com"
默认会在相应路径下（/your_home_path）生成私钥id_rsa和公钥id_rsa.pub两个文件，如下面代码所示

```s
# Creates a new ssh key using the provided email
ssh-keygen -t rsa -C "your_email@example.com"
```
Generating public/private rsa key pair.
Enter file in which to save the key (/your_home_path/.ssh/id_rsa):
第二步：输入passphrase（本步骤可以跳过）
设置passphrase后，进行版本控制时，每次与GitHub通信都会要求输入passphrase，以避免某些“失误”
Enter passphrase (empty for no passphrase): [Type a passphrase]
Enter same passphrase again: [Type passphrase again]
在github或者gitlab上输入sshkey，
cat ~/.ssh/id_rsa.pub

##### 服务器免密码登录

1. 修改本地的公钥id_rsa.pub名称为anthorized_keys，上传到服务器
2. 在服务器上，执行cd ~/.ssh， 把本地的anthorized_keys上传到服务器
3. 保存之后就行了