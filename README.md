 
# Harvard Middle School
## listen1 网页版安装 (Chrome Extension) V2.26.1

（最后更新于 2022 年 09 月 10 日）

[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg)](LICENSE)

[English Version](https://github.com/listen1/listen1_chrome_extension/blob/master/README_EN.md)

## 缘起

当我发现找个想听的歌因为版权听不了，需要打开好几个网站开始搜索，来回切换让我抓狂的时候，我知道是时候该做点什么了。

妈妈再也不用担心我找不到我想听的歌了。

支持音乐平台

- 网易云音乐
- QQ 音乐
- 酷狗音乐
- 酷我音乐
- bilibili
- 咪咕音乐
- 千千音乐

搜歌，听歌，就用 `Listen1`。

[![imgur](https://i.imgur.com/dIVFtor.gif)]()

V2.9.0 新特性：自动切换播放源(Beta)

当一首歌的播放源不可用时，会自动搜索其他平台，获得可用的播放源。避免了用户手动搜索的麻烦。

还有精选歌单哦。

## 官方商店安装（推荐）

按你的浏览器类型点击下面的链接安装

- [Chrome Web Store 安装](https://chrome.google.com/webstore/detail/listen-1/indecfegkejajpaipjipfkkbedgaodbp)
- [FireFox 安装](https://addons.mozilla.org/zh-CN/firefox/addon/listen1/)
- [Microsoft Edge 安装](https://microsoftedge.microsoft.com/addons/detail/hneiglcmpeedblkmbndhfbeahcpjojjg)

感谢 [@TNT-c](https://github.com/TNT-c) 维护 Firefox 的发布渠道

感谢 [@dhxh](https://github.com/dhxh) 维护 Microsoft Edge 的发布渠道

## Chrome 下载安装

1. 下载项目的 zip 文件，在右上方有个 `Download ZIP`, 解压到本地

2. chrome 右上角的设置按钮下找到更多工具，打开`扩展程序`

3. 选择 `加载已解压的扩展程序`(如果没有显示先选中`开发者模式`)，选中解压后的文件夹，完成！

## Firefox 打包安装

1. 将根目录下 manifest_firefox.json 替换 manifest.json

2. `cd listen1_chrome_extension`

3. `zip -r ../listen1.xpi *`, 完成打包 xpi 文件

4. 打开 Firefox，加载 xpi 文件，完成安装

## Listen1 Mobile V0.8.1

[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg)](LICENSE)

## 简介

一款支持多平台音乐播放和搜索的移动音乐 App。现有版本已支持网易云音乐，QQ 音乐，虾米音乐。还有丰富的歌单管理功能。使用 React Native 开发，基于 MIT 协议开源免费。

**支持 iOS 和 Android 平台**

[![imgur](https://i.imgur.com/zYyaK92.png)]()

## 特性

- 一个 App 播放多平台的音乐
- 搜索多平台音乐
- 浏览，播放多平台歌单
- 收藏音乐到自建歌单
- 夜间模式
- 备份，恢复(支持从`Listen1 chrome extension`导入数据)

## 下载

Github 主页下载： https://listen1.github.io/listen1

[<img src="https://fdroid.gitlab.io/artwork/badge/get-it-on.png"
    alt="Get it on F-Droid"
    height="80">](https://f-droid.org/packages/com.listen1.app)

## 安装

### iOS

iOS 只支持编译安装，请拥有开发者证书的开发者连接 iPhone 后，将项目文件中的证书换成自己的证书，然后执行命令安装。

### Andriod

下载 apk 安装, apk 下载地址请访问[项目 release 页面](https://github.com/listen1/listen1_mobile/releases)

## 编译

开发环境

- Java 8 JDK （更高版本需更新默认 gradle 版本）
- Nodejs 8 （版本>12.10.0 可能遇到 metro 一个关于正则表达式的 bug 导致的启动失败）
- Android Studio (Android SDK 版本 v28)

编译步骤

- Clone 或下载本项目代码
- `yarn` 安装依赖
- `yarn run link` 链接 React Native 的依赖库
- `yarn start:ios` 将在 iOS 模拟器上运行项目
- `yarn start:android` 将在安卓真机或模拟器（取决于手机是否连接）运行项目

Apk 打包

```
   cd .\android\
   ./gradlew assembleRelease
   react-native run-android --variant=release

```

更详细的打包信息（包括生成 keystone）

https://reactnative.cn/docs/signed-apk-android

## 代码基本结构

- api: 音乐平台相关资源 API
- asset: 图片等资源
- components: 可复用的组件
- views: 业务相关的 screen 组件
- modules: 组件使用的自定义函数库
- redux: redux 需要的 action 和 reducer 函数
