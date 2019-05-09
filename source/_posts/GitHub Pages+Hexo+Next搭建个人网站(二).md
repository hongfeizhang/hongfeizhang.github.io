---
title: GitHub Pages+Hexo+Next搭建个人网站(二)
date: 2019-05-09 23:22:10
categories: 建站
tags: Hexo|Next
---
### 自定义域名

懒得备案，域名注册选择[godaddy](http://www.godaddy.com/)。

注册、付款，域名到手。没有选择保护隐私服务（60），除了邮箱其他个人信息都随便填。

进入我的域名，选择管理DNS。

![](https://raw.githubusercontent.com/hongfeizhang/Image-Hosting/master/20190509232614.png)

填上GitHub的地址和自己的仓库地址。

![](https://raw.githubusercontent.com/hongfeizhang/Image-Hosting/master/20190509232828.png)

在GitHub对应的项目仓库，进行设置。

![](https://raw.githubusercontent.com/hongfeizhang/Image-Hosting/master/20190509233136.png)

![](https://raw.githubusercontent.com/hongfeizhang/Image-Hosting/master/20190509233217.png)

稍等几分钟，大功告成。

![](https://raw.githubusercontent.com/hongfeizhang/Image-Hosting/master/20190509233350.png)

### [使用Next主题](https://theme-next.iissnan.com/)

> 在 Hexo 中有两份主要的配置文件，其名称都是 _config.yml。 其中，一份位于站点根目录下，主要包含 Hexo 本身的配置；另一份位于主题目录下，这份配置由主题作者提供，主要用于配置主题相关的选项。
> 为了描述方便，在以下说明中，将前者称为 站点配置文件， 后者称为 主题配置文件。

下载Next主题

```bash
$ cd your-hexo-site
$ git clone https://github.com/iissnan/hexo-theme-next themes/next
```

启用主题，在站点配置文件中

```yaml
language: zh-CN

theme: next
```

在主题配置文件中

```yaml
# Schemes
#scheme: Muse
#scheme: Mist
scheme: Pisces
#scheme: Gemini
```

