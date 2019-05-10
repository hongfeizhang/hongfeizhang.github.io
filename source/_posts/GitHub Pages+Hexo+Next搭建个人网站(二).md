---
title: GitHub Pages+Hexo+Next搭建个人网站(二)
date: 2019-05-09 23:22:10
categories: 建站
tags: 
    - Hexo
    - Next
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

#### 评论系统，选择

