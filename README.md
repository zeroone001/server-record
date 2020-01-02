#### Mac + HomeBrew

Homebrew的安装很简单，只需在终端下输入如下指令

`ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

#### Mac + wget

`brew install wget`

#### Mac + Node

`brew install node`

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

```
#### Mac + ADB Android调试桥

```s
# install
brew cask install android-platform-tools
# 测试是否正常安装
adb devices
```

