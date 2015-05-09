# ray-grunt-template
一个基于 [gruntjs](http://gruntjs.org) 及其多个插件的Web前端开发项目初始化模板，切图好帮手。

## Gulp Version
这里有一个正在开发中的[gulp 版](https://github.com/lpgray/gulp-boilerplate)

## 使用步骤
1. 安装 [nodejs](http://nodejs.org) 与 [gruntjs](http://gruntjs.com) 环境
2. `npm install -g grunt-init` 安装 `grunt-init`
3. 创建项目目录，`mkdir yourproject`
4. `git clone git@github.com:lpgray/ray-grunt-template.git`
5. 使用 ray-grunt-template，运行 `grunt-init ~/ray-grunt-template`
6. 安装依赖，运行 `npm install`
7. 运行 `grunt dev` enjoy it!

## 特性

### CSS
- 使用Less写样式，然后使用grunt-contrib-less来进行编译、合并
- 使用grunt-contrib-cssmin来进行压缩（或者直接使用grunt-contrib-less来压缩）

### JavaScript
- 使用grunt-contrib-concat进行代码合并
- 使用grunt-contrib-uglify进行代码压缩

### HTML
使用 grunt-includes 来做动态引用公共模板，能像后端动态include一样来制作前端页面。

> 在`src/html`文件夹中编辑html，最终的html是置于`src`下

### Build
- 每次build代码都会生成全新的css与js文件，以构建时间做为文件名称的一部分
- 使用process-html来替换引用部分

### Develop
- 采用更强大的 [browser-sync](https://github.com/shakyShane/browser-sync) 工具，来实现多屏同步开发，CSS自动注入无需刷新就可以看到浏览器效果，而且还能多屏幕同步操作，运行 `grunt dev` 使用此开发模式。
