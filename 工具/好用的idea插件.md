# IDEA插件

## GitToolBox

### 一、插件介绍

git工具箱，提供各种git操作。

其中比较方便的是可以即时看到每一行代码的blame

![image-20210404210657765](好用的idea插件.assets/gittoolbox1.png)

### 二、安装方式

使用IDEA下载安装

![image-20210404210955599](好用的idea插件.assets/gittoolbox2.png)

### 三、使用方式

通过以下配置

![image-20210404211251793](好用的idea插件.assets/gittoolbox3.png)



# PlantUML integration

### 一、插件介绍

PlantUML在Idea中的插件，PlantUML是一种高效绘制UML图的工具，官网：https://plantuml.com/zh/

### 二、安装方式

idea中下载，其中PlantUML Parser可以转换类图为PlantUML，PlantUML Syntax Check可以检查语法

![image-20210426224807751](好用的idea插件.assets/image-20210426224807751.png)

### 三、使用方式

1. 下载Graphviz dot

官网：http://www.graphviz.org/

使用homebrew安装：

``` bash
brew install graphviz
```

2. 配置Graphviz dot路径

* 执行which dot获取dot路径

```bash
which dot
/usr/local/bin/dot
```

* 在bash_profile中export环境变量

``` bash
export GRAPHVIZ_DOT=/usr/local/bin/dot
```

* source环境变量
* 在IDEA的plantuml界面点击设置，勾选 Use GRAPHVIZ_DOT

![image-20210426225644769](好用的idea插件.assets/image-20210426225644769.png)

* 重启IDEA后生效。

## 插件名称

### 一、插件介绍

### 二、安装方式

### 三、使用方式