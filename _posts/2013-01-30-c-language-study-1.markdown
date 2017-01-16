---
layout: post
title:  "C语言个人学习记录（一）基本从完全不懂开始。"
date:   2013-01-30 16:00:58 +0800
categories: it clang
tags: [it,c,编程]
---

<div style="text-indent: 2em;">学习记录中基本除去高中已学习内容。</div>
<!-- more -->
<div style="text-indent: 2em;">
基本应该是没有人会看我的博客的，不过如果有的并且发现我哪里错的请指出，谢谢帮忙了。</div>
<div style="text-indent: 2em;">一直错下去可不是什么好主意。</div>
<div style="text-indent: 2em;">学习按清华大学出版社的《C语言入门很简单》来。</div>
<div style="text-indent: 2em;"><br></div>
1.首先，是计算机语言发展史，简图。
<div>&nbsp;<wbr> &nbsp;<wbr>
（摘自清华大学出版社的《C语言入门很简单》）</div>
<img src="{{ site.post_image_directory }}/2013-01-30-c-language-study-1-1.jpg" >
<div>2.开发过程中的三个基本工具（主要功能）</div>
<div>
<ul>
<li>编辑器——即由输入端输入至电脑，最基本的例子为由敲击键盘转化为至电脑中的含代码文件。得到的文件称为（程序）源文件。</li>
<li>编译器——保存源文件并转化为目标文件（二进制文件）（机器语言）。此过程称为“编译”。</li>
<li><span style="text-indent: 2em;">链接器——将目标二进制文件与库二进制文件结合，生成操作系统下可执行文件。此过程称为“链接”</span></li>
</ul>
&nbsp;<wbr> &nbsp;<wbr> &nbsp;<wbr>
（我想了一个比喻，以做巧克力为喻。首先要入手巧克力，无论是去超市买还是买了各种原材料自己搞，总之做成了一块巧克力。此过程为编辑。</div>
<div>&nbsp;<wbr> &nbsp;<wbr> &nbsp;<wbr>
&nbsp;<wbr>
而我们的最终目的是做出一个有特定形状的巧克力，这块整块的巧克力并不能讨女朋友的欢心，所以需要一些别的工程。</div>
<div>&nbsp;<wbr> &nbsp;<wbr> &nbsp;<wbr>
&nbsp;<wbr>
接下来我们把巧克力加热溶解了变成巧克力浆，这下我们能把巧克力变成任何形状了。此过程为编译。</div>
<div>&nbsp;<wbr> &nbsp;<wbr> &nbsp;<wbr>
&nbsp;<wbr>
最后我们把巧克力浆倒入模具，等待它凉下来固化。最后就形成了我们需要的漂亮的能讨女朋友欢心的巧克力。此过程为链接。</div>
<div>&nbsp;<wbr> &nbsp;<wbr> &nbsp;<wbr>
&nbsp;<wbr> 不知形不形象。。总之我觉得还算不错的样子。。）</div>
<div>&nbsp;<wbr> &nbsp;<wbr> 在visual
studio中编译与链接是一体化的，我是说操作。只要点一次生成或者开始运行或者启动调试就能在各不同文件夹中生成可执行程序或者是输出库文件。</div>
<div><br></div>
<div>3.一般的开发环境——visual studio</div>
<div>&nbsp;<wbr> &nbsp;<wbr>
本人用的版本是2010专业版的。。我也忘了是哪里下载的了，刻成光盘后就保存着。。</div>
<div>&nbsp;<wbr> &nbsp;<wbr>
接下来换篇记录关于新建项目与执行。。虽然这第一篇好像挺短的。。</div>
<div>&nbsp;<wbr> &nbsp;<wbr>
不过要说的话我认为其实也没什么特别需要记得啦。。到代码之类的才有许多需要记的，大概。。等我学到了再看看吧。。</div>
<div><br></div>
<div>4.基本代码记录</div>
<div>学到哪里更新到哪里。</div>
<div><font style="font-size: 20px;"><br></font></div>
<div><font style="font-size: 20px;">-------------------------------------------------------------</font></div>
<div><font style="font-size: 22px;">三种基本数据类型</font></div>
<div><span style="line-height: 30px;"><font style="font-size: 14px;">（类型名：表示符（关键字）（括号内为可省略）：精度：表示范围：适合表示的数字）</font></span></div>
<div>
<ul>
<li><font style="font-size: 14px;">整形（精度均为1）</font></li>
</ul>
</div>
<div>有符号整形：(signed )int：-2^31~2^32-1：大整数</div>
<div>有符号短整形：(signed )short( int)：-2^15~2^15-1：小整数</div>
<div>有符号长整形：(signed )long( int)：<span style="line-height: 21px;">-2^31~2^32-1：大整数</span></div>
<div><span style="line-height: 21px;">无符号整形：unsigned
int：0~2^32-1：大正整数</span></div>
<div><span style="line-height: 21px;">无符号短整形：unsigned short(
int)：0~2^16-1：小正整数</span></div>
<div><span style="line-height: 21px;">无符号长整形：unsigned long (
int)：</span><span style="line-height: 21px;">0~2^32-1：大正整数</span></div>
<div>[<font color="#ED1C24">整理</font>：有符号与无符号的差别在于能不能表示负数，“-”号是一个符号，所以需要有符号整形来表示。</div>
<div>&nbsp;<wbr> &nbsp;<wbr> &nbsp;<wbr>
&nbsp;<wbr>而长短整形的区别在于表示区间的大小。这个很简单，如字面上的意思。</div>
<div>&nbsp;<wbr> &nbsp;<wbr> &nbsp;<wbr>
&nbsp;<wbr>至于为什么把数字设定在2^32与2^16我就不理解了，是因为人定的标准吗？还是因为机器物理上的极限？不过暂时我也不想具体了解。。还是以后再论吧。。]</div>
<div>
<ul>
<li>浮点型</li>
</ul>
单精度浮点型：float：3.4*10^38：3.4*10^-38~3.4*10^38：精度要求不高的小数</div>
<div>双精度浮点型：double：1.7*10^308:1.7*10^-308~1.7*10^308：精度要求高的小数</div>
<div>[<font color="#FF0000">整理</font>：浮点型主要用于表示小数。原书上写区间时为3.4*10^38~3.4*10^38，与1.7*10^308~1.7*10^308这不就是一个数了吗？大概是编辑错了还是打印错了。。</div>
<div>&nbsp;<wbr> &nbsp;<wbr> &nbsp;<wbr>
&nbsp;<wbr>我猜测浮点型需要的空间比整形的大，否则以其区间之大与灵活性之高，整形都差不多该废弃了。。不过存在即为合理，应该不止是我想的那么简单。学下去应该能知道。]</div>
<div>
<ul>
<li>字符型</li>
</ul>
各种符号，如“A”、“我”、“1”均可为字符。</div>
<div>
----------------------------------------------------------------------------------------</div>
<div>变量声明</div>
<div><span style="color: rgb(0, 183, 239);">变量类型 变量名;</span></div>
<div>（例：</div>
<div>&nbsp;<wbr> int abc;</div>
<div>&nbsp;<wbr> 此例中把“abc”定义为整形）</div>
<div>
-----------------------------------------------------------------------------------------</div>
<div><font color="#ED1C24">标示符</font>包括类型名与变量名，类似于人的“名字”。</div>
<div>标示符 = 首部 + 其他（本书上把“其”写成“基”了）</div>
<div><font color="#FF0000">首部</font>：只能用大小写字母或下划线</div>
<div><font color="#FF0000">其他</font>：除去首部以外的部分。可以为数字、大小写英文字母、数字）</div>
<div>
------------------------------------------------------------------------------------------</div>
<div>c语言中的<font color="#ED1C24">关键字</font>（如同巧克力的模板，不可作为“名字”来使用）</div>
<div>auto break case char const continue default</div>
<div>do double else emun extern float for</div>
<div>goto if int long register return short</div>
<div>signed sizeof static struct switch typedef union</div>
<div>unsigned void volatile while</div>
<div>
-------------------------------------------------------------------------------------------</div>
<div>常量的使用</div>
<div>
为了使程序在修改时方便，当然还有别的各种各样的好处，常将要计算的值赋予某个变量，当然如果对计算较方便那么直接用数字、字母也行，不过许多情况都是赋值予有名字的变量比较方便。</div>
<div>const常量表示</div>
<div><font color="#00B7EF">const 变量类型名 变量名 = 变量要赋的值;</font></div>
<div>（例：const int abc = 500</div>
<div>&nbsp;<wbr> 此例中将abc定义为整形，值固定为500）</div>
<div>
--------------------------------------------------------------------------------------------</div>
<div>赋值运算</div>
<div><font color="#00B7EF">变量名 = 值;</font></div>
<div>但是注意，在C语言中规定，必须先声明、定义变量，然后才能赋值。也就是先</div>
<div><font color="#00B7EF">变量类型 变量名;</font></div>
<div>不过有时为了方便可以在初次定义时直接赋值。此时结合就为</div>
<div><font color="#00B7EF">变量类型 变量名 = 值;</font></div>
<div>（例：</div>
<div>int abc</div>
<div>abc = 500</div>
<div>可结合为</div>
<div>int abc = 500）</div>
<div>
--------------------------------------------------------------------------------------------</div>
<div>灵活的赋值，可手动输入</div>
<div><font color="#00B7EF">scanf{"%变量类型名",&amp;变量名);</font></div>
<div>（例：</div>
<img src="{{ site.post_image_directory }}/2013-01-30-c-language-study-1-2.jpg" >
<div>此例中，前面的先不管，书上也没说。。</div>
<div>int abc 为申明变量。</div>
<div>scanf("%d",&amp;abc)
为此式应用。利用scanf函数给abc赋值，值由之后输入。d代表的是十进制。之后详列。</div>
<div>重点为这两行。）</div>
<div>
-----------------------------------------------------------------------------------------</div>
<div>scanf函数中%后那个字母代表的及各进制赋值规定</div>
<div>d = 十进制（按十进制赋值按普通的来就行了）</div>
<div>o = 八进制（按八进制赋整形常量值时需在最前面一位加个0，如十进制的100就在八进制中表示为0144）</div>
<div>x = 十六进制（按十六进制时要以“0x”或“0X”开头，如十进制的100在十六进制中可表示为0x64）</div>
<div>[<font color="#FF0000">整理</font>：写到这而我突然想到，原来psp中的数据是这样啊。。习惯一样，所以判断里面的数据基本都是用16进制的，所以才可以用16进制查看器来看啊。。某种意义上来说有种豁然开朗的感觉。。）</div>
<div>
------------------------------------------------------------------------------------------</div>
<div>把值输出到终端，查看变量</div>
<div><font color="#00B7EF">printf("%变量类型表示,变量名);</font></div>
<div>可在“""”内“%变量类型名”之后加一个“\n”来使输出后换行，看起来舒服些。</div>
<div>与scanf的用法有些类似。但是<font color="#FF0000">注意变量名前不用&amp;</font>。</div>
<div>[<font color="#FF0000">笔记</font>：遇到了一个问题，win7+vs2010环境下，printf函数使用时，cmd终端闪了一下就跳掉了。</div>
<div>&nbsp;<wbr> &nbsp;<wbr> &nbsp;<wbr>
&nbsp;<wbr>后来找到一个办法，在“return 0;”前一行加“getchar()”]</div>
