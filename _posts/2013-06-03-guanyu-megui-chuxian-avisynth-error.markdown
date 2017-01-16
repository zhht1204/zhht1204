---
layout: post
title:  "关于megui中出现avisynth error（directshowsource：Could not open as video or audio"
date:   2013-06-03 15:39:29 +0800
categories: it software
tags: [it,megui,software,错误]
---

<article>
<p>这个错误百度上一搜倒是不少，只是我找了半天也没找到到底是什么错误，还有怎么改正。</p>
<!-- more -->
<p>毕竟我之前是可以正常使用的，后来也没重装系统，只是有些地方的设置改了，就不能用了。时间段太长，我也记不得到底是哪里改过导致错误了。</p>
<p>废话不多说了，其实很简单，是<a style="color:red">终极解码的设置错误</a>（其它的应该也是解码设置问题？我没试过不太清楚。）。我试了老半天别的，最后却发现居然是这个。。</p>
<p>其中的Mp4/Mov分离器，按照编码模式的默认设置的话是<a style="color:red">NDigital</a>，只要是这个的话就会出现directshowsource错误。</p>
<p>只要把它改成<a>其它两个中任意一个</a>就行了。</p>
<p>顺便说句我是xp系统的。。这个好像有点废话了。。</p>
</article>