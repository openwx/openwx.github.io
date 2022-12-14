---
layout: post
title: '为 Jekyll 博客添加 Google SEO 功能'
subtitle: 'Add Google SEO to Your Jekyll Blog'
author: 'openwx'
header-style: text
onTop: true
tags:
  - Google SEO
---

创建了自己的博客，并不能马上通过 google 或者百度搜索得到，需要搜索引擎将博客网站地址收录后才能搜索到。有两种方法能够让搜索引擎添加自己网站的索引。一个是提高自己的网站知名度，让搜索引擎主动去添加索引。另外一种就是主动把个人博客地址链接添加到搜索引擎的索引当中。这里只针对 google，因为百度暂时无法有权利对某些网站进行爬取。

下面是操作步骤：

<!-- TOC -->

- [1. 查看网站是否被收录](#1-查看网站是否被收录)
- [2. 提交搜索资源](#2-提交搜索资源)
- [3. 添加站点地图](#3-添加站点地图)
- [4. 到 Google Search Console 提交站点地图](#4-到google-search-console提交站点地图)
- [5. 手动请求（重新）编入索引](#5-手动请求重新编入索引)

<!-- /TOC -->

# 1. 查看网站是否被收录

用 google 搜索，来查看一下自己的网站是否被收录了，在输入框输入如下内容：

```
site:https://openwx.github.io
```

其中后面的连接`https://openwx.github.io`就是自己的网站地址，如果查看的结果是没有显示自己网站相关的内容的时候，也就是说明自己的网站是没有被收录的。如果被收录了，那么就不用看下面的步骤了。

# 2. 提交搜索资源

点击[Google Search Console](https://search.google.com/search-console?hl=zh)，注意：这里需要用 Google 账号来登录。

点击左上角的添加资源，然后就会出现如下图的选择。

![](/img/in-post/2022-09-26-Jekyll-SEO/%E7%BD%91%E7%AB%99%E8%B5%84%E6%BA%90%E9%80%89%E6%8B%A9.png)

这里选择网址前缀，输入自己的网站地址。然后会生成一个 html 文件，将这个文件上传到自己的网站根目录下即可。这里我是已经上传过了，然后出现下面的显示结果。

![](/img/in-post/2022-09-26-Jekyll-SEO/%E5%AE%8C%E6%88%90%E4%B8%8A%E4%BC%A0.png)

# 3. 添加站点地图

站点地图(Site Map)是用来注明网站结构的文件，我们希望搜索引擎的爬虫了解我们的网站结构,以便于高效爬取内容，快速建立索引。

1. 点击进入 XML-Sitemaps.com 页面，输入博客地址，点击 start。

![](/img/in-post/2022-09-26-Jekyll-SEO/%E7%BD%91%E7%AB%99%E5%9C%B0%E5%9B%BE.png)

2. 等待搜索完成，点击 VIEW SITEMAP DETAILS。

![](/img/in-post/2022-09-26-Jekyll-SEO/%E7%BD%91%E7%AB%99%E5%9C%B0%E5%9B%BE%E5%AE%8C%E6%88%90.png)

3. 下载 SITEMAP 文件 sitemap.xml，并将其上传到网站的根目录。

![](/img/in-post/2022-09-26-Jekyll-SEO/%E4%B8%8B%E8%BD%BD%E7%BD%91%E7%AB%99%E5%9C%B0%E5%9B%BE.png)

> 其实自己可以打开这个文件可以查看一下，其实也就是自己的一些博客的链接。

4. 接下来就是把下载的这个文件上传到自己的网站根目录下。

# 4. 到 Google Search Console 提交站点地图

打开 Google Search Console 网站，然后选择左侧栏选择**站点地图**，如下图所示，然后输入`sitemap.xml`，点击提交。

![](/img/in-post/2022-09-26-Jekyll-SEO/%E6%8F%90%E4%BA%A4%E7%AB%99%E7%82%B9%E5%9C%B0%E5%9B%BE.png)

之后，就会显示站点地图提交成功。

![](/img/in-post/2022-09-26-Jekyll-SEO/%E6%8F%90%E4%BA%A4%E7%AB%99%E7%82%B9%E5%9C%B0%E5%9B%BE%E6%88%90%E5%8A%9F.png)

但是，如果再次在 google 搜索框中输入`site:https//openwx.github.io`发现还是出现一样的结果，这是因为要等待 google 下一次更新索引的时候才会将你添加的内容收录进去的。

# 5. 手动请求（重新）编入索引

编入索引可能需要长达 1-2 周的时间，这个对于有些博客主是接受不了的，当然可以自己手动去添加要求编入索引。当然不一定有效，不过肯定是比被动添加搜索是快一些的。那么如何操作的呢。

我们继续来到 Google Search Console 界面，然后点击左侧栏的**网站检测**，然后输入自己的某一个博客的完整的地址，然后回车。

![](/img/in-post/2022-09-26-Jekyll-SEO/%E7%BD%91%E7%AB%99%E6%A3%80%E6%B5%8B1.png)

然后就会显示**请求编入索引**，点击编入即可。

**转载自：https://zoharandroid.github.io/ 。**
