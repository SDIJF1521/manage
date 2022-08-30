# manage
这是基于mysql数据库用来管理群的插件如果您要使用这个插件请保证您的电脑上面有mysql数据库
插件使用方法如下:

首先先下载文件然把文件里面的两个py文件放入机器人的plugins文件夹
[![vfzMeU.png](https://s1.ax1x.com/2022/08/30/vfzMeU.png)](https://imgse.com/i/vfzMeU)

将文件放入文件夹后需要在mysql数据库里面创建一个名为qqai的数据库(这里我推荐一个图形化管理mysql的工具Navicat 15 for MySQL这个工具用来管理mysql很方便但是要付费才可以使用如果你想免费使用可以去看一下这个视频https://www.bilibili.com/video/BV1H44y1W7F9?spm_id_from=333.880.my_history.page.click&vd_source=832a4d4cc4c7b9c9a6cff589f41803ed)qqqq数据库内要在创建两张表，表名分别为gl；word
[![vfzQwF.png](https://s1.ax1x.com/2022/08/30/vfzQwF.png)](https://imgse.com/i/vfzQwF)

gl的字段为admin类型为varchar
[![vfztQx.png](https://s1.ax1x.com/2022/08/30/vfztQx.png)](https://imgse.com/i/vfztQx)

word的字段为wordlist类型为varchar
[![vhSP6x.png](https://s1.ax1x.com/2022/08/30/vhSP6x.png)](https://imgse.com/i/vhSP6x)

到这里数据库就配置好了
数据库配置好后要修改部分源码
要修改的部分分别是
不良语句撤回.py文件的29行71和104行，群管理系统.py的29行43行44行58行59行116行的群号改为自己的群号，群管理系统.py 86行写入群主QQ

如上操作完插件就可以使用了
本插件有如下功能
群禁言 OFF
群禁言 NO
禁言
不良言语撤回功能（支持在QQ群内添加或删除语言词汇）

在使用插件前先在群内使用刷新命令这样做是为了给所有群管理添加此模块的操作权限

查看命令方式输入群管理菜单即可


单人禁言语法如下：禁言 @禁言的人 禁言时间（以分为单位）若要放出将时间设置为0即可

多人禁言语法如下：禁言 @禁言的人 禁言时间| @禁言的人 禁言时间 若要放出将时间设置为0即可

不良言语撤回功能刚开始使用请用*命令进行不词汇添加添加语法如下:                     
单个添加：         \*词汇                
多个添加：         \*词汇|词汇

若要删除某个词汇请这样做：
单个删除：     -*词汇         多个删除：    -*词汇|词汇
添加完毕后普通成员只要一句话里面有这些词汇就会被机器人撤回，但是若身份为管理成员则不会
