---

date: 2017-11-19 23:20:00
title: python爬虫爬取ajax加载的动态内容
tags: python
categories: python

---


在使用python爬取网页内容的时候，发现请求到的内容和浏览器开发者工具上看到的不一样，
经过一番百度，才发现该内容是使用ajax加载的内容：
![浏览器上看到的数据](http://img.blog.csdn.net/20171231133004429?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvdTAxMzU2MjYyNQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)


![python请求到的数据](http://img.blog.csdn.net/20171231133037220?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvdTAxMzU2MjYyNQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)


两处相差甚远。

最终在这里找到ajax请求的url
![](http://img.blog.csdn.net/20171231133543138?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvdTAxMzU2MjYyNQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

使用此地址完美请求到缺失的数据
![请求到一组json数据](http://img.blog.csdn.net/20171231133956311?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvdTAxMzU2MjYyNQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)


