# yoferzhang.github.io

 　　本blog已经重新部署在[coding](https://coding.net/u/yoferzhang/p/yoferzhang/git)了，Github这里只是留一个备份。

 >欢迎光临我的博客：[http://yoferzhang.com/](http://yoferzhang.com/)

> 版权声明：本文为博主原创文章，如需转载请注明出处。

## 前言 | Preface
>建立博客也花了些心思，记录下这点滴

　　前后也是花了一天时间才建立好博客，之前总有点惰性，但好歹下决心把博客建起来了；我之前在CSDN上的博客写过三百多篇文章，感觉并不是很舒服，最后就自己搭建了；我这里使用的是[Hexo](http://hexo.io/docs/)加上[Github](https://github.com/)。具体这些是什么就自行谷歌吧，本文主要写整个流程和一些问题，希望能切实帮助到其他第一次建立博客的同学，尤其一些不是很懂前端的。

>我其实刚开始搭建就是对前端了解太少，后来遇到很多小白的问题

## 安装Hexo，Node.js和Github
>关于什么是Hexo，推荐看：[http://zipperary.com/2013/05/28/hexo-guide-1/](http://zipperary.com/2013/05/28/hexo-guide-1/)

　　Note：本文使用的环境是Window用户，至于Linux和Mac用户我暂时还没有尝试，可以[Google](https://www.google.com/)。我的系统是win8.1。

### 安装Node.js

　　Node.js下载地址：[https://nodejs.org/en/](https://nodejs.org/en/)。可能某些同学会遇到MSI格式的文件无法安装的问题，具体情况在安装程序的时候会报错：“There is a problem with this Windows Installer package. A DLL required for this install to complete could not be run. Contact your support personnel or package vendor.”

　　这是因为没有取得管理员权限，而MSI格式的文件右键也没有“以管理员身份运行”的菜单项。这时候要在管理员权限下的命令提示符运行这个软件，比如下图所示：

<center>
![](http://ww3.sinaimg.cn/mw690/a9c4d5f6jw1f280obmv4kj20it0cbdfw.jpg)
</center>

>现在应该需要科学上网才能去下载，没办法做到的同学国内找资源，也是比较好找的。

### 安装Github

　　小白推荐使用Github for windows，下载地址[https://desktop.github.com/](https://desktop.github.com/)。

### 安装Hexo

　　前一步安装Github for windows之后，桌面上会有一个GIt Shell，双击打开。
在里面输入npm命令安装Hexo。

```
npm install hexo-cli -g
npm install hexo --save
```

>这一步可能会比较慢，如果时间太长，推荐全局科学上网。

　　到这需要安装的东西就完成了，下面开始进行配置。

## 配置文件

### 创建Hexo文件夹

　　自行建立一个空文件夹，比如我的是：`E:\blog`。进入Git Shell切换到该路径下(`cd e:\blog`)，然后执行以下指令。

```
hexo init
```

>等待Hexo初始化完成，文件夹中会自动新建所需要的文件夹。
>然后执行

```
npm install
```

　　现在文件已经部署到自己的电脑上了，可以在本地进行查看。

### 本地查看

　　1. 生成完整的网页静态文件，命令为：

```
hexo g
```

>此时目录中会生成一个文件夹，比如在我的目录(`E:\blog`)下生成了一个`public`文件夹，这里面放的就是我们后面要传到GIthub上面的文件。

　　2. 本地生成服务器，命令为：

```
hexo s
```

>效果如下图：

<center>
![](http://ww3.sinaimg.cn/mw690/a9c4d5f6jw1f281r3oadfj20ja01gglh.jpg)
</center>

　　然后在浏览器地址栏中输入：`localhost:4000`，就可以查看最终的效果。这里我就不展示了，因为hexo原本的模板效果我已经没有了，我的博客都已经改为了Jacman模板，之后会说明。

### 部署到Github上

>首先注册帐号

　　Github帐号注册地址：[https://github.com/](https://github.com/)。

>接下来创建仓库(repository)。

<center>
![](http://ww4.sinaimg.cn/mw690/a9c4d5f6jw1f285ea61t5j20rz04kdhf.jpg)
</center>

　　在自己Github主页下点击repository，然后点击new。接下来输入名字，如下图：

<center>
![](http://ww4.sinaimg.cn/mw690/a9c4d5f6jw1f285fjm9fuj20j90ffq3w.jpg)
</center>

>注意这里因为我已经创建过了，所以有错误提示，第一次建立的时候没事。要用自己的用户名加`.github.io`，比如我的就是`yoferzhang.github.io`，名字千万别错。

　　打开之前安装好的Github for windows客户端Github，然后点左上角的加号，选择`Clone`，下面选中刚刚新建的仓库，确定。选择自己喜欢的位置，我直接就放在了E盘根目录下(`E:\`)。这时候E盘下就会生成一个文件夹，我的是`E:\yoferzhang.github.io`。

<center>
![](http://ww2.sinaimg.cn/mw690/a9c4d5f6jw1f285oq0tw0j20fl0e574j.jpg)
</center>

>把刚才Hexo生成的静态文件拷贝到Github生成的文件夹中。

　　我的是`E:\blog\public`文件夹下的所有文件，拷贝到`E:\yoferzhang.github.io`。此时Github客户端就会识别出文件的改变，输入Summary，提交，然后点右上角的`Sync`，第一次`Sync`可能是`Publish`。这时候就可以在浏览器中输入`yoferzhang.github.io`(注意把用户名换成你的)，查看自己的主页。

>官方说明：[https://pages.github.com/](https://pages.github.com/)

>至此你已经可以通过`yoferzhang.github.io`来访问你的网站了，但我们还想用独特的域名。

## 域名和DNS

### 购买域名
>域名我是在GoDaddy上买的，整个购买过程很简单，后面的配置问题再详细说明；我买的是.com域名，毕竟这个识别度高些吧。

[http://www.godaddy.com/](http://www.godaddy.com/)

### DNS
>我用DNSPOD，用QQ就可以登录管理，这个不需要买，但这个需要配置，后面讲到。

[https://www.dnspod.cn/](https://www.dnspod.cn/)

### 配置域名和DNS

　　首先去DNOPOD上面添加自己在GoDaddy上购买的域名。

<center>
![](http://ww3.sinaimg.cn/mw690/a9c4d5f6jw1f28x5vsg18j20j708ugmk.jpg)
</center>

　　然后去GoDaddy官网，登录进入，找到自己的产品，管理域名，设置域名服务器为DNSPod的2个DNS短地址，参考官方说明：
[https://support.dnspod.cn/Kb/showarticle/tsid/42/](https://support.dnspod.cn/Kb/showarticle/tsid/42/)

>PS:官方说明中的图片是比较老的版本，GoDaddy新界面也很好找到相应的设置。

　　下面需要在项目中添加一个名为`CNAME`的文件，可以直接在本地用sublime text新建，比如我在`E:\yoferzhang.github.io`文件夹下建立了一个`CNAME`的文件，里面输入你自己的域名(我输入的内容是`yoferzhang.com`)。至此，你的博客已经可以通过独有域名(http://yoferzhang.com)进行访问了。

## 写博客

　　在你的Hexo文件夹下(我的是`E:\blog`)用Git Shell输入：

```
hexo n "hexo post" #`hexo post`是文件名，自己修改
```

　　就会在`E:\blog\source\_posts`中生成一个`hexo-post.md`文件，这个文件就是你的博文md文件，推荐用`sublime text`编辑，自行寻找sublime添加markdown语法高亮的方法。当然，其他markdown编辑器也非常多，自行取舍。重要的是动手写。

>发布内容到`pulbic`文件夹，最后同理手动复制内容到Github本地仓库目录(`E:\yoferzhang.github.io`)，同步到Github。查看效果。

```
hexo clean
hexo g
```

## 模板

　　大家刚部署好的博客可能和我现在长的不一样，那是因为我使用了Jacman模板，Jacman模板的下载和配置大家可以直接参考原博主：

- [https://github.com/wuchong/jacman](https://github.com/wuchong/jacman)
- [http://wuchong.me/blog/2014/11/20/how-to-use-jacman/](http://wuchong.me/blog/2014/11/20/how-to-use-jacman/)

## 参考文献

>对于其中很多概念不理解的地方可以参考下面的博客。

- 使用GitHub和Hexo搭建免费静态Blog - [http://wsgzao.github.io/post/hexo-guide/](http://wsgzao.github.io/post/hexo-guide/)
- 如何搭建一个独立博客——简明 Github Pages与 jekyll 教程 - [http://cnfeat.com/blog/2014/05/10/how-to-build-a-blog/](http://cnfeat.com/blog/2014/05/10/how-to-build-a-blog/)
- Zippera hexo系列教程 - [http://zipperary.com/categories/hexo/](http://zipperary.com/categories/hexo/)
>Zippera的系列里面有Hexo原模板的详细优化配置。

## 写于最后

　　可能有同学会在Jacman模板的配置那里遇到比较多的问题，我就直接把我的配置贴在这里了，不懂的可以参考一下。

>Hexo配置文件(`E:\blog\_config.yml`)

```
# Hexo Configuration
## Docs: http://hexo.io/docs/configuration.html
## Source: https://github.com/hexojs/hexo/

# Site
title: Yofer Zhang
subtitle: 数学出身，功底扎实，热爱编程，虽然编程起步晚，但是冲劲十足。
description: 接下来自己能够坚持写博客，记录是一个好习惯
author: Yofer
language: zh-CN
timezone:

# URL
## If your site is put in a subdirectory, set url as 'http://yoursite.com/child' and root as '/child/'
url: http://yoferzhang.com
root: /
permalink: post/:title/
permalink_defaults:

# Directory
source_dir: source
public_dir: public
tag_dir: tags
archive_dir: archives
category_dir: categories
code_dir: downloads/code
i18n_dir: :lang
skip_render:

# Writing
new_post_name: :title.md # File name of new posts
default_layout: post
titlecase: false # Transform title into titlecase
external_link: true # Open external links in new tab
filename_case: 0
render_drafts: false
post_asset_folder: false
relative_link: false
future: true
highlight:
  enable: true
  line_number: true
  tab_replace:

# Category & Tag
default_category: uncategorized
category_map:
tag_map:

# Date / Time format
## Hexo uses Moment.js to parse and display date
## You can customize the date format as defined in
## http://momentjs.com/docs/#/displaying/format/
date_format: YYYY-MM-DD
time_format: HH:mm:ss

# Pagination
## Set per_page to 0 to disable pagination
per_page: 10
pagination_dir: page

# Extensions
## Plugins: http://hexo.io/plugins/
## Themes: http://hexo.io/themes/
theme: jacman

# Deployment
## Docs: http://hexo.io/docs/deployment.html
deploy:
  type: git
  repository: https://git.coding.net/yoferzhang/yoferzhang.git
  branch: coding-pages

# Others
index_generator:
  per_page: 10 ##首页默认10篇文章标题 如果值为0不分页

archive_generator:
    per_page: 0 ##归档页面默认10篇文章标题
    yearly: true  ##生成年视图
    monthly: true ##生成月视图

tag_generator:
    per_page: 0 ##标签分类页面默认10篇文章

category_generator: 
    per_page: 0 ###分类页面默认10篇文章

feed:
    type: atom ##feed类型 atom或者rss2
    path: atom.xml ##feed路径
    limit: 20  ##feed文章最小数量
```

>上面repository里面我没有填github，而是coding的地址，是因为我换到coding部署了，毕竟github国内访问会稍慢。下一篇说一下转到coding配置的问题。

>Jacman配置文件(`E:\blog\themes\jacman\_config.yml`)

```
##### Menu
menu:
  主页 | Home: /
  索引 | Index: /index
  归档 | Archives: /archives
  关于 | About: /about
## you can create `tags` and `categories` folders in `../source`.
## And create a `index.md` file in each of them.
## set `front-matter`as
## layout: tags (or categories)
## title: tags (or categories)
## ---

#### Widgets
widgets: 
- github-card
- category
- links
- douban
- rss
- weibo
  ## provide eight widgets:github-card,category,tag,rss,archive,tagcloud,links,weibo



#### RSS 
rss: /atom.xml ## RSS address.

#### Image
imglogo:
  enable: true             ## display image logo true/false.
  src: img/logo.jpg        ## `.svg` and `.png` are recommended,please put image into the theme folder `/jacman/source/img`.
favicon: img/faviconr.ico   ## size:32px*32px,`.ico` is recommended,please put image into the theme folder `/jacman/source/img`.     
apple_icon: img/jacman.jpg ## size:114px*114px,please put image into the theme folder `/jacman/source/img`.
author_img: img/author.jpg ## size:220px*220px.display author avatar picture.if don't want to display,please don't set this.
banner_img:  #img/banner.jpg ## size:1920px*200px+. Banner Picture
### Theme Color 
theme_color:
    theme: '#9933FF'    ##the defaut theme color is blue

# 代码高亮主题
# available: default | night
highlight_theme: night

#### index post is expanding or not 
index:
  expand: false           ## default is unexpanding,so you can only see the short description of each post.
  excerpt_link: Read More  

close_aside: false  #close sidebar in post page if true
mathjax: false      #enable mathjax if true

### Creative Commons License Support, see http://creativecommons.org/ 
### you can choose: by , by-nc , by-nc-nd , by-nc-sa , by-nd , by-sa , zero
creative_commons: none

#### Author information
author:
  intro_line1:  "Hello ,I'm Yofer Zhang in Tencent."    ## 网站底部的个人介绍
  intro_line2:  "This is my blog,thank you to here."  
  weibo_verifier:  ## 微博秀的验证码
  tsina:  ## 用于微博秀和微博分享
  weibo:  ## 用于显示网站底部社交按钮，下同
  douban:  ## 是从豆瓣个人主页拔下来的：https://www.douban.com/people/zyq522376829/        
  zhihu:  ## 同上：https://www.zhihu.com/people/yoferzhang
  email:    
  twitter:  
  github:    
  facebook: 
  linkedin: 
  google_plus: 
  stackoverflow: 
## if you set them, the corresponding  share button will show on the footer

#### Toc
toc:
  article: true   ## show contents in article.
  aside: true     ## show contents in aside.
## you can set both of the value to true of neither of them.
## if you don't want display contents in a specified post,you can modify `front-matter` and add `toc: false`.

#### Links链接
links:
  Hexo: https://hexo.io/
  Github: https://github.com/yoferzhang



#### Comment 评论
duoshuo_shortname: yoferzhang
disqus_shortname:     ## e.g. wuchong   your disqus short name.

#### Share button 分享按钮
jiathis:
  enable: false ## if you use jiathis as your share tool,the built-in share tool won't be display.
  id:    ## e.g. 1889330 your jiathis ID. 
  tsina: ## e.g. 2176287895 Your weibo id,It will be used in share button.

#### Analytics 网站统计
google_analytics:
  enable: false
  id:        ## e.g. UA-46321946-2 your google analytics ID.
  site:      ## e.g. wuchong.me your google analytics site or set the value as auto.
## You MUST upgrade to Universal Analytics first!
## https://developers.google.com/analytics/devguides/collection/upgrade/?hl=zh_CN
baidu_tongji:
  enable: true
  sitecode:  ## e.g. e6d1f421bbc9962127a50488f9ed37d1 your baidu tongji site code
cnzz_tongji:
  enable: false
  siteid:    ## e.g. 1253575964 your cnzz tongji site id



#### Miscellaneous
ShowCustomFont: true  ## you can change custom font in `variable.styl` and `font.styl` which in the theme folder `/jacman/source/css`.
fancybox: true        ## if you use gallery post or want use fancybox please set the value to true.
totop: true           ## if you want to scroll to top in every post set the value to true


#### Custom Search
google_cse: 
  enable: false
  cx:   ## e.g. 018294693190868310296:abnhpuysycw your Custom Search ID.
## https://www.google.com/cse/ 
## To enable the custom search You must create a "search" folder in '/source' and a "index.md" file
## set the 'front-matter' as
## layout: search 
## title: search
## ---
baidu_search:     ## http://zn.baidu.com/
  enable: false
  id:  ## e.g. "783281470518440642"  for your baidu search id
  site: http://zhannei.baidu.com/cse/search  ## your can change to your site instead of the default site
  
tinysou_search:     ## http://tinysou.com/
  enable: false
  id:  ## e.g. "4ac092ad8d749fdc6293" for your tiny search id

swiftype:     ## https://swiftype.com/
  enable: true
```

>里面涉及到我自己一些帐号的问题我就删掉了