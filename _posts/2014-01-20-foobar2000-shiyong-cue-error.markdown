---
layout: post
title:  "foobar2000中使用cue文件出现解析 cuesheet 错误: invalid TITLE syntax错误"
date:   2014-01-20 00:51:27 +0800
categories: it software
tags: [it,foobar200,software,错误]
---

<article>
<div>因为我在网上找了半天，发现解决方法都是些什么把双引号改成单引号之类的，而我试了却没什么用，最后解决了所以来分享下经验。
<div>其实问题很简单，问题出在<font color="#FF0000">文字编码</font>。</div>
<!-- more -->
<div>我的cue文件是这样的：</div>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>REM DISCID 45066606</div>
<iframe id="tmp_downloadhelper_iframe" style="display: none;"></iframe></div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>REM COMMENT "ExactAudioCopy v1.0b1"</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>CATALOG 4582328740111</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>TITLE "親愛なる世界へ"</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>FILE "SCMN-006.wav" WAVE</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>&nbsp;<wbr> TRACK 01 AUDIO</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>TITLE "親愛なる世界へ"</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>PERFORMER "Ceui"</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>&nbsp;<wbr> &nbsp;<wbr> INDEX 01 00:00:00</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>&nbsp;<wbr> TRACK 02 AUDIO</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>TITLE "Close My Eyes"</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>PERFORMER "Ceui"</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>&nbsp;<wbr> &nbsp;<wbr> INDEX 00 05:16:29</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>&nbsp;<wbr> &nbsp;<wbr> INDEX 01 05:18:74</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>&nbsp;<wbr> TRACK 03 AUDIO</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>TITLE "親愛なる世界へ -Off Vocal-"</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>PERFORMER "Ceui"</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>&nbsp;<wbr> &nbsp;<wbr> INDEX 00 09:40:59</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>&nbsp;<wbr> &nbsp;<wbr> INDEX 01 09:43:29</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>&nbsp;<wbr> TRACK 04 AUDIO</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>TITLE "Close My Eyes -Off Vocal-"</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>PERFORMER "Ceui"</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>&nbsp;<wbr> &nbsp;<wbr> INDEX 00 14:59:06</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>&nbsp;<wbr> &nbsp;<wbr> INDEX 01 15:01:51</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>&nbsp;<wbr> TRACK 05 AUDIO</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>TITLE "親愛なる世界へ -Shifted-"</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>PERFORMER "Ceui"</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>&nbsp;<wbr> &nbsp;<wbr> INDEX 00 19:23:69</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>&nbsp;<wbr> &nbsp;<wbr> INDEX 01 19:26:39</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>&nbsp;<wbr> TRACK 06 AUDIO</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>TITLE "親愛なる世界へ -DayBreak-"</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>PERFORMER "Ceui"</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>&nbsp;<wbr> &nbsp;<wbr> INDEX 00 23:44:31</div>
</div>
</blockquote>
<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
<div>
<div>&nbsp;<wbr> &nbsp;<wbr> INDEX 01 23:47:01</div>
</div>
</blockquote>
</blockquote>
<br>
<div>如上所见，并没有出现单、双引号嵌套的问题，然而我死马当活马医把双引号全改成单引号了，也还是没用。</div>
<div>翻来覆去我也找不到有什么语法问题，最后随便试了试改编码，没想到居然成了。。。</div>
<div style="line-height: 21px;">首先一开始是这样的：</div>
<img src="{{ site.post_image_directory }}/2014-01-20-foobar2000-shiyong-cue-error-1.jpg" >
<img src="{{ site.post_image_directory }}/2014-01-20-foobar2000-shiyong-cue-error-2.jpg" >
<div style="line-height: 21px;">然后是这样：</div>
<img src="{{ site.post_image_directory }}/2014-01-20-foobar2000-shiyong-cue-error-3.jpg" >
<div>↓</div>
<img src="{{ site.post_image_directory }}/2014-01-20-foobar2000-shiyong-cue-error-4.jpg" >
<div><img src="{{ site.post_image_directory }}/2014-01-20-foobar2000-shiyong-cue-error-5.jpg" ></div>
<div>其实我建议，cue的文字编码最好都转成ansi，这样最不容易出错。</div>
</article>