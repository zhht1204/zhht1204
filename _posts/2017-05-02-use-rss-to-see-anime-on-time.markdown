---
layout: post
title:  "使用RSS实现自动动漫更新提醒（追番）"
date:   2017-05-02 00:00:00 +0800
categories: software
tags: [software,visual-studio,community,offline]
---

<p>喜欢追动漫番并且喜欢下载下来看和收藏的各位应该都有个觉得不方便的地方，那就是每天都得跑去下载的网站进行查看追的剧是否更新。</p>
<p>而这并不是难受的地方，更麻烦的是还要记每部剧上个星期放到了第几集，有时候忘记看了，下个星期跳过了一集下载下来，打开看了才发现，然后还得回去下，这真是gay得一批。。</p>
<p>好吧闲话有点多了。进入正题吧。</p>
<!-- more -->
<hr>
<p>作为程序狗的各位对这种需求自然有自己的解决办法，自己写程序进行定时检查是最直接且最贴合个人需要的方法，但如果闲暇时间并没有那么多的话就可以使用现有的技术。</p>
<p>本人喜欢从[动漫花园](http://share.dmhy.org/)下载动漫（现在这个网站也需要fq才能看了。。），动漫花园提供了RSS订阅服务，首先简要介绍一下RSS。</p>
<p>以下摘自<a href="http://baike.baidu.com/link?url=2v4okQhh1HvUQkOs5VKtrnzvW_g4DKzWP21q5WhiyafT6_wLoBrMWMiRjKi17TyjOqneKLNYrxIuOozBa3fZxK">百度百科</a></p>
<p class="well"><em>RSS/Atom源是基于XML的语义网内容,能够被客户端解析程序用做数据源。微格式是嵌入到网页中的语意网微内容。Web源包括RSS/Atom源和微格式源。RSS/Atom的标准化带来了众多软件和网站的广泛应用。扩展的RSS/Atom可用于专业领域。聚合供源与聚合消费器之间,采用"服务器/客户机"模式和标准的HTTP通讯。网站可以根据现有网页或者网站数据库生成RSS/Atom源,也可以考虑将多个外部RSS/Atom源聚合成新的RSS/Atom源。列表RSS/Atom源同时支持对客户端缓存的更新与删除操作。面向浏览器用户通报网站发布的RSS/Atom源,首选自动发现方式。微软提出的SSE协议,用于松散协作的两个网站之间交叉订阅对方的RSS/Atom源,服务于新条目和更新条目的双向、延时同步。</em></p>
<p>简要来说，RSS作为一种经典的订阅方式已经趋于成熟。想要完成一方发布，自己收看这种功能，只需要发布方提供订阅源就行了。</p>
<p>原理之类的暂时不深入了，这篇文章也不是说这个的。</p>
<p>有了订阅源后就只缺阅读工具了，国内有<a href="http://www.yilan.io/">一览</a>和<a href="http://beta5.xianguo.com/">鲜果</a>，以前一览是免费提供服务的，现在需要付费才能自定义订阅源。鲜果阅读器则还是免费的，不过有点难用感觉。而且由于动漫花园需要fq才能看，我也没去尝试是否可以订阅dmhy。</p>
<p>目前我在用的是<a href="https://www.inoreader.com/">Inoreader</a>，一个国外的阅读器。可以免费添加自定义订阅源，并且支持很多语言（包括<strong>中文</strong>），虽然界面有广告不过影响不大。</p>
<p>注册登录后添加订阅源，首先要在dmhy网站上找到RSS的链接，通常每一页上都会有对应的RSS按钮，复制其链接到
<p><img src="{{ image_directory }}/images/posts/2017-05-02-use-rss-to-see-anime-on-time-1.jpg"></p>
<p>点击添加订阅源就可以了。</p>
<p>然后就可以从订阅源列表中看到各种自己定义的订阅源了，省去了每周重复查找和记录的麻烦。</p>

