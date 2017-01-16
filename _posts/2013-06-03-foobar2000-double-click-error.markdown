---
layout: post
title:  "foobar2000中双击添加文件会覆盖原播放列表的问题"
date:   2013-06-03 15:41:38 +0800
categories: it software
tags: [it,foobar200,software,错误]
---

<article>
<p>改一下设置就好了。之前为了这个受到不少麻烦啊。一开始几次都没想到可以撤销，结果重新弄了好几次播放列表。。
<!-- more -->
<p>顺便说句我的foobar版本是v1.2.6的。。</p>
<p>在参数选项里的<font color="#FF0000">外壳交互</font>。</p>
<p>建议把设置加入队列为默认操作关掉，因为这样双击了文件也只是加入队列而不会播放，挺麻烦的。</p>
<p>主要就是那个“<font color="#FF0000">总是发送新文件到播放列表</font>”，（之前我怎么都没注意到呢。。）把它点上就行了。</p>
<p>这样双击了也只会把文件发送到某个指定列表。</p>
<p>
不过要注意的是，就算是这样设置了，双击时那个被指定的列表还是会被覆盖的，最好是建好自己的列表，把默认作为指定列表，或者新建个列表专门作为指定列表。</p>
<img src="{{ site.post_image_directory }}/2013-06-03-guanyu-megui-chuxian-avisynth-error-1.jpg" >
</article>