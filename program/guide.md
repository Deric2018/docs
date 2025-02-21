## Git 上克隆项目代码

```bash
# 申请 Git 权限后 登录 [Gitlab地址](http://dev1.athenaplat.com:9099/)
# 获取 git clone 地址信息
  git clone -b +分支 + 地址

# 下载 git 客户端进行操作  tortoisegit（windows）  Tower、Fork（Mac）

  第一步：创建本地分支
  点击右键选择TortoiseGit，选择Create Branch…，在Branch框中填写新分支的名称（若选中”switch to new branch”则直接转到新分支上，省去第二步），点击OK按钮：

  第二步：通过“Switch/Checkout”切换到新创建的分支上，点击OK：

  第三步：在新分支下执行PUSH操作，在对话框中保持远程分支为空白，点击OK，则将在远程创建了新的分支（在PUSH的时候远程服务器发现远程没有该分支，此时会自动创建一个和本地分支名称一样的分支，并将本地分支的内容上传到该分支）。

  第四步：其他成员切换该新分支：
  首先进行pull操作， 然后进行切换分支（如第二步）

  第五步：分区合并
  进行分支合并之前我们需要明确哪个分支将要合并到哪个分支，首先通过“Switch/CheckOut”切换到主干分支（如develop分支）,然后通过“Merge”继进行合并操作，在对话框中选择需要合并的分支。
  分支合并成功后，我们即可以通过Commit与PUSH操作将合并上传到中心服务器。

  第六步：删除分支
  当我们已将新分支合并到主分支后，或者放弃该分支的时候，可以对该分支进行删除操作。
  首先通过“CheckOut/Switch”打开对话框，点击Switch to区域中Branch条目后面的更多按钮，打开分支列表对话框，右键点击要删除的分支，选择delete branch进行删除。
  注意，在删除远程分支的时候，本地分支并不会删除，这也说明了本地分支与远程分支并无从属关系

```

## 前端代码开发

**1.开发工具（Vscode & HbuilderX）**

- 进入 vscode 官网下载 vscode

- 汉化 vscode

  中文插件 Chinese(simplified) 重新安装一遍，然后重启 vscode 即可
  如果重启 vscode 后还是英文的，按 f1 搜索 Configore Display Language 设置 zh-cn 关闭软件重启，

- 安装插件 Prettier - Code formatter

  为保证代码规范统一，配置了 Eslint + Prettier，实现在 Vscode 中保存时自动格式化代码

- 更多 vscode 使用技巧请查看软件自带说明文档或官网查询

> **_PS：PC 端开发使用 Vscode [官网](https://code.visualstudio.com/)，APP 开发使用 Hbuilder X [官网](https://www.dcloud.io/)_**

**2.前端项目启动**

```bash
# 进入项目目录
cd qcloud-customer-web

# 安装依赖
npm install

# 本地开发 启动项目
npm run serve
```

**3.查看开发文档**

```bash
# 全局安装 docsify
npm install docsify-cli@4.4.3 -g

# 进入项目目录
cd qcloud-customer-web

# 运行文档服务
npm run doc  || docsify serve docs

```

参考：[docsify 文档](https://docsify.js.org/) &nbsp;&nbsp;&nbsp; [Markdown 基本语法](https://www.jianshu.com/p/191d1e21f7ed/)

## 接口地址配置

```bash
# 进入目录
└── src
    ├── ...
    └── config
        ├── default
        ├── config.js
        ├── permission.js
        ├── settings.js
        └── static.js
    ├── ...


# 打开 config.js

// 配置成自己需要的接口地址
const urlObj = {
  /** 开发环境连接地址 可以修改为开发人员ip地址 */
  development: "http://dev1.athenaplat.com:8099/api",

  /** 114测试环境 自动发布连接地址  @extends { 请勿随便修改 } */
  test: "http://dev1.athenaplat.com:8099/api",

  /** 119正式环境连接地址  @extends { 请勿随便修改 } */
  production: "http://119.3.162.214:19093/api",

};

# 其他配置 详见 前端开发-目录详解

```
