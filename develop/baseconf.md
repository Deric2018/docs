#### 地址配置

```code
const urlObj = {
  /** 开发环境连接地址 可以修改为开发人员ip地址 */
  development: "http://dev1.athenaplat.com:8099/api",

  /** 114测试环境 自动发布连接地址  @extends { 请勿随便修改 } */
  test: "http://dev1.athenaplat.com:8099/api",

  /** 119正式环境连接地址  @extends { 请勿随便修改 } */
  production: "http://119.3.162.214:19093/api",

};
```

#### 各客户标题/Logo/图标

```code
# 通用变量配置
# 内网IP
VUE_APP_NW = ''
# 浏览器ico图标
VUE_APP_FAVICON = 'favicon.ico'
# 项目标题名称
VUE_APP_TITLE = '雅典娜'
# 项目LOGO
VUE_APP_LOGO_IMG = 'logo-ydn.png'
# 登录页顶部图片
VUE_APP_LOGIN_TOP_IMG = 'login-top-ydn.png'

```

#### 封装请求

```code

import { getAction, postAction } from "@/api/apiManage";

//post请求
postAction("地址", {参数}).then((res) => {
    if (res.code === 200) {
    console.log(res);
    }
});
//get请求
getAction("地址", {参数}).then((res) => {
    if (res.code === 200) {
    console.log(res);
    }
});

```
