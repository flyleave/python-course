# 网络爬虫工作原理及常用第三方库

#### 网络爬虫使用的技术--数据抓取： <a id="&#x7F51;&#x7EDC;&#x722C;&#x866B;&#x4F7F;&#x7528;&#x7684;&#x6280;&#x672F;--&#x6570;&#x636E;&#x6293;&#x53D6;&#xFF1A;"></a>

* 在爬虫实现上，除了scrapy框架之外，python有许多与此相关的库可供使用。其中，在数据抓取方面包括： urllib2（urllib3）、requests、mechanize、selenium、splinter；
* 其中，urllib2（urllib3）、requests、mechanize用来获取URL对应的原始响应内容；而selenium、splinter通过加载浏览器驱动，获取浏览器渲染之后的响应内容，模拟程度更高。
* 考虑效率、当然能使用urllib2（urllib3）、requests、mechanize等解决的尽量不用selenium、splinter，因为后者因需要加载浏览器而导致效率较低。
* 对于数据抓取，涉及的过程主要是模拟浏览器向服务器发送构造好的http请求，常见类型有：get/post。

#### 网络爬虫使用的技术--数据解析： <a id="&#x7F51;&#x7EDC;&#x722C;&#x866B;&#x4F7F;&#x7528;&#x7684;&#x6280;&#x672F;--&#x6570;&#x636E;&#x89E3;&#x6790;&#xFF1A;"></a>

* 在数据解析方面，相应的库包括：lxml、beautifulsoup4、re、pyquery。
* 对于数据解析，主要是从响应页面里提取所需的数据，常用方法有：xpath路径表达式、CSS选择器、正则表达式等。
* 其中，xpath路径表达式、CSS选择器主要用于提取结构化的数据。而正则表达式主要用于提取非结构化的数据。

