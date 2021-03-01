# Qt5.15_example
Qt5.15 examples for testing.

## 本环境基于Qt5.15.0构建，分为以下部分。
qt5.15_lib.tar.gz - Qt5.15.0交叉编译生成库  
examples.tar.gz   - Qt样例程序  
dispInit.tar.gz	  - 初始化disp和panel样例程序  
qt_test.tar.gz	  - Qt样例程序运行环境  

## 构建过程  
### 环境准备
Qt5下载地址：<http://download.qt.io/>

### 目录结构说明
| 目录 | 说明 |  
| :---- | :---- |  
| archive | 各种Qt开发工具安装包，包含新旧版本，可以下载开发工具和源码 |  
| community_releases | 社区定制的Qt库，Tizen版Qt以及Qt附加源码包 |
| development_releases | 开发版，包含新的和旧的不稳定版本，在Qt开发过程中的非正式版本 |
| learning | 有学习Qt的文档教程和示范视频 |
| ministro | Mini版本，目前是针对Android的版本 |
| official_releases | 正式发布版，是与开发板相对的稳定版Qt开发库和开发开发工具，可以下载开发工具和源码 |
| online | Qt在线安装源 |
| snapshots | 预览版，最新的开发测试中的Qt库和开发工具 |

当前环境使用archive Qt5.15.0版本。
<http://download.qt.io/archive/qt/5.15/5.15.0/single/qt-everywhere-src-5.15.0.tar.xz.mirrorlist>

## Qt5交叉编译
本例使用toolchain: gcc-arm-8.2-2018.08-x86_64-arm-linux-gnueabihf编译qt5。编译依赖perl5.8或以上版本，python2.7或以上版本。要支持使用触摸还需要链接tslib库。  
下载toolchain gcc-arm-8.2-2018.08-x86_64-arm-linux-gnueabihf.tar.xz：  
<https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-a/downloads>  

### 设置环境变量：  
vim /etc/profile 添加toolchain路径：**export PATH=/opt/toolchain/gcc-arm-8.2-2018.08-x86_64-arm-linux-gnueabihf/bin:$PATH**
