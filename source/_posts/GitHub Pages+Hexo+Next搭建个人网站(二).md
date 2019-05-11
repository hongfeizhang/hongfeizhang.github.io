---
title: GitHub Pages+Hexo+Next搭建个人网站(二)
date: 2019-05-09 23:22:10
categories: 建站
tags: 
    - Hexo
    - Next
---
### [使用Next主题](https://theme-next.iissnan.com/)

> 在 Hexo 中有两份主要的配置文件，其名称都是 _config.yml。 其中，一份位于站点根目录下，主要包含 Hexo 本身的配置；另一份位于主题目录下，这份配置由主题作者提供，主要用于配置主题相关的选项。
> 为了描述方便，在以下说明中，将前者称为 站点配置文件， 后者称为 主题配置文件。

#### 下载Next主题

```bash
$ cd your-hexo-site
$ git clone https://github.com/iissnan/hexo-theme-next themes/next
```

#### 启用主题，设置语言，编辑站点配置文件

```yaml
language: zh-CN

theme: next
```
<!-- more -->
#### 选择 Scheme，编辑主题配置文件

```yaml
# Schemes
#scheme: Muse
#scheme: Mist
scheme: Pisces
#scheme: Gemini
```

#### 设置菜单，编辑主题配置文件
```yaml
menu:
  home: / || home
  #about: /about/ || user
  tags: /tags/ || tags
  categories: /categories/ || th
  archives: /archives/ || archive
```

#### 标签与分类
```yaml
categories:
- 父类
- 子类
tags:
- 标签1
- 标签2
---
```

#### 侧边栏社交链接，编辑主题配置文件

```yaml
# Social links
social:
  GitHub: https://github.com/your-user-name
  Twitter: https://twitter.com/your-user-name
  微博: http://weibo.com/your-user-name
  豆瓣: http://douban.com/people/your-user-name
  知乎: http://www.zhihu.com/people/your-user-name
# Social Icons
social_icons:
  enable: true
  # Icon Mappings
  GitHub: github
  Twitter: twitter
  微博: weibo
```

#### 开启打赏功能，订阅微信公众号，编辑主题配置文件
```yaml
reward_comment: 坚持原创技术分享，您的支持将鼓励我继续创作！
wechatpay: /path/to/wechat-reward-image
alipay: /path/to/alipay-reward-image

# Wechat Subscriber
wechat_subscriber:
  enabled: true
  qcode: /uploads/wechat-qcode.jpg
  description: 欢迎您扫一扫上面的微信公众号，订阅我的博客！
```

#### 友情链接，编辑主题配置文件
```yaml
# title
links_title: Links
links:
  MacTalk: http://macshuo.com/
  Title: http://example.com/
```

#### 评论系统，不能被墙，不要备案，选择来必力
```yaml
livere_uid: #your livere_uid
```

#### [阅读次数统计](https://notes.wanghao.work/2015-10-21-%E4%B8%BANexT%E4%B8%BB%E9%A2%98%E6%B7%BB%E5%8A%A0%E6%96%87%E7%AB%A0%E9%98%85%E8%AF%BB%E9%87%8F%E7%BB%9F%E8%AE%A1%E5%8A%9F%E8%83%BD.html#%E9%85%8D%E7%BD%AELeanCloud)

注册leancloud，登陆，新建应用
![](https://raw.githubusercontent.com/hongfeizhang/Image-Hosting/master/20190511154316.png)

在存储中创建Counter表
![](https://raw.githubusercontent.com/hongfeizhang/Image-Hosting/master/20190511154405.png)

在应用key中找到相应的app_id和app_key
![](https://raw.githubusercontent.com/hongfeizhang/Image-Hosting/master/20190511154715.png)

```yaml
leancloud_visitors:
  enable: true
  app_id: 
  app_key: 
  # Dependencies: https://github.com/theme-next/hexo-leancloud-counter-security
  # If you don't care about security in leancloud counter and just want to use it directly
  # (without hexo-leancloud-counter-security plugin), set `security` to `false`.
  security: true
  betterPerformance: false
```