
## Introduction

Markdown has been widely used in recent years. With this lightweight markup language, users can easily format plain texts. If using the extended features of markdown, users can even insert footnotes, equations,  citations, etc. Some software based on markdown, such as Typora,  even supports flowcharts, gannt charts, and sequence diagrams. Therefore, markdown is supported on many websites, such as steemit.com, utopian.io, github.com, jianshu.com, stackoverflow.com, etc.

I am kinda a guitar player. I often have to write down guitar chords with lyrics. Commercial software packages cost a lot. I  found free software such as LaTeX with some packages, but LaTeX is hard to use, especially for non-programmers. As markdown is free and easy to use, is it possible to integrate guitar chords, just like equations, into markdown files?

The answer was no, until I developed bookdown-guitar.


## Features

bookdown-guitar is an open-source project based on the R package bookdown. Technically, it is a template. You can download it or fork it, and write your own guitar chords out of it. You can change the chord commands as you like, and create some personal chords of your own.

In the meanwhile, bookdown-guitar is more than a template. It is a book as well. I have collected some often-used chords together. I have also collected the lyrics of some pop songs in it, and converted into a pdf book, which is friendly to print. You can use it as a song book or a guitar chord reference book.

Last but not the least, bookdown-guitar is free of charge and cross platform. As it is built in the framework of R environment, bookdown package, markdown syntax, you don't have to spend a single penny on it. You can use it on Windows, Linux and macOS.

The following images show the guitar book you will get. A song with guitar chords looks like this:

