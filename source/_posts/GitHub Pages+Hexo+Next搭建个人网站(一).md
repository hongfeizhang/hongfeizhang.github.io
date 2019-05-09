---
title: GitHub Pages+Hexo+Next搭建个人网站(一)
date: 2019-05-08 17:15:32
categories: 建站
tags: Hexo|Next
---
# 简单记录一下建站过程

### GitPages Hexo Next

[GitHub Pages](https://pages.github.com/)是一种静态站点托管服务，旨在直接从GitHub存储库托管个人，组织或项目页面。

[Hexo](https://github.com/hexojs/hexo)是一个快速、简洁且高效的静态博客站点生成框架。

[Next](https://github.com/theme-next/hexo-theme-next)是Hexo框架一个非常好用的主题。

### 创建GitHub存储库

登录GitHub，Create a new repository。

![](https://raw.githubusercontent.com/hongfeizhang/Image-Hosting/master/20190509135759.png)

Repository name为''用户名.github.io'。

![](https://raw.githubusercontent.com/hongfeizhang/Image-Hosting/master/20190509135858.png)



### 安装Node.js和Git

- [Node.js](http://nodejs.org/)
- [Git](http://git-scm.com/)

安装后可以看到软件版本。

```bash
$ git --version
git version 2.21.0.windows.1

$ npm --version
6.9.0
```

### [安装Hexo](https://hexo.io/docs/index.html)

执行命令。

```bash
npm install -g hexo-cli
```

hexo安装后，执行。\<folder\>是需要创建的网站目录。

```bash
hexo init <folder>
cd <folder>
npm install
```

安装后的目录结构。

```
.
├── _config.yml
├── package.json
├── scaffolds
├── source
|   ├── _drafts
|   └── _posts
└── themes
```

创建测试页面

```
hexo new testpage
hexo generate

hexo server
INFO  Start processing
INFO  Hexo is running at http://localhost:4000 . Press Ctrl+C to stop.

```

访问http://localhost:4000 ，即可看到测试页。

然后，在配置文件_config.yml中设置github信息

```yaml
deploy:
  type: git
  repo: 前面创建的GitHub Repository 
  branch: master
  message: Personal Blog
```

安装部署插件，部署到github

```
npm install hexo-deployer-git --save
hexo deploy
```

略等几分钟即可正常访问 username.githu.io 