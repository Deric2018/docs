> # 雅典娜项目说明文档

## Git 地址

| 名称          | Git 地址                                                            | 分支名称                                |
| ------------- | ------------------------------------------------------------------- | --------------------------------------- |
| Customer 前端 | http://dev1.athenaplat.com:9099/qtmw/qcloud/qcloud-customer-web.git | 新版： /upgrade-yadianna 旧版：yadianna |
| Admin 前端    | http://dev1.athenaplat.com:9099/qtmw/qcloud/qcloud-admin-web.git    | yadianna                                |
| APP 前端      | http://dev1.athenaplat.com:9099/qtmw/qcloud/qcloud-app-server.git   | yadianna                                |
| APP 后端      | http://dev1.athenaplat.com:9099/qtmw/qcloud/qcloud-app-server.git   | master-athenaplat                       |
| customer 后端 | http://dev1.athenaplat.com:9099/qtmw/qcloud/qcloud-customer.git     | master-athenaplat                       |
| admin 后端    | http://dev1.athenaplat.com:9099/qtmw/qcloud/qcloud-admin.git        | master-athenaplat                       |

## 部署信息（114）

| 标题           | 114 部署地址                                                                             | 账号 | 密码       |
| -------------- | ---------------------------------------------------------------------------------------- | ---- | ---------- |
| 雅典娜旧版地址 | http://dev1.athenaplat.com:18096                                                         | htya | zyyt123abc |
| 新版地址       | http://dev1.athenaplat.com:18098                                                         |      |            |
| admin 管理端   | http://dev1.athenaplat.com:18097                                                         |      |            |
| 墨刀原型       | https://modao.cc/app/krtyet5clynntz?simulator_type=device&sticky=#screen=skrkpmdkoyz76ye |      |            |
| H5 地址        | http://m.athenaplat.com/                                                                 |      |            |

| 标题          | 正式服务部署地址           | 接口路径 | 账号 | 密码 |
| ------------- | -------------------------- | -------- | ---- | ---- |
| admin 前端    | http://119.3.162.214:19090 |          |      |      |
| admin 后端    | http://119.3.162.214:19092 |          |      |      |
| customer 前端 | http://119.3.162.214:19091 |          |      |      |
| customer 后端 | http://119.3.162.214:19093 |          |      |      |
| job           | http://119.3.162.214:19094 |          |      |      |
| apk 包        | http://119.3.162.214:19095 |          |      |      |
| app 后台      | http://119.3.162.214:19097 | appv1.x  |      |      |

## SVN 地址

| 名称         | SVN 总地址                     | 雅典娜文件目录地址 |
| ------------ | ------------------------------ | ------------------ |
| 114 SVN 地址 | svn://dev1.athenaplat.com:8089 | /qcloud/雅典娜平台 |

## Git 权限申请

- 准备姓名、常用邮箱等信息
- 申请项目的名称或 git 分支地址信息
- 提供以上信息给管理员，等待权限分配
- 权限分配完成后可登录[Gitlab 地址](http://dev1.athenaplat.com:9099/)查看详细信息

  > **_PS：第一次登录需要设置密码_**

## Git 常用命令

---

![Git命令速查表](https://note.youdao.com/yws/api/personal/file/WEB32db9bbd347224e945f1839d1b5397b7?method=download&shareKey=5de97be6256f3e9e1246bf0a2b405a4b "Git命令速查表")

**git 常用命令**

```
查看各个分支当前所指的对象 git log --oneline --decorate
项目分叉历史 git log --oneline --decorate --graph --all
分支创建 git branch testing
分支切换 git checkout testing
创建加切换 git checkout -b testing
分支都会向前移动一步 git commit -m "A" (ABCD....)
创建分支 git checkout dev
代表切换分支 git checkout -b dev
查看当前分支 git branch
提交分支 git add readme.txt
创建分支下的分支 git commit -m "d" (git commit -m “branch test”)
把分支移到主分支上 git checkout master
合并分支 git merge dev
删除分支 git branch -d dev
```
