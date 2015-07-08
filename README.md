# fis3-vue

这个demo集成了目前前端开发比较流行的开源工具。
适用用于简单的前后端分离，移动端开发。

开发关键字：**MVVM**， **模块化**，**ES6**，**Combo**，**自动化部署**

------

包括：

  * Node.js
  * Express
  * Fis3
  * Vue
  * Sass
  * PM2
  * Gulp
  * Babel
  * Webpack
  * BrowserSync


界面和样式是直接copy腾讯CDC的idesign.qq.com

------

[点击查看demo](http://idesign.kulife.net/)

------

#### 快速开始

    // 安装fis及相关插件
    npm i -g fis3
    npm i -g fis3-hook-module
    npm i -g fis-parser-sass3
    npm i -g fis-parser-babel2
    npm i -g fis-optimizer-uglify-js
    npm i -g fis-optimizer-html-minifier
    npm i -g fis-optimizer-clean-css

    // 打包npm前端库工具
    npm i -g webpack

    // node调试工具
    npm i -g node-dev
    npm i -g node-inspector

    // 类似livereload的工具
    npm i -g browser-sync
    npm i -g browser-sync-vue

    // 发布工具
    npm i -g pm2

    // 下载项目
    git clone https://github.com/okoala/fis3-vue.git

    // 运行项目
    cd fis3-vue
    npm install
    npm run dev

    // 初始化服务器环境
    npm run setup

    // 发布项目
    npm run deploy

    // 回滚操作
    npm run revert

    // 服务器重启服务
    npm run start

------

#### 使用说明

    1. 通过package.json的components字段，可以添加指定的库。例如：
      "components": [
        "vue",
        "vue-resource",
        "vue-view"
      ]
      说明指定vue,vue-resource,vue-view,这三个为前端库。
      使用的时候可以直接require('vue'),require('vue-resource')。
      当然你需要确认库是否已经在node_modules里了。

    2. 目录结构
      │  
      ├─.dist (fis构建后文件)
      │
      ├─.tmp (webpack临时文件)
      │
      ├─build (开发，构建工具配置)
      │  ├─bs (BrowserSync配置)
      │  │
      │  ├─fis (Fis3配置)
      │  │
      │  ├─gulp (Gulp配置)
      │  │
      │  └─webpack (Webpack配置)
      │
      ├─client (非业务相关资源)
      │  │  index.html (layout文件)
      │
      ├─components
      │  ├─boot (启动相关)
      │  │  │  boot.js (启动文件，加载默认启动依赖)
      │  │  │  restApi.js (接口)
      │  │  │  routes.js (路由)
      │  │  │  
      │  │  ├─directives (指令)
      │  │  │
      │  │  ├─effects (特效)
      │  │  │
      │  │  └─filters (过滤器)
      │  │
      │  ├─c (组件)
      │  │
      │  ├─p (页面)
      │  │
      │  └─util (工具)
      │
      ├─config (项目配置)
      │
      ├─docs (文档)
      │
      └─server (Node服务相关)
      │
      └─fis-conf.js (fis3编译配置)

-----

### 截图

![](http://i1.tietuku.com/8f4dd53803c48148.png)

![](http://i1.tietuku.com/50a4afbf50a549fc.png)
