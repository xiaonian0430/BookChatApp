# ShareKnowApp

![](static/images/logo.png)

通用书籍阅读 APP，[ShareKnowApp](https://github.com/xiaonian0430/ShareKnowApp) 的 `uni-app` 实现版本，支持多端分发，编译生成 Android 和 iOS 手机APP以及各平台的小程序。

使用`ShareKnowApp`，您可以轻松地将您的电子书、文档手册和在线书籍分发到各个小程序平台，以及编译生成手机APP发布到各大手机软件市场供用户下载和使用。


## APP 体验

目前 `ShareKnowApp` 已经打包编译生成的 Android 和 iOS 手机APP，您可以直接下载体验和感受下。

APP下载体验地址： https://sk.showcm.top/app


## 设计开发

`ShareKnowApp`中对HTML内容的渲染，经过多次对性能和渲染效果体验的对比，最终没有采用网上开源的第三方渲染组件，直接使用了`uni-app`自带的`rich-text`组件，而将`ShareKnowApp`编译成各平台的小程序的时候，同样也是用了各小程序平台的`rich-text`组件。


## 特点

- 开源：基于 Apache 2.0 开源协议进行开源，对商业友好
- 秀气：简洁、美观，给您焕然一新的视觉体验，让你都不敢相信这是一个擅长后端的程序员设计和开发实现的
- 丰富：注册、登录、搜索、书架、书签、阅读偏好设置等功能齐全，麻雀虽小，五脏俱全
- 强大：尽管`ShareKnowApp`使用的是混合开发，但是编译生成的手机App以及各平台的小程序，性能和体验也没见得真比原生的差


### 后端程序

`ShareKnowApp`的配套后端程序是 `ShareKnow`。

**ShareKnow 开源地址**

- Gitee: https://gitee.com/xiaonian0430/ShareKnow
- GitHub: https://github.com/xiaonian0430/ShareKnow

**ShareKnow 官网**

共享知识： https://sk.showcm.top


### 二次开发基本步骤

1. 安装部署`ShareKnow`
1. 克隆下载`ShareKnowApp`源码
1. 使用`HBuilderX`打开项目文件夹
1. 将下载程序中的`config.example.js`文件重命名为`config.js`文件
1. 根据自己的开发环境，设置`host`配置项

> 如果是在开发环境，请把`debug`设置为true，编译生成生产程序的时候，把`debug`设置为false


## 程序页面

- [x] 目录页            /pages/menu/menu
- [x] 书籍阅读页         /pages/read/read
- [x] 用户中心页         /pages/ucenter/ucenter
- [x] 首页              /pages/index/index
- [x] 分类页            /pages/cate/cate
- [x] 书架页            /pages/bookshelf/bookshelf
- [x] 列表页            /pages/list/list
- [x] 个人主页          /pages/me/me
- [x] 书签页            /pages/bookmarks/bookmarks
- [x] 搜索结果页         /pages/search/search
- [x] 内容点评页         /pages/comment/comment
- [x] 404页            /pages/notfound/notfound
- [x] 登录页            /pages/login/login
- [x] 注册页            /pages/register/register
- [x] 书籍介绍页         /pages/intro/intro


## 开源协议

Apache v2.0