![20180104-183138.jpg](https://res.cloudinary.com/hpiynhbhq/image/upload/v1515087356/m8bycdyimtfotktn2bnd.jpg)


bookdown-guitar support Chinese characters. A Chinese song with guitar chords looks like this:

![20180104-183010.jpg](https://res.cloudinary.com/hpiynhbhq/image/upload/v1515087414/ys2a214hap5uqluitcdh.jpg)


The collection of the often-used guitar chords is on the last page of the guitar book., which is shown below:

![20180104-183157.jpg](https://res.cloudinary.com/hpiynhbhq/image/upload/v1515087449/o504lmmin1tnedgt2vln.jpg)



## Quick Start

### Preparation

- [Download R](https://cran.r-project.org) and install it.
- [Download](https://www.rstudio.com/) RStuidio IDE and install it.
- [Download LaTeX](http://www.ctex.org/CTeXDownload) and install it.  Choose the right distribution out of MikTeX, TeXLive and MacTeX for your operation system. 
- In R environment, run the following codes to install bookdown package.

```
install.packages('bookdown')
```


### Download or clone bookdown-guitar

- Visit the link to the repo: https://github.com/pzhaonet/bookdown-guitar
- Click the dark green button 'Clone or Download', and then Download ZIP. You will get a compressed file named bookdown-guitar-master.zip.

![20180104-162130.jpg](https://res.cloudinary.com/hpiynhbhq/image/upload/v1515087551/i7tvi8c1weixopjhorjr.jpg)


- Unzip bookdown-guitar-master.zip and you will get a folder.  You can clone it as well if you have a github account.
- Click the file 'bdguitar.Rproj', and it will be opened by RStudio by default.

### Structure of the folder

The structure of the folder 'bookdown-guitar-master' is shown as follows.

```
bookdown-guitar-master
│  bdguitar.Rproj
│  cd.Rmd
│  hallelujah.Rmd
│  hh.Rmd
│  index.Rmd
│  index.txt
│  mk.Rmd
│  README.md
│  sqxy.Rmd
│  ybgs.Rmd
│  ybzsqln.Rmd
│  zzz_toolbox.Rmd
│  _bookdown.yml
│  _output.yml
├─css
├─images
├─latex
│      after_body.tex
│      before_body.tex
│      chordbox.tcl
│      preamble.tex
│      preamble_backup.tex
│      template.tex
│      _gchords.sty
├─_book
│  │  bdguitar.epub
│  │  bdguitar.pdf
│  │  bdguitar.tex
│  │  cd.html
│  │  hallelujah.html
│  │  hh.html
│  │  index.html
│  │  method.html
│  │  mk.html
│  │  search_index.json
│  │  sqxy.html
│  │  toolbox.html
│  │  ybgs.html
│  │  ybzsqln.html
│  ├─bdguitar_files
│  ├─css
│  ├─images
└─_bookdown_files
```

The beginners don't have to understand most of these files, except *.Rmd* files, which contains lyrics and guitar chords in them. The demo book is in the *_book* folder. You can view the bdguitar.pdf with any pdf viewer.

### Examples

Open hallelujah.Rmd file, as an example, in RStudio. You will see a text editor window as follows. 

![20180104-172620.jpg](https://res.cloudinary.com/hpiynhbhq/image/upload/v1515087645/efeqnenqpwbcu1zlssku.jpg)


The commands beginning with `\` are the guitar chords. `\CM` means C major, `\Am` means A minor, and so on so forth. There are guitar chords already inserted into the first paragraph as a demo. You can insert some chords into the second paragraph like this:

```
Your \CM faith ~~was~~ **strong** 
But you \Am needed [proof](https://utopian.io)

You \CM saw her bathing 
\Am On the roof

Her \F beauty and the Moonlight 
\CM overthrew you \GM
```



You can change the format of the text with markdown syntax as shown above.

Then click the `Build Book` button on the top right, then `bookdown::pdf_book` (instead, you can do it via the hot key ctrl+shift+b). The guitar book will be updated. 



After several seconds (it depends on your computer's calculation power), a pdf file will be opened automatically, and you will see the guitar book updated as follows.

![20180104-210300.jpg](https://steemitimages.com/DQmSpRMLvqgFKJZriKJUFFZVG7wK6QwbDCsqoPJhsFLf4zX/20180104-210300.jpg)

As it is a book for printing, the format of hyperlink is converted into footnote.
### Advanced Users

Advanced users might want to know how it works and how to insert other guitar chords not shown in the example. This is going to be written in a tutorial if anyone is interested in it. Shortly speaking, please read the manual of the LaTeX package 'gchords' and then find the definition of the chord commands in '/latex/preamble.tex'.

---



近年来，Markdown 应用越来越广泛。使用这种轻量级的标记语言，用户可以轻松地为纯文本添加格式。如果是用 markdown 的扩展语法，还可以插入脚注、公式、引用等。有些软件，例如我喜欢的 Typora，还能支持流程图、甘特图、序列图等。因为 markdown 的强大和易用，很多网站都采用它，例如 steemit.com, utopian.io, github.com, jianshu.com, stackoverflow.com, 等等。

熟悉我的朋友知道，我会弹一点吉他，经常需要在歌词上记录吉他谱。吉他谱商业软件价格不菲，而吉他手往往很穷。免费的记录吉他谱软件，如 LaTeX 附加扩展包，并不方便使用，对非程序员尤为如此。既然 markdown 是免费的，而且易用，那么有没有可能将吉他和弦谱融入到 markdown 文件里呢？

答案曾经是不可能， 直到我开发了 bookdown-guitar 这个项目。

bookdown-guitar 是个基于 R 语言扩展包 bookdown的 开源项目。本质上，它是个模板。你可以下载或者 fork 这个模板，在其基础上写你自己的吉他谱。你也可以随心所欲更改吉他谱的插入命令。当然，你也可以创建新的和弦指法图。

同时，bookdown-guitar 远远不只是个模板。它还是一本书。这本书里搜集了常用的和弦指法表，以及我喜欢的一些歌曲。我把它做成了一本 pdf 书，非常方便打印，可以用作歌本或和弦字典。

最后，bookdown-guitar 是跨平台的免费软件。由于建立在免费的 R 语言环境的框架里，并且使用免费的 bookdown 扩展包和通用的 markdown 语法，你不用花一分钱，就可以在 Windows, Linux 或 macOS 任意平台使用。

上面的英文部分的插图展示了 bookdown-guitar 的模样。



## 快速入门

### 准备

- [下载和安装 R 语言环境](https://cran.r-project.org)。
- [下载和安装RStuidio IDE](https://www.rstudio.com/).
- [下载和安装 LaTeX](http://www.ctex.org/CTeXDownload)。为你的操作系统选择合适的发行版，例如MikTeX, TeXLive，MacTeX等。
- 在 R 语言环境里，运行下面的代码，安装 bookdown 扩展包。

```
install.packages('bookdown')
```

### 下载或克隆 bookdown-guitar

- 访问 bookdown-guitar 的主页: https://github.com/pzhaonet/bookdown-guitar
- 点击深绿色按钮 'Clone or Download' 来下载压缩文件 bookdown-guitar-master.zip。
- 解压缩，会得到一个文件夹。当然，如果你有 github 账号，也可以克隆这个项目。
- 双击 'bdguitar.Rproj' 文件，在 RStudio 里打开。

### 示例

在 RStudio 里打开 hallelujah.Rmd 文件，会看到下面的编辑窗口。



以 `\` 开头的命令就是吉他和弦谱。 `\CM` 表示 C 大三和弦， `\Am` 表示 A 小三和弦。

歌曲第一段已经插入了和弦谱，作为示例。你可以将第二段改为下面的代码，来插入新的和弦谱。:

```
Your \CM faith ~~was~~ **strong** 
But you \Am needed [proof](https://utopian.io)

You \CM saw her bathing \Am On the roof

Her \F beauty and the Moonlight  
\CM overthrew you \GM
```



文字部分可以用 markdown 语法来修改格式。

然后，点击右上角的 `Build Book` 按钮，选中 `bookdown::pdf_book` (也可以用快捷键 ctrl+shift+b)。吉他书就会得到更新。

等几秒钟 (时间取决于你的计算机速度)，一个 pdf 文件会自动打开。看看你自己输入的和弦谱吧！

### 高级用户

### Advanced Users

高级用户或许想知道 bookdown-guitar 是如何工作的，如何插入示例之外的和弦谱。如果有人感兴趣，我或许会写个教程。简单来说，那就是去阅读 LaTeX 的 'gchords' 扩展包说明文档，然后在 '/latex/preamble.tex' 文件里定义和弦谱。



写得累死我了。预祝大家玩得愉快吧。


<iframe width="100%" height="166" scrolling="no" frameborder="no" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/347459247&amp;color=%23ff5500&amp;auto_play=false&amp;hide_related=false&amp;show_comments=true&amp;show_user=true&amp;show_reposts=false&amp;show_teaser=true"></iframe>
