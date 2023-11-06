---
title: GPT4.0使用体验：越来越牛的AI
categories:
  - 思考
toc: true 
date: 2023-09-21
thumbnail: https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/%E6%80%9D%E8%80%83%201.png
---

今年ChatGPT、Midjourney等工具的发展掀起了一股AI热潮。在我试用了一段时间后明显能够感受到GPT-3.5在自然语言、信息检索、辅助创作等方面确实大幅领先了传统ai工具。但它并不完美，一方面，它有时会给出看似合理但实际错误的答案，并且没有数据来源去验证回答的真实性；另一方面，在内容创作上GPT-3.5仍显现出较低的水平，这也许就是人类最难被ai取代的地方。

3.5差强人意，4.0是否会有更好的表现？出于好奇我又试用了下GPT-4。前沿科技体验起来有些许昂贵，白嫖党选择试玩搭载GPT-4内核的New Bing。

首先弄清楚GPT-4相比于GPT-3.5主要进步在哪些方面：

![image-20230912161845545](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/image-20230912161845545.png)

可以看到GPT-3.5明显给出了错误的信息，GPT-4.0早在今年3月便已发布，3.5却回答尚未发布，而4.0给出了我们想要的答案，简单总结一下4.0的进步之处：

- 多模态模型，能更好地理解图像、音频等非文本信息
- 能处理更复杂的任务
- 更好的性能，更强大的创造力
- 更可靠

下面我们分别测试一下这几个方面。

### 图像处理

开胃小菜，**图生文**：

![image-20230918172218730](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/image-20230918172218730.png)

（。。。。。。。。。。。。文言文这一段太过抽象）

通过图片信息编写一段故事脚本：

![image-20230921110622423](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/image-20230921110622423.png)

（迪士尼编剧：？）接着看下**图像推理**方面，AI能否通过图片推理出一些简单信息：

![image-20230918185900061](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/image-20230918185900061.png)

![image-20230918190632661](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/image-20230918190632661.png)

### 复杂任务处理

找了几个难度不等的逻辑推理问题来试试4.0的含金量：

Q1：一楼到十楼的每层电梯门口都放着一颗钻石，钻石大小不一。你乘坐电梯从一楼到十楼，每层楼电梯门都会打开一次，只能拿一次钻石，问怎样才能拿到最大的一颗？

![image-20230918174751400](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/image-20230918174751400.png)

Q2：1元钱一瓶汽水，喝完后两个空瓶换一瓶汽水，问：你有20元钱，最多可以喝到几瓶汽水？

![image-20230918182302328](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/image-20230918182302328.png)

Q3：There are 9 birds in the tree,the hunter shoots one,how many birds are left in the tree?

![image-20230918182809566](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/image-20230918182809566.png)

此外我还发现bing chat已经能够解析网页和文档内容并总结出要点。具体做法：1、用edge打开pdf；2、点开bing chat的窗口；3、输入指令即可。

![image-20230919155224950](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/image-20230919155224950.png)

让人口水直流的功能🤩甚至能让他写一段读后感，体验一把中学语文老师...

![image-20230919155912634](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/image-20230919155912634.png)

### 创造力

#### 图像创作

Q1：请帮我画一张猫的画，关键词：美漫风、凶猛、帅气、戴着骑士帽

![image-20230912172559506](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/image-20230912172559506.png)

视觉表现力还不错，有midjourney的味道了。特别要提的一点是，Bing Chat可以根据原始问题提供一系列衍生问题，顺着这些问题我们可以不断完善图画：

![image-20230912180232924](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/image-20230912180232924.png)

#### 文案写作

Q1：我面前有一杯白开水，请帮我写一段富有创意的广告宣传语，突出他的特质，激发人们的购买欲

![image-20230919155525135](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/image-20230919155525135.png)

再来一个复杂一点的，能看出有明显差距：

![image-20230919161636523](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/image-20230919161636523.png)

#### 编程

正好最近在学processing，看看ai能否写出有趣的代码

Q1：请帮我写一段processing的代码，我希望画面具有视觉冲击力，生动有趣

![image-20230921110231490](https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/image-20230921110231490.png)

仅从视觉上来看，3.5似乎有更好的表现，但4.0的图案是通过鼠标运动来绘制的，多一个交互性。再看下面一个例子（左：GPT-3.5，右：GPT-4.0）

<div> <img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/iShot_2023-09-21_11.10.30.gif" width="560px"/>   <img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/output.gif" width="425" /></div>

除了能写代码，ai还能根据代码进行反向推导，并为代码添加注释、debug。如图所示，即使我故意录入了一段重复错误的代码，ai也能输出正确结果，甚至还分析了代码潜在的问题。Bing更进一步地给出了潜在问题的修改建议和代码，这一点体验真的太好了。

GPT-3.5:

<div align="center"><img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/iShot_2023-09-21_11.41.03.png" alt="iShot_2023-09-21_11.41.03" width="640"/></div>

GPT-4.0:

<div align="center"><img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/iShot_2023-09-21_14.16.01.png" alt="iShot_2023-09-21_14.16.01" width="600"/></div>

在带有玩票性质地，粗略地体验了下GPT-3.5、GPT-4.0后，我发现自己已经对它形成了路径依赖。当我想要快速了解一个新的行业时，以前需要花费大量时间去不同平台搜寻信息，还要甄别信息的时效性。现在有了GPT，它能帮我快速从网络世界中找到最新的有效信息，极大程度上降低了我的时间成本。

在享用ai带来的便利的同时，网上也会有很多声音担心人类迟早会被ai取代。个人认为在可预见的未来内，这种事只会发生在个别行业群体，并不具备普世性。举个例子，大型农业机械本身是非常落后的技术，如果在中国按照黑龙江的标准推广大型农业机械，全中国的耕地只要几百万职业农民就能种完，多出来的上亿人怎么办？这才只是黑龙江的标准，要是按照美国标准去推广，连这几百万里的90%都得失业。现在这上亿人并没有失去营生上街打砸，而是仍然在村里岁月静好，显然这里面有技术之外的看不见的手在发挥着作用。

不仅仅在中国，全世界哪怕是英美这样的发达国家，仍然有极大比例的人每天在使用中世纪的生产方式进行办公，即使一个脑子机灵点的应届大学生都完全有能力去优化这些工作的流程，从而裁掉这当中的绝大部分百万漕工。为什么没有呢？显然这里面有技术之外的看不见的手在发挥着作用。

