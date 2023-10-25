---
title: 个人博客的搭建及写作
categories:
  - 技术
toc: true
date: 2023-03-01
thumbnail: https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/%E6%8A%80%E6%9C%AF%201.png
---
## 如何搭建个人博客
### 买域名
- [godaddy.com](https://sg.godaddy.com/)
- [https://buy.cloud.tencent.com/domain](https://buy.cloud.tencent.com/domain)

### 代码托管
github：[https://github.com/](https://github.com/)
图形化界面管理：GitHub desktop

### 部署平台-Vercel
1. add new project
2. import
3. browse all templates>hexo>deploy

### 博客框架：hexo
静态博客：

- [Hexo](https://hexo.io/zh-cn/) (https://hexo.io/zh-cn/)
- [Hugo](https://www.gohugo.cn/) (https://www.gohugo.cn/)
- [VuePress](https://www.vuepress.cn/) (https://www.vuepress.cn/)
- [Jekyll](https://www.jekyll.com.cn/) (https://www.jekyll.com.cn/)

动态博客：
- [WordPress](https://wordpress.org/) (https://wordpress.org/)
- [Typecho](https://typecho.org/) (https://typecho.org/)
- [Halo](https://halo.run/) (https://halo.run/)

> 所谓的动态网页，是指跟静态网页相对的一种网页编程技术。静态网页，随着html代码的生成，页面的内容和显示效果就基本上不会发生变化了——除非你修改页面代码。而动态网页则不然，页面代码虽然没有变，但是显示的内容却是可以随着时间、环境或者数据库操作的结果而发生改变的

![image.png](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1676629134769-0ad92cbd-d0e1-40a0-b500-8a2a806a7ece.png)

**Hexo**
Hexo 是一个基于Node.js的快速、简洁且高效的静态博客框架。Hexo 使用 Markdown（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。Hexo具有丰富的主题、插件系统。
**优点**
- 纯静态博客，部署简单、成本低廉、运行优化非常高效。
- Hexo 静态博客框架可以在云端，也可以在本地电脑上甚至手机上。
- Hexo 框架的博客网站没有网站后台，不存在后台安全漏洞的问题。
- 因为是纯静态的，几乎所有的 CDN 服务都可以完美的加速提升浏览速度。
- 搜索引擎对纯静态网站有天然的青睐度，收录、权重优先权明显。
- 纯静态网站会让网络攻击成本大大的增加也就是说纯静态网站被攻击的可能性更低了

### 安装git：
1. [https://git-scm.com/downloads](https://git-scm.com/downloads)
2. git --version
如果电脑自带git，会提示如下:
![image.png](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1676621557837-408315de-e7b2-47b0-bba8-f4b38682ca69.png)
如果电脑没有没有git，系统可能会给出如下提示信息：
![image.png](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1676621697517-2a736aac-91fa-497b-ab5c-33e4d10a55a8.png)

3. 利用 brew 工具包管理器进行 git 安装，如果本机没有 brew，可以使用如下命令安装：
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
安装完成后，就可以安装 git 工具，执行命令如下：
```
brew install git
```

### 安装node.js
地址：[https://nodejs.org/zh-cn/download/](https://nodejs.org/zh-cn/download/)
**查看下Git、Node.js版本，确保安装无误**：
```
git --version 
node -v   
npm -v 
```
### 安装Hexo
```
npm install -g hexo-cli
```
目录权限问题：
<div align="left"><img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1676622322727-320648f9-7a5d-48c5-bab8-df99dfcbdfbc.png" width="700px"></div>

修改目录文件权限：
```
chmod -R 777 /usr/local/lib
```
mac直接：
```
sudo npm install hexo-cli -g
```
出现如下提示代表安装成功：
<img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1676622768831-690df981-ed84-4213-85af-df4718312ffa.png" alt="image.png" style="zoom:67%;" />

也可以check一下：
```
hexo -v
```
<div align='left'><img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1676622854789-8cf51416-663d-46d3-bb5e-92d6a83c5a3e.png" alt="image.png" style="zoom:50%;" /></div>

首先我们需要新建一个项目目录，例如在桌面的code目录下新建一个HexoBlog文件夹用于存放该项目相关文件:
```
cd  /Users/stephen/Desktop/code 
cd myblog&&mkdir myblog
```
mkdir：创建文件夹<br />cd：进入文件夹<br />初始化博客
```
hexo init 
```
进入文件夹，安装一下npm：
```
cd myBlog 
npm install
```
<div align='left'><img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1676626249515-a4ee6da3-56cb-44c0-911b-55c2250f19e9.png" alt="image.png" style="zoom:60%;" /></div>

初始化成功！可以在文件夹里找到如下文件：
<div align='left'><img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1676626460861-b25a9f99-c558-46e1-a755-720909e1dba9.png" alt="1676626460861-b25a9f99-c558-46e1-a755-720909e1dba9" style="zoom:50%;" /></div>

node_modules：用来存储已安装的各类依赖包
scaffolds：博客模版文件夹，包含page.md，post.md，draft.md三种
source：资源文件夹，存放静态资源如博客md文件、图片等
themes：主题文件夹，Hexo通过将网站内容与主题组合来生成静态网站
package-lock.json：包版本依赖锁文件
package.json：应用数据，Hexo的版本以及相关依赖包的版本等
config.landscape.yml：主题配置文件 
config.yml：站点配置文件，对站点进行配置
hexo指令：[https://hexo.io/zh-cn/docs/commands](https://hexo.io/zh-cn/docs/commands)

### 更换博客主题
```
cd /Users/stephen/Documents/GitHub/myblog
```
```
git clone https://github.com/cofess/hexo-theme-pure.git themes/pure
```
打开_config.yml，更改主题名称
theme: xxxx

### 本地查看博客
生成页面，每次你加入了一篇新博客的时候，都要生成一次
```
hexo g
```
进入myblog文件夹，启动本地服务：
```
cd /Users/stephen/Documents/GitHub/myblog
hexo s
```
浏览器输入：localhost：4000 即可看到 （172.20.10.3:4000）

### 添加live2d模型
安装
```
npm install --save hexo-helper-live2d
```
在 hexo 的 config.yml中添加参数：
```
live2d:
enable: true
  scriptFrom: local
  pluginRootPath: live2dw/
  pluginJsPath: lib/
  pluginModelPath: assets/
  tagMode: false
  log: false
  model:
    use: live2d-widget-model-‘模型名字’
  display:
    position: right
    width: 150
    height: 300
  mobile:
    show: true
```
下载模型
```
npm install --save live2d-widget-model-`模型名字`
```
其他模型：
- live2d-widget-model-hijiki
- live2d-widget-model-hibiki
- live2d-widget-model-tororo

运行！

安装包
```
sudo npm install -g yuque-hexo
```

### 零散的知识点
' ' 前需要加空格
<img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1677059600655-082fa697-7f2a-4960-af53-6db62880a1cb.png" alt="image.png" width="200px" />
#### 关闭search:
/Users/stephen/Desktop/myblog/themes/pure/layout/_search
复制index.ejs作备份index2.ejs，将原index.ejs内容删除
#### 关闭文章下的版权说明/自我介绍
/Users/stephen/Desktop/myblog/themes/pure/layout/_partial/post
复制copyright.ejs作备份copyright2.ejs，将原copyright.ejs内容删除
#### 删除文章底部的捐赠、目录开关
<img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1677750277771-8c25d5b8-9451-4352-b8de-c30de375e92a.png" alt="image.png" style="zoom:67%;" />  <br>/Users/stephen/Desktop/myblog/themes/pure/layout/_partial/post
打开nav.ejs文件，删除相关代码：

```
 <% if (theme.donate.enable){ %>
  <!-- Button trigger modal -->
  <button type="button" class="btn btn-fancy btn-donate pop-onhover bg-gradient-warning" data-toggle="modal" data-target="#donateModal"><span><%= __('donate.button') %></span></button>
  <!-- <div class="wave-icon wave-icon-danger btn-donate" data-toggle="modal" data-target="#donateModal">
    <div class="wave-circle"><span class="icon"><i class="icon icon-bill"></i></span></div>
  </div> -->
  <% } %>
  
  <div class="bar-right">
    <% if (theme.share.enable){ %>
    <div class="share-component" data-sites="<%= theme.share.sites %>" data-mobile-sites="<%= theme.share.mobile_sites %>"></div>
    <% } %>
  </div>
  </div>
```
```
 <% if (!index && theme.config.toc && post.toc) { %>
    <li class="toggle-toc">
      <a class="toggle-btn <% if(!theme.config.autoUnfold){%>  collapsed  <%}%>" data-toggle="collapse" href="#collapseToc" aria-expanded="false" title="<%= __('article.catalogue') %>" role="button">    <span>[&nbsp;</span><span><%= __('article.catalogue') %></span>
        <i class="text-collapsed icon icon-anchor"></i>
        <i class="text-in icon icon-close"></i>
        <span>]</span>
      </a>
    </li>
    <% } 
%>
```

#### 目录样式
.../theme/pure/source/css/# style.css
调整文字与icon的距离：
<img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1677834422048-6cebf6de-6016-48bc-9268-bc09ee8b4fd5.png" alt="image.png" style="zoom:67%;" />
调整页边距：
<img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1677834515716-b31654ad-adea-4121-a859-d4e6745eacf8.png" alt="image.png" style="zoom:67%;" />

#### 关闭文章目录编号

将 sidebar-toc.ejs 中的
<%- toc(post.content) %>
改成
<%- toc(post.content, {list_number: false}) %>

#### 文章插入图片

1、下载插件
```
npm install https://github.com/CodeFalling/hexo-asset-image --save
```
注意 不要使用npm install hexo-asset-image --save这个命令安装,版本号不对<br />2、把_config.yml中的post_asset_folder设为true<br />这个配置的意思是每次new post一个博客，会增加一个和博客同名的文件夹
```
hexo new post <title>
```
3、把图片放到.md文件的同名文件夹里，最后在.md文件中引用图片
```
![图片描述]（./文件夹名/文件名.jpg）
```
调整图片大小
```
<img src="图片名称.jpeg" alt="提示词"  width="600"/>  
```

#### 关闭评论
/Users/stephen/Desktop/myblog/themes/pure/layout/script/comment.ejs<br />script: true --> script: false<br /><img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1681283233779-f6d71a33-e647-4db8-a453-40aa49740ac2.png" alt="image.png" style="zoom:60%;" /><br />关闭list的评论按钮：<br />/Users/stephen/Desktop/myblog/themes/pure/layout/partial/archive-post.ejs<br /><img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1681358721855-b894bf5d-429a-4269-9fef-2eaa706e2b20.png" alt="image.png" /><br />关闭文章头部的评论按钮<br />/Users/stephen/Desktop/myblog/themes/pure/layout/partial/article.ejs<br />![image.png](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1681358721855-b894bf5d-429a-4269-9fef-2eaa706e2b20-20230614143001708.png)

#### css样式
多个div并排方法：
1、display：inline
2、float，清除float对父元素的影响：**在父元素设置 overflow：auto**
3、position：absolute



## 如何让写blog更轻松

### markdown语法
很多工具都h支持markdown写作，我自己常用obsidian和typora，配合picgo和云服务器能大幅提高图片管理效率
基础教程：
[Markdown 教程 | 菜鸟教程](https://www.runoob.com/markdown/md-tutorial.html)
进阶教程：
[Markdown笔记 | 一篇最详细的Markdown 教程 --> 收好-腾讯云开发者社区-腾讯云](https://cloud.tencent.com/developer/article/1461211)

### typora+picgo+腾讯云COS
它山之石：[手把手教你Typora图床配置(PicGo+阿里云OSS/腾讯云COS)-阿里云开发者社区](https://developer.aliyun.com/article/1231108?spm=5176.26934562.main.1.ccc631baBG4cLH#slide-4)
配置过程稍微有点复杂，但是配置完成后，用typora写文章时，只需要将图片拖到typora，就能自动上传到云服务器（即图床)并生成可访问的URL，写作体验直线上升！！
首先准备好三个工具:
1. 安装typora，[下载地址](https://typoraio.cn/)
2. 安装picgo，[下载地址](https://github.com/Molunerfinn/PicGo/releases?spm=a2c6h.12873639.article-detail.4.45b6d5c5fSTnnk)
3. 注册、登录[腾讯云](https://cloud.tencent.com/)

#### picgo关联typora
第一步：检查一下server是否打开，目前默认都是打开的

![image.png](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1686653754937-d2e40952-16ac-47ad-b364-ce94e7eb0b69.png)
![image.png](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1686653771438-7f6a3551-91be-40cf-bcac-ea4a3a4a336b.png)
可以选择需要显示的图床，默认全部勾选的，建议用哪个勾选哪个![image.png](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1686654128075-b00da7e2-e5c4-41bb-a596-a019cd564854.png)
第二步：打开typora的设置，1、选择图像；2、插入图片时：上传图片；3、上传服务：picgo.app
![image.png](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1686653965172-27026c85-616f-4f63-ad8a-290db367ff26.png)

#### 腾讯云COS搭建图床
**购买cos服务**
注意新用户有优惠，1元享50G/年存储容量
![image.png](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1686654401063-85c935ff-8b4b-490e-904d-5cdcd7a4e2d2.png)
**创建bucket**
配置如图，其中区域可以选择附近的城市
![image.png](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1686654792266-dd87e421-5d41-4e85-ab66-e10b87348aa4.png)
**申请密钥**
前往[个人中心](https://console.cloud.tencent.com/cam/capi?spm=a2c6h.12873639.article-detail.128.76a7d5c55bvpD8)，新建密钥拿到SecretId和SecretKey
![image.png](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1686655057694-e21336fb-bd31-4ad5-8989-d48ac0c8633a.png)
到这里我们能得到的东西有：
- SecretId、SecretKey
- APPID
- bucket名称
- 所在区域（存储区域）

最后一步，打开picgo的设置>图床设置/腾讯云COS，将所需信息填入即可，注意：存储路径为在bucket中创建的文件夹名。
![image.png](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/1686655331276-b7eeacdb-c282-4bfc-be43-42732bc4932e.png)