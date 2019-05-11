---
title: GitHub Pages+Hexo+Next搭建个人网站(三)
date: 2019-05-11 15:22:41
categories: 建站
tags: 
    - Hexo
    - Next
---


### 自定义域名

懒得备案，域名注册选择[godaddy](http://www.godaddy.com/)。

注册、付款，域名到手。没有选择保护隐私服务（60大洋），除了邮箱其他个人信息随便填。

进入我的域名，选择管理DNS。
<!-- more -->

![](https://raw.githubusercontent.com/hongfeizhang/Image-Hosting/master/20190509232614.png)



填上GitHub的地址和自己的仓库地址。

![](https://raw.githubusercontent.com/hongfeizhang/Image-Hosting/master/20190509232828.png)

在GitHub对应的项目仓库，进行设置。

![](https://raw.githubusercontent.com/hongfeizhang/Image-Hosting/master/20190509233136.png)

![](https://raw.githubusercontent.com/hongfeizhang/Image-Hosting/master/20190509233217.png)

稍等几分钟，大功告成。

![](https://raw.githubusercontent.com/hongfeizhang/Image-Hosting/master/20190509233350.png)

### 设置图床
使用[PicGo](https://github.com/Molunerfinn/PicGo)，进行文章图片上传、管理，方便快捷。
图床选择GitHub ，省心、方便、快捷。

### 站点源码管理
```yaml
hexo deploy
```
hexo仅仅上传了生成后的静态页面，站点源码也需要管理起来，新建分支save，将源码包括hexo、next主题等等add/commit/push。
![](https://raw.githubusercontent.com/hongfeizhang/Image-Hosting/master/20190511160308.png)

![](https://raw.githubusercontent.com/hongfeizhang/Image-Hosting/master/20190511160347.png)

### Google Webmaster tools
设置 [Google站点管理工具](https://www.google.com/webmasters/) 的验证字符串，用于提交 sitemap

获取 google site verification code
登录 Google Webmaster Tools，导航到验证方法，并选择 HTML Tag。将会获取到一段代码：
```html
<meta name="google-site-verification" content="XXXXXXXXXXXXXXXXXXXXXXX" />
```
将 content 里面的 XXXXXXXXXXXXXXXXXXXXXXX 复制出来。

设置主题。编辑 主题配置文件，修改字段 google_site_verification。
```yaml
google_site_verification: XXXXXXXXXXXXXXXXXXXXXXX
```