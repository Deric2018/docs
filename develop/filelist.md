## 开发目录详解

```code
# 进入目录
└── qcloud-customer-web
    ├── .vscode               // vscode 编辑软件配置文件（只在此项目下生效）
    ├── docs                  // markdown 文档目录
    ├── http                  // mockserve 模拟请求(对接接口后无作用)
    ├── mock                  // mockserve 模拟请求(对接接口后无作用)
    ├── node_modules          // node 依赖文件包
    ├── public                // 静态资源存放目录（不会被webpack打包）
    └── src                   // 开发主目录
        ├── api               // 存放接口统一目录
        ├── assets            // 静态资源存放目录（会被webpack打包）
        ├── components        // 通用组件目录
        └── config            // 配置文件
          ├── default         // 主要分网络配置(net.config.js)、基础配置(setting...)、主题配置(theme...)三部分
          ├── config.js       // 自定义配置js文件，默认会覆盖上述三部分文件配置
          ├── permission.js   // 权限、路由拦截js
          ├── settings.js     // 导出所有配置js文件
          └── static.js       // mockjs 文件（暂无作用）
        ├── layouts           // 基础布局组件目录（写在此处的组件不用 import 引入，可在页面直接使用）
        ├── plugins           // 外部第三方 js 插件
        ├── remixIcon         // 自定义 svg 图标目录
        ├── router            // 前端所有路由（即使路由方式由后端接口返回，仍然需要在此目录下声明路由信息）
        ├── store             // vuex 状态管理目录（state，mutation，action等处理逻辑均在此目录）
        ├── styles            // 通用样式文件目录
        ├── utils             // 常用工具类方法 js
        └──  views            // vue 页面存放目录
    ├── App.vue
    ├── main.js
    ├── ...                   // babel转译、Eslint配置、git忽略等配置文件 省略...
    ├── package-lock.json     // 根据官方文档，在 `npm install`时候生成锁定安装时的包的版本号的文件
    ├── package.json          // node 项目配置文件
    ├── prettier.config.js    // 格式化插件配置文件
    ├── README.md             // reademe 介绍文档
    └── vue.config.js         // vue 3.0 开发及打包配置文件


```
