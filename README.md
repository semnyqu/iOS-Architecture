# iOS架构

## 目录

* [代码规范](#style_guide)
* [项目架构(MVC)](#project_architecture)
* [工具](#tools)
* [引用第三方开源项目](#quote_third_OSS)


<a name="style_guide"></a>
## 代码规范

### 1. [Objective-C](https://github.com/WithoutEvil/objective-c-style-guide)
### 2. [Swift](https://github.com/WithoutEvil/swift-style-guide)

<a name="project_architecture"></a>
## 项目架构(MVC)

### 1. Model

目前项目所用框架:[JSONModel](https://github.com/icanzilb/JSONModel)，
类似框架:[Mantle](https://github.com/Mantle/Mantle)

### 2. View

代码编写UI所用AutoLayout库: [Masonry](https://github.com/SnapKit/Masonry)

#### 特点

1. 优势：可以设置约束优先级
2. chain式语法
3. update、remake约束
4. 也有swift版本项目[SnapKit](https://github.com/SnapKit/SnapKit)

项目早期也使用过[PureLayout](https://github.com/PureLayout/PureLayout)，但和[Masonry](https://github.com/SnapKit/Masonry)相比，虽然语法工整了一些，但是还是毫无置疑地使用[Masonry](https://github.com/SnapKit/Masonry)


<a name="tools"></a>
## 工具

### 1. Git

#### 1. Git学习：
* 教程：http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000

* 进阶教程：http://git-scm.com/book/zh/v1

* git及相关gui工具下载地址：http://git-scm.com/

#### 2. Git Team

* 写出好的 commit message
https://ruby-china.org/topics/15737

* Git分支管理是一门艺术
http://roclinux.cn/?p=2129


<a name="quote_third_OSS"></a>
## 引用第三方开源项目

###1. submodule
引用第三方开源项目的一种方式
#### 如何checkout相关的submodule的代码  

`checkout submodule project source:`  

1. `git submoule init`: initialize your local configuration file 

2. `git submodule update`: fetch all the data and check out the appropriate commit listed in your superproject

#### add an existing Git repository as a submodule of the repository that we’re working on

1. `git submodule add https://github.com/demo/demo`

摘自: https://git-scm.com/book/en/v2/Git-Tools-Submodules

###2. cocoapods
引用第三方开源项目的一种方式

Search for pods (above). Then list the dependencies in a text file named Podfile in your Xcode project directory:

```
platform :ios, '8.0'
use_frameworks!

target 'MyApp' do
  pod 'AFNetworking', '~> 2.6'
  pod 'ORStackView', '~> 3.0'
  pod 'SwiftyJSON', '~> 2.3'
end
```

Tip: CocoaPods provides a `pod init` command to create a Podfile with smart defaults.   
####1. Now you can install the dependencies in your project:
```shell
$ pod install
```
####2. Make sure to always open the Xcode workspace instead of the project file when building your project:
```shell
$ open App.xcworkspace
```
####3. Now you can import your dependencies e.g.:
```shell
Now you can import your dependencies e.g.:
```
摘自: https://cocoapods.org/ 中 `GET STARTED`

