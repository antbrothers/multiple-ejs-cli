# multiple-ejs-cli
node+ejs+jQuery 多页面脚手架

## 开发前景
```javascript
  要求兼容到iE6,并且有SEO需求, 市面上一些MVVM 框架都不能用，只能用比较原始的 jquery, 
  但是mvvm的开发模式实在有很爽，于是用node webpack ejs express 
  配置了一个多页面应用程序，支持模块独立开发，模块预览，模块独立调试
  技术栈: jquery webpack ejs node express 
```
## 部署介绍
```javascript
  生成静态页面部署: 1 npm run probuild
                   2 把生成的dist 拷贝到服务器上即可
  支持服务端渲染部署(把 css、html、js写入到内存): 
                  1 把项目通过ftp上传到服务器
                  2  npm install
                  3 pm2 start ./build/server.js production
"scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "devbuild": "webpack --config ./build/webpack.dev.config.js",
    "probuild": "webpack --config ./build/webpack.pro.config.js",
    "server": "node ./build/server.js development",
    "pro": "node ./build/server.js production"
  }
```
##### 全局安装 
npm install multiple-ejs-cli -g
##### 初始化项目
m-ejs init XXX
##### 安装依赖
npm install
##### 本地启动服务
npm run server
##### 测试环境打包
npm run devBuild
##### 生产环境打包
npm run proBuild
##### 模拟服务端渲染部署
npm run pro

#### 开启服务
```javascript
 首页： http://localhost:3001/
 预览：http://localhost:3001/contentpage
```


