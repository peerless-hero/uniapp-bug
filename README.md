# darkmode-bug

本项目用于演示个人发现到的uniapp相关的bug。

## 项目来源

项目源码基础来源于官方提供的脚手架项目。

地址：[https://zh.uniapp.dcloud.io/quickstart-cli.html#%E5%88%9B%E5%BB%BAuni-app](https://zh.uniapp.dcloud.io/quickstart-cli.html#%E5%88%9B%E5%BB%BAuni-app)

## 项目安装

```bash
yarn install
```

自行申请调试证书，修改src/manifest.json内"app-harmony"的相关鸿蒙配置。

## bug描述

使用HBuildX5.04正式版启动本项目，深色模式样式失效，且无法监听主题切换。

将HBuildX回退到4.87版本，深色模式一切正常。
