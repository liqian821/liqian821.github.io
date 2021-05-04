# 在Mac下安装Enterprise Architect

参考：https://sparxsystems.com/enterprise_architect_user_guide/15.2/product_information/enterprise_architect_macos.html

## 安装wine

### 安装homebrew

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### 安装XQuartz

``` bash
brew install --cask xquartz
```

### 安装wine

```bash
brew tap homebrew/cask-versions
brew install --cask --no-quarantine wine-stable
```

在64位系统，将wine的软链接指向wine64

```bash
zhaolus-iMac:Downloads zhaolu$ ll /usr/local/bin/wine
lrwxr-xr-x  1 zhaolu  admin  62  4 24 12:02 /usr/local/bin/wine@ -> /Applications/Wine Stable.app/Contents/Resources/wine/bin/wine
zhaolus-iMac:Downloads zhaolu$ ll /usr/local/bin/wine64 
lrwxr-xr-x  1 zhaolu  admin  64  4 24 12:02 /usr/local/bin/wine64@ -> /Applications/Wine Stable.app/Contents/Resources/wine/bin/wine64
zhaolus-iMac:Downloads zhaolu$ rm -rf /usr/local/bin/wine
zhaolus-iMac:Downloads zhaolu$ ln -s /Applications/Wine\ Stable.app/Contents/Resources/wine/bin/wine64 /usr/local/bin/wine
zhaolus-iMac:Downloads zhaolu$ ll /usr/local/bin/wine
lrwxr-xr-x  1 zhaolu  admin  64  4 24 12:37 /usr/local/bin/wine@ -> /Applications/Wine Stable.app/Contents/Resources/wine/bin/wine64
```

安装完成后通过执行wineconsole就可以使用wine Terminal window

### 安装运行依赖库

使用win

