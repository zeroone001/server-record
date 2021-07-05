#### Mac + HomeBrew

Homebrew的安装很简单，只需在终端下输入如下指令

`ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

#### Mac + wget

`brew install wget`

#### Mac + Node

PS： 不要用brew装，直接去官网下载

```s
sudo xcode-select -s /Applications/Xcode.app/Contents/Developer
xcodebuild -license
```

#### Mac + npm

```s
npm install -g npm@6.9.0

# 这个时候出现了一个问题, 解决方案

cd /usr/local/Cellar/node/13.5.0/lib/node_modules/npm/

# 复制里面的文件，到下面的路径
cd /usr/local/lib/node_modules/

# NPM 全局安装的依赖放置位置
/usr/local/lib/node_modules/

```
#### Mac + ADB Android调试桥

```s
# install
brew cask install android-platform-tools
# 测试是否正常安装
adb devices
```
#### Mac + chrome
```s
open -n /Applications/Google\ Chrome.app/ --args --disable-web-security  --user-data-dir=/Users/smzdm/MyChromeDevUserData/
```
#### shell

[Linux command](http://linuxcommand.org/index.php)

#### sourceTree 密码总是自动改的问题解决

* 密码过期处理
* 钥匙链。忘记密码
* 访达-前往-文件夹- ~/Library - Application Support - SourceTree

#### V


### 测试一下access Token 2