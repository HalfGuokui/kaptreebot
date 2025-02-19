# kaptreebot机器人开源

## 关于项目

本项目基于[nonebot2](https://v2.nonebot.dev/)框架，采用[go-cqhttp]( https://github.com/Mrs4s/go-cqhttp)协议，python3语言编写的

## 关于配置
如果你是一个纯小白，那么请先下载[python3]( https://www.python.org/)，记得勾选环境变量的选项
如果你已经配置好python环境，那么请安装nonebot2 -> 打开你的cmd，(需要注意的是这里装的环境是实体环境，如果你要做二次开发请在你的虚拟环境，IDE的终端继续安装下面的库)
然后输入`pip install nb-cli`

然后输入`nb driver install aiohttp`和`nb driver install websockets`安装驱动器

然后输入`nb adapter install nonebot-adapter-onebot` 安装适配器

接着输入`pip install requests requests_html Pillow ffmpeg lxml`

然后输入`nb plugin install nonebot_plugin_apscheduler`

后续就根具你的需求自己安装库啦

## 使用说明
1.请先配置好go-cqhttp协议(只用修改我文件夹的config.yml文件里面)，当然这个我这里配置好了的，你只需要更改QQ的UIN(账号)和password(密码)即可(这里是机器人的账号和密码)
&nbsp;

2.在py编译器打开kaptreebot文件夹，然后运行bot.py文件

&nbsp;
如果没有py编译器的话，为了你运行方便，我写了个begin.bat，双击它也能运行(当然无论哪种方式你都要有py环境)

3.在我的kaptreebot目录下面有两个文件.env.dev和.env.prod，请在里面修改成你的QQ号（这里是权限账号）



# 从0开始学习视频连接:

## 一、Nonebot+go-cq环境搭建

[www.bilibili.com/video/BV1DP4y1W7ji](https://www.bilibili.com/video/BV1DP4y1W7ji)

## 二、nonebot聊天bot的插件编写
[www.bilibili.com/video/BV1dM4y157Zk](https://www.bilibili.com/video/BV1dM4y157Zk)

## 三、nonebot2插件编写完结

[www.bilibili.com/video/BV13h411B7eN](https://www.bilibili.com/video/BV13h411B7eN)

## 四、Linux部署bot机器人

[www.bilibili.com/video/BV1gQ4y1U7v9](https://www.bilibili.com/video/BV1gQ4y1U7v9)

![image-20210818144520047](image-20210818144520047.png)

## 目前实现功能
|功能                   | 使用方法 |
| ---- | ---- |
|1.B站直播第一时间发消息                        | eg:如果想修改成自己的直播间需要去bilbili.py 文件中修改|
|2.天气查询                        | eg:天气 成都|
|3.单词翻译                         | eg:翻译 我逢考必过 (目前已实现句子翻译) |
|4.戳一戳                              | eg:手机戳我头像|
|5.每日一图                             | eg:每日一图/mc酱/R18|
|6.我要抱抱                              |eg:我要抱抱/我要亲亲|
|7.朋友圈文案/彩虹屁/开始网抑    | eg:“/开始网抑，/彩虹屁，/朋友圈文案”|
|8.情感语录 && 毒鸡汤                   | eg:情感语录/毒鸡汤/舔狗日记 (关键词匹配) |
|9.智能回复                             | eg:你随便问什么都会有回复(在群里问的时候记得@她或者/她) |
|10.语音回复                             | 通过你和她对话，可能会触发设置的语音(触发条件请参考 语音调用.txt) |
|11.ph制图				|eg:ph 芜 湖 |
|12.表情包搜索			|eg: 表情包 就这 |
|13.王者荣耀出装搜索			|eg: 王者荣耀 李白 |
|14.随机短视频播放		|eg: 短视频 |
|15.抽签小游戏		|eg: 抽签 |
|16.早报和节日推送		|每天自动推送到群里 |
|17.运气王@出来		|红包领完后就会@运气王 |
|18.DOJ用户查询|eg：DOJ kaptree 或者 find kaptree，参数数在DreamOJ上面的**用户名**|
|19.各大OJ最近三场比赛|eg： 最近比赛|
|20.分享关于最近一场Codeforces的比赛|eg：cf|
|21.每日一题|每天自动发送到群聊中，当然也可以使用命令：`每日一题`|
|22.To be continue……                    |还有一些彩蛋等你触发哦，eg:指令：绿茶，情话 |




## 关于作者
作者: Mangata
QQ:1196991321
作者的交流群: [传送门]( https://jq.qq.com/?_wv=1027&k=UwKSTvSn)
作者的博客 [传送门]( https://www.cnblogs.com/Mangata/)

## 感谢人员
感谢对我指导的群友，还感谢群里帮我测试的同学@zoey,@Untergehen

快来star我吧

后续有时间的话，我会更新的(可能跟新的周期有点长 To Be Continue……

&nbsp;
&nbsp;
&nbsp;

## 关于bug
1.在你打开bot的时候可能bot会主动给好友发一些消息，这个bug是go-cqhttp框架的作者的问题，从最开始到现在这个问题并没有得到有效的解决

2.目前由于go-cqhttp作者的问题，写了一个新的消息类型，但是这个消息类型并不被nonebot2支持，所以会出现报错但是不影响使用的情况，请忽略即可，等nonebot2的版本更新即可解决

3.还有一些潜在的bug，我不能保证我写的代码一点问题都没有，所以如果有代码还请在issue处或者直接加入我的交流群告诉我，阿里嘎多

## 更新

### 版本0.8 -2022.2.27
1.适配了最新Nonebot版本的b2

2.增加了一个关于DreamOJ查询的插件

3.新增最近比赛、cf比赛等插件

4.新增了一个随时捕获B站直播状态插件

5.修复了一些不能使用的插件

### 版本0.7 -2021.8.19

1.更新了每日一图的API，更加好看(se)了（逃

2.新增了表情包搜索

3.新增了王者荣耀英雄出装搜索

4.新增了随机短视频播放

5.新增了一个抽签小游戏

6.新增了每天早上60s看世界播报，并且推送今天的节日

### 版本0.6 &nbsp;&nbsp;&nbsp;&nbsp;-2021.6.11 
1.更新了一个ph制图的小功能
2.新增了几个定时任务
……
### 版本 0.5  &nbsp;&nbsp;&nbsp;&nbsp;-2021.2.26 
1.首先是关于智能闲聊机器人，之前用的是图灵，但是图灵好贵，作为学生的我还支付不起，所以我把闲聊机器人换成了[小思机器人](https://console.ownthink.com/)，重写了bot的API调用(现在每天调用次数无上限了，还免费，嘿嘿)

2.关于每日一句我也更新了，将金山的每日一句换成了[一言](https://pa-1251215871.cos-website.ap-chengdu.myqcloud.com/)，一言在调用和语句数目上面有很大的优势

3.新增了两个爬虫，爬取一个个网站的[情话部分](https://lovelive.tools/)以及[绿茶语句部分](https://lovelive.tools/)

4.翻译部分，我取消使用之前的翻译爬虫，使用了百度翻译API(每个月有100w免费的翻译字数)，实现了之前不能翻译句子的问题，但是目前我只做了仍和语种翻译成英语，后面有时间更新

5.关于图片的API，我新增了R18，关于句子的API，我新增了朋友圈文案、彩虹屁、网易语录等功能

6.不知不觉又是第二天凌晨了，今天也是元宵节，祝各位元宵节快乐😘😘😘 &nbsp; &nbsp;-2021.2.26.0:20

### 版本 0.4  &nbsp;&nbsp;&nbsp;&nbsp;-2021.2.23
1.修复了bot自己调用自己的bug

2.新增了50条，部分关键词，部分命令的语音发送(注意:私聊的时候手机端收不到语音消息，电脑端能收到，群聊的时候都能看到，这个bug应该是go-cqhttp的作者写出了bug)

3.更新了go-cqhttp的版本


### 版本 0.3 &nbsp;&nbsp;&nbsp;&nbsp;-2021.2.22
1.更新了语音发送(但是这个mp3文件云盘还未找到，实在找不到，到时候自己写一个了)

2.将代码的priority全部重新编写

3.添加了图灵机器人API,让bot聊天更加智能，但是每天只能使用100次(后面会转腾讯/百度)


### 版本 0.2 &nbsp;&nbsp;&nbsp;&nbsp;-2021.2.18
1.更新了爬虫 舔狗日记/毒鸡汤/社会语录

2.将许多命令都改成了关键词匹配 eg: 每日一图、情感语录、mc酱等等

3.添加了 @群红包最后一位领取的成员

4.更新了群消息撤回后发送调戏消息

5.更新了好友添加自动同意功能

6.更新了文档信息(关于小白配置自己的机器人)
