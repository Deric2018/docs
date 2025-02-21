### 接口地址配置

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

### 封装请求

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
