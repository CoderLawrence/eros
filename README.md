### Intro
eros 是基于 [weex](https://weex-project.io/cn/) 封装面向前端的 vue 写法的解决方案，由于 app 开发的特殊性，eros 则更偏重关心于整个 app 项目。

#### 优势：
* eros 对 weex 官方进行二次封装，能及时跟进 weex 的新特性，
* eros-cli 支持生成开发模板，更新平台相关依赖，打包等，在熟悉了 eros 之后，对于中小型 app 应用能进行快速迭代。
* eros-cli 和 eros-publish 的搭配使用，可以搭建简易增量发布。
* 在开发中能更少的关注 weex 版本升级和本身的兼容性问题。**（综合在一个平台，当你遇到一个兼容性问题，当 eros 修复了，就是其他人少遇到一个问题，节约的是大家的时间）**。
* 跟 weex 一样，给 vue 开发者另一个舞台。

#### 不足：
* weex debug 会出现些问题，eros 已经有方法解决，但不完美，还需要改进。
* 由于人手不足，许多功能可能并不完善，修复可能需要大家的参与。
* 由于 eros 本身是从公司业务冲抽离出来的，有些代码冗余和不规范。
eros 会尽全力弥补不足。

#### 功能：

* 客户端拓展了数十个 module
* 提供 appboard 机制来减少包体积
* 内置了一套完整的 widget ，可根据业务自行修改
* eros-publish 提供了服务器端增量发布更新逻辑
* eros init 生成开发模板
* eros dev 启动服务进行实时开发效果查看和 debug 调试
* eros install 更新开发平台所需 eros 依赖
* eros pack 打对应平台内置包
* eros build 支持生成全量包，增量包，并内置与更新服务器交互逻辑
* eros update 同步更新模板内容
* 支持 vue、sass、stylus、less、babel
* 支持 weex 的 vue 入口式开发和 js 入口式开发
* 等等...

## Required
开发之前您需要学习 weex 知识，并且能熟练使用 vue 开发，文档地址如下。
* [weex](http://weex.apache.org/cn/guide/)
* [vue](https://cn.vuejs.org/v2/guide/)
## Docs
* [eros v1](https://karynsong.gitbooks.io/weex-eros/content/)
* eros v2 (building...)
## Support 
> 跟随着 weex 的支持性，`但目前我们并不支持开发代码兼容 web 端`

* Android 4.1 (API 16)
* iOS 8.0+ 
* WebKit 534.30+ 

## Environment
以下为不同 OS 开发不同客户端所需环境。
#### 脚手架所需环境:
darwin: 
* Node.js (>=6.x), npm version 4+ 
* Python 2，并配置到环境变量中

windows: 
* Git bash 
* Python 2，并配置到环境变量中。
* .NET Framework 2.0 SDK 或以上 （Window 10 安装4.0及以上）
* Microsoft Visual Studio 2005 或以上

#### 脚手架安装:
```
$ npm i eros-cli -g
```
如果你在中国地区，我们还是推荐您使用 [cnpm](https://npm.taobao.org/) 安装
```
$ cnpm i eros-cli -g 
```
#### darwin 开发 iOS:
* Xcode
* CocoaPods
    * 升级 Ruby 环境：`$ sudo gem update --system`
    * 移除现有 Ruby 镜像：`$ gem sources --remove https://rubygems.org/`
    * 添加ruby-china镜像：`$ gem source -a https://gems.ruby-china.org/`
    * 安装 CocoaPods：`$ sudo gem install cocoapods`
    * 如果以上命令报错则执行：`$ sudo gem install -n /usr/local/bin cocoapods --pre`
    * 最后执行：`$ pod setup 过程比较漫长，请耐心等待执行完成`

#### darwin 开发 Android:
* 下载并安装 [JDK](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)。
* 下载并安装 [Android Studio](https://developer.android.google.cn/studio/index.html)。
#### windows 开发 Android
* 下载并安装 [JDK](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)。
* 下载并安装 [Android Studio](https://developer.android.google.cn/studio/index.html)。

> 如果您使用虚拟机进行跨平台开发，也需要配置好对应平台的所需环境。

## Start
1. 首先通过脚手架自动生成开发模板(我们不推荐用sudo来执行脚手架的任何指令)
```
$ eros init
```
按提示选择模板，填写 app/项目名称和版本后在当前路径下会生成对应模板，然后 `cd` 到项目中

2. 下载所需依赖
```
$ npm install
$ eros install
```
3. 安装完依赖之后:
* iOS: 会自动打开 `Xcode` ，然后选择一个模拟器，点击左上角的播放(运行)按钮，即可看到内置包中已经内置好的 eros demo.
* Android: writing...

## Developing and debugging
(building...) 具体请查看文档

## Ecosystem
| Project | Description |
|---------|-------------|
| [eros-cli](https://github.com/bmfe/eros-cli) | 简单的 eros 项目构建工具，可以提供搭建，开发，调试和发布等功能。 |
| [eros-publish](https://github.com/bmfe/eros-publish) | 简单的服务器差分包更新逻辑，需要和脚手架搭配使用。 |

