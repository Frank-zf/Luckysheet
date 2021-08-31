Luckysheet本地开发项目，详见README-OKR.md

原项目git地址：https://github.com/mengshukeji/luckysheet

目前PC-web项目中白板模块中的表格用的就是这个代码

使用方法：
### Installation
```
npm install
npm install gulp -g
```
### Development
```
npm run dev
```
### Package
```
npm run build
```

### 本地开发
需要用外链加载此项目中的打包后dist目录下的文件


主要是一下两个js文件和四个css文件

/plugins/js/plugin.js
/luckysheet.umd.js

/plugins/css/pluginsCss.css
/plugins/plugins.css
/css/luckysheet.css
/assets/iconfont/iconfont.css

这里需要使用代理工具，例如：LightProxy

### 代理配置参考：

https://local.test-okr-hrec.worktrans.cn:8081/server  http://localhost:3000

https://local.test-okr-hrec.worktrans.cn:8081/forward_webfront/api/okr-white/web/console/excel/load  https://test-okr-hrec.worktrans.cn/forward_webfront/api/luckysheet/api/load

https://local.test-okr-hrec.worktrans.cn:8081/forward_webfront/api/okr-white/web/console/excel/loadsheet   http://192.168.70.119:9004/luckysheet/api/loadsheet

同理，websocket地址也需要代理。

wss://test-okr-hrec.worktrans.cn/forward_webfront/api/luckysheet/websocket/luckysheet  ws://192.168.70.119:9004/luckysheet/websocket/luckysheet

192.168.70.119:9004为后端提供的ip和端口号

### 测试&生产环境
将build后的dist文件夹拷贝到 https://cdnstyle.woqukaoqin.com/okr_excel下

在需要用到的组件中去引入

luckysheet.umd.js体积较大，建议压缩后替换

