# 微信小程序开发教程示例

> 一个微信小程序（应用号）开发示例（豆瓣电影）https://github.com/zce/weapp-demo

## 我学习到的
微信小程序」的背后运行的是一个名为MINA框架。

### Transform wxml和wxss
当我们修改完WXML、WXSS的时候，我们需要重新编译项目才能在浏览器上看到效果。这时候后台就会执行一些**transform**动作：
1. wcc来转换wxml为一个genrateFun，执行这个方法将会得到一个virtual dom
2. wxss就会转换wxss为css。

## 完整示例特点

- app.json文件：每个新页面都需要在其中进行注册，tabBar也是在这里进行注册，同时定义一些全局样式。
- 每个页面都由.js（controller）,.json（配置）,.wxss（样式）和.wxml（模板）组成。
- 页面的.js文件中，可以定义页面scope的数据，以及page的生命周期函数
- 模板由这些标签组成：view,text,image,button 等等
- 样式中，像素的单位为rpx
- 可以定义template模板
- 整体感觉跟vue.js很像


## 运行指南

```bash
$ cd path/to/root
$ git clone git remote add origin https://github.com/guanyuan/wechat-app-douban-movie.git [project-name] --depth 1
$ cd [project-name]
$ npm install
$ npm run build
$ npm run watch
```
then, open `dist` in wechat devtools
