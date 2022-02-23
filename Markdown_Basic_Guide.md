---
title: "Markdown_Basic_Guide"
date: 2019-08-11T18:32:08+08:00
draft: true
---

# Markdown基础指南

## 简介

Markdown 是一种轻量级标记语言，创始人为约翰·格鲁伯（John Gruber）。它允许人们“使用易读易写的纯文本格式编写文档，然后转换成有效的XHTML(或者HTML)文档”。

Markdown 可以用于编辑 .md后缀的文档，也可以用于博客文章、笔记的写作，可以在印象笔记(马克飞象)、有道云笔记、简书、掘金、CSDN等平台上发表自己的文章。

Markdown 最大的特点就是它的易读易写性，无需过多的排版操作就能写出美观简洁的文章。

## 语法

### 标题

可以在标题内容前输入特定数量的井号(‘#’)来实现对应级别的HTML样式的标题，一共支持六级标题。
例如：

```markdown
## 二级标题
#### 四级标题
###### 六级标题
```

或者用 = （最高阶标题）和 - （第二阶标题）的方法，此方法只支持两级标题。
例如：

```markdown
This is an H1
=============
This is an H2
-------------
```

### 列表

Markdown 支持有序列表和无序列表。
无序列表使用星号（*）、加号（+）或是减号（-），作为列表标记，可以进行嵌套：

```markdown
* 红
- 黄
+ 蓝
    + 绿
    + 紫
```

效果如下:

* 红

* 黄

* 蓝
  * 绿
  * 紫

有序列表则使用数字接着一个英文句点（.），甚至可以不在意数字排序(但还是希望用有序写法)：

```markdown
1. 第一
2. 第二
4. 第三
3. 第四
```

效果如下：

1. 第一
2. 第二
4. 第三
3. 第四

注意：

* 列表项目标记通常是放在最左边，但是其实也可以缩进，最多 3 个空格。
* 列表项目可以包含多个段落，每个项目下的段落都必须缩进 4 个空格或是 1 个制表符。
* 如果要在列表项目内放进引用，那就需要缩进。
* 如果要放代码区块的话，该区块就需要缩进两次，也就是 8 个空格或是 2 个制表符。

### 分隔线

以在一行中用三个以上的星号（*）、减号（-）、底线（_）来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。
例如：

```markdown
* * *
***
- - -
---------------------------------------
```

效果如下：
* * *
***
- - -
---------------------------------------

### 强调

Markdown 使用星号（*）和底线（_）作为标记强调字词的符号。强调就是**加粗**、*倾斜*、~~删除线~~三种效果。
倾斜:用1个星号或者底线将待处理文本包围起来。
加粗：用2个星号或者底线将待处理文本包围起来。
删除线：用2条波浪线（~~）**将待处理文本包围起来。

例如：

```
*倾斜效果* 或者 _倾斜效果_
**加粗效果** 或者 __加粗效果__
~~删除线效果~~
```

效果如下：
*倾斜效果* 或者 *倾斜效果*
**加粗效果** 或者 **加粗效果**
~~删除线效果~~

注意：

* 如果 * 和 _ 两边都有空白的话，它们就只会被当成普通的符号。
* 如果要在文字前后直接插入普通的星号或底线，可以用反斜线。

例如：

```markdown
\*this text is surrounded by literal asterisks\*
```

效果如下：
\*this text is surrounded by literal asterisks\*

另外，在Meme博客主题中，还支持一种叫..着重号..的强调格式：用2个点(.)将待处理文本包围起来。
例如：
``.. 着重号效果 ..``

效果如下：..着重号效果..

### 插入链接
Markdown 支持两种形式的链接语法： ..行内式.. 和 ..参考式.. 两种形式。不管是哪一种，链接文字都是用 [方括号] 来标记。

行内式的格式为：``[link text](URL 'title text'"title")``

例如：

```makrdown
[Google](http://www.google.com/ "谷歌")
[百度](http://www.baidu.com/ "baidu")
```

显示效果如下：
[Google](http://www.google.com/ "谷歌")
[百度](http://www.baidu.com/ "baidu")

参考式链接的写法相当于行内式拆分成两部分，并通过一个[id]来连接两部分。id，可以用字母、数字和空格，不分大小写，方便我们在文章中多次引用。参考式能尽量保持文章结构的简单，也方便统一管理 URL。
格式为：

```makrdown
[link text][name]
[name]: link "title"
```

例如：

```markdown
我日常使用 [Google][1] 多一些,偶尔使用 [百度][2]，很少使用[Bing][3]。
我不得不使用 [百度搜索][2]的时候，总是感觉 [谷歌][1]大法好啊。

[1]: https://www.google.com/ "Google"
[2]: https://www.baidu.com/ "Baidu Search"
[3]: https://cn.bing.com/ "Bing Search"
```

显示效果：
我日常使用 [Google][1] 多一些,偶尔使用 [百度][2]，很少使用[Bing][3]。
我不得不使用 [百度搜索][2]的时候，总是感觉 [谷歌][1]大法好啊。

[1]: https://www.google.com/ "Google"
[2]: https://www.baidu.com/ "Baidu Search"
[3]: https://cn.bing.com/ "Bing Search"

### 插入代码

Markdown 中在行内插入代码用1个反引号（\`）把代码包围起来，效果如下：
在行内插入`代码code`效果。

Markdown 中建立代码区块有两种方法：

1. 在代码区前缩进 4 个空格或是 1 个制表符
2. 代码段落的头部和尾部用```包围起来

第一种用法很简单，直接用Tab就好。第二种用法可以实现代码高亮等特殊效果，更推荐用第二种方法。

第二种方法用法如下：

```markdown
\`\`\`
[language] [title] [url] [link-text]
代码段
\`\`\`

* [language] 是代码语言的名称，用来设置代码块颜色高亮，非必须；
* [title] 是顶部左边的说明，非必须；
* [url] 是顶部右边的超链接地址，非必须；
* [link text] 如它的字面意思，超链接的名称，非必须。
```

例如：

```markdown
\`\`\` [C] [文件位置：helloworld.c]
#incldue <stdio.h>

int main()
{
printf(“hello world！\n”);
return 0;
}
\`\`\`
```

效果如下：

```C [文件位置：helloworld.c]
#incldue <stdio.h>

int main()
{
    printf("hello world！\n");
    return 0;
}
```

### 插入表格
Markdown中插入表格的方法如下:

```markdown
| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |
```

详细说明如下：

* 第一行为定义表格头部标题，而第二行是区分头部和设置对齐方式, 减号(-)至少有3个。
* 表格外围的管道的可选的, 也不需要让每行的每个TD的管道对齐。
* 在减号的两侧定义冒号”:” 可设置该竖行的对齐方式, 左边加等于左对齐，两边都加等于居中对齐。

显示效果如下：

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

### 插入图片
Markdown 使用一种和链接很相似的语法来标记图片，同样也允许两种样式：..行内式.. 和 ..参考式.. 。

行内式的图片语法：

```markdown
![Alt text](/path/to/img.jpg)
![Alt text](/path/to/img.jpg "Optional title")
```

详细叙述如下：

1. 一个惊叹号 !
2. 接着一个方括号，里面放上图片的替代文字
3. 接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上选择性的 ‘title’ 文字。

例如：

```markdown
![百度Logo](https://www.baidu.com/img/baidu_jgylogo3.gif)
![百度Logo](https://www.baidu.com/img/baidu_jgylogo3.gif "Baidu logo")
```

效果如下：
![百度Logo](https://www.baidu.com/img/baidu_jgylogo3.gif)
![百度Logo](https://www.baidu.com/img/baidu_jgylogo3.gif "Baidu logo")

参考式的图片语法：

```markdown
![Alt text][id]
```

「id」是图片参考的名称，图片参考的定义方式则和连结参考一样：

```makrdown
[id]: url/to/image  "Optional title attribute"
```

### 插入音乐

插入音乐有两种方法：

1. 使用HTML标签
2. 使用aplayer插件

#### HTML方法
```markdown
<audio src="https://什么什么什么.mp3" style="max-height :100%; max-width: 100%; display: block; margin-left: auto; margin-right: auto;" controls="controls" loop="loop" preload="meta">Your browser does not support the audio tag.</audio>
```

也可以直接使用网易云音乐等音乐平台的外链直接粘贴

```html
<iframe
frameborder="no"
border="0"
marginwidth="0"
marginheight="0"
width=330
height=86
src="//music.163.com/outchain/player?type=2&id=27867503&auto=0&height=66">
</iframe>
```

效果如下：
<iframe
frameborder="no"
border="0"
marginwidth="0"
marginheight="0"
width=330
height=86
src="//music.163.com/outchain/player?type=2&id=27867503&auto=0&height=66">
</iframe>

#### Aplayer插件

首先在..站点..文件夹根目录安装插件：``npm install hexo-tag-aplayer --save``

在文章中的写法：

单曲：

```css
{%
aplayer
"歌曲名"
"歌手名"
"https://什么什么什么.mp3"
"https://封面图.jpg"
"lrc:<https://歌词.lrc>"
%}
```

歌单：
```css
{% aplayerlist %}
{
    "autoplay": false,
    "showlrc": 3,
    "mutex": true,
    "music": [
        {
            "title": "歌曲名",
            "author": "歌手名",
            "url": "https://什么什么什么.mp3",
            "pic": "https://封面图.jpg",
            "lrc": "https://歌词.lrc"
        },
        {
            "title": "歌曲名",
            "author": "歌手名",
            "url": "https://什么什么什么.mp3",
            "pic": "https://封面图.jpg",
            "lrc": "https://歌词.lrc"
        }
    ]
}
{% endaplayerlist %}
```

### 插入视频

像插入音乐一样，可以采取HTML标签和插件两种方法。

#### 使用HTML标签

```html
<video
poster="https://封面图.jpg"
src="https://什么什么什么.mp4"
style="max-height :100%;
max-width: 100%;
display: block;
margin-left: auto;
margin-right: auto;"
controls="controls"
loop="loop"
preload="meta">
</video>
```

也可以在哔哩哔哩或者YouTube上复制嵌入代码，例如：

```html
<iframe
src="https://player.bilibili.com/player.html?aid=59593621&cid=103820040&page=1"
scrolling="no"
border="0"
frameborder="no"
framespacing="0"
allowfullscreen="true"
style="width: 640px; height: 500px;">
</iframe>
```

效果如下：
<iframe
src="https://player.bilibili.com/player.html?aid=59593621&cid=103820040&page=1"
scrolling="no"
border="0"
frameborder="no"
framespacing="0"
allowfullscreen="true"
style="width: 640px; height: 500px;">
</iframe>

注意：

* 在src后面应加入“https:”
* 调整视频显示尺寸: style=”width: 640px; height: 500px;

#### 使用dplayer插件

首先在..站点..文件夹根目录安装插件：``npm install hexo-tag-dplayer --save``

文章中的写法：

```css
{% dplayer
"url=<https://什么什么什么.mp4>"
"https://封面图.jpg"
"api=<https://api.prprpr.me/dplayer/>"
"id="
"loop=false"
%}
```

此插件可支持弹幕，必须有api和id两项，id值随便取即可。

### 插入公式

NexT主题支持 MathJax 进行数学公式显示。
可以利用gulp 和 gulp-mathjax-page 对将公式渲染为SVG并嵌入HTML并实现静态化。

#### 安装插件
```
npm install -g gulp@3.9.1
npm install -s gulp@3.9.1 gulp-mathjax-page
```

修改gulpfile.js
```js
[文件位置：~/blog/gulpfile.js]
var gulp = require('gulp')
var mathjax = require('gulp-mathjax-page')

gulp.task('mathjax', function() {
    gulp.src('./public/**/*.html')
    .pipe(mathjax({
        mjpageConfig: {
            format: ['TeX'],
            singleDollars: true,
            cssInline: false,
            mhchem: {legacy: true}
        },
        mjnodeConfig: {
            svg: true,
            css: false,
            speakText: false
        }
    }))
    .pipe(gulp.dest('./public'))
})
```

修改样式

```js
[文件位置：~/blog/themes/next/source/css/_custom/custom.styl]
.mjpage__block {
    display: inline-block;
    text-align: center;
    width: 100%;
    overflow-x: auto;
    vertical-align: bottom;
}
/*
如果出现尺寸过大的问题，则加上以下代码
*/
.mjpage {
    font-size: 10px;
}
```

#### 使用

语法请参考MathJax 中文文档

## 编辑器

* MarkdownPad: 一款全功能的编辑器，被很多人称赞为Windows 平台最好用的Markdown 编辑器
* Typora: 颜值不错，支持Windows、Linux、OS X
* Boostnote: 对程序员友好，支持多种代码高亮功能
* VSCode: 宇宙第一编辑器，当然要支持Markdown了

## 参考资料

Markdown语法说明
打造个性超赞博客 Hexo + NexT + GitHub Pages 的超深度优化
Markdown教程
Markdown在线编辑器
