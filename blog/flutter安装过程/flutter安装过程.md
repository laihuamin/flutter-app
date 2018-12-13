### vscode安装flutter插件

在插件中搜索flutter，安装flutter

### 下载flutter sdk

1、官网下载flutter sdk
2、下载完之后解压sdk
3、添加sdk配置

```
// 编辑配置文件
vim ./.bash_profile
// 配置环境变量路径
export PATH=/Users/laihuamin/Documents/flutter/bin:$PATH
// 配置国内镜像源
export PUB_HOSTED_URL=https://pub.flutter-io.cn
export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn
```

4、验证环境变量是否配置成功

```
flutter -h
```

### 安装android sdk

1、安装android studio及android sdk
2、检测安卓环境是否ok

```
flutter doctor
```

3、出现的问题

```
! Some Android licenses not accepted.  To resolve this, run: flutter doctor --android-licens
```
需要运行

```
flutter doctor --android-licenses
```
之后一直按y就行了

### 安装ios sdk

```
Xcode installation is incomplete; a full installation is necessary for iOS development.
      Download at: https://developer.apple.com/xcode/download/
      Or install Xcode via the App Store.
      Once installed
```
运行

```
sudo xcode-select --switch /Applications/Xcode.app/Contents/Developer
```

```
libimobiledevice and ideviceinstaller are not installed. To install with Brew, run:
```
需运行

```
 brew update
 brew install --HEAD usbmuxd
 brew link usbmuxd
 brew install --HEAD libimobiledevice
 brew install ideviceinstaller
```

```
ios-deploy not installed
```
运行
```
brew install ios-deploy
```

```
CocoaPods not installed.
```

运行

```
brew install cocoapods
pod setup
```