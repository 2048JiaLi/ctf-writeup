[TOC]

# 2024年獬豸(xiè zhì)杯

## 写在前面：

笔者属于新手，还有许多需要学习的地方，不喜勿喷。本篇WP目的在于介绍，使用非**取证大师**、**火眼**等授权软件的解法，全部使用**开源或免费工具**解题（部分题解是赛后学习得到，个人成绩为88名，前20%），并附上工具地址！！

- 官方通告如下：

<img src=".\images\官方.jpg" style="zoom:25%;" />

比赛于2024年1月28日9-12时比赛，全程三小时时间（对于笔者来说时间还是不够，部分题有思路之后没时间继续做了），最终取得了88th的成绩，收获是又学习到了新工具，向大佬们学习。

<img src=".\images\计分板.png" style="zoom: 33%;" />

> 题目分为三大类，有三个压缩包（解压密码：都考100分）
>
> - apk分析.zip
>
> - ISO备份.zip
>
> - 计算机镜像.zip
>
>   > 官方检材地址：
>   >
>   > 比赛检材： https://pan.baidu.com/s/1KYq_HkpPBHWCvWTzz6yzSw?pwd=xzcp
>   > 提取码：xzcp

```
  ○ 手机备份包
 手机基本信息
 1、IOS手机备份包是什么时候开始备份的。（标准格式：2024-01-20.12:12:12)
 2、请分析，该手机共下载了几款即时通讯工具。（标准格式：阿拉伯数字）
 3、手机机主的号码得ICCID是多少。（标准格式：阿拉伯数字）
 4、手机机主登录小西米语音的日期是什么时候。（标准格式：20240120）
 地图数据
 5、请问嫌疑人家庭住址在哪个小区。（标准格式：松泽家园）
 浏览器
 1、Safari浏览器书签的对应数据库名称是什么。（标准格式：sqltie.db)
 2、手机机主计划去哪里旅游。（标准格式：苏州）
 即时通讯
 1、手机机主查询过那个人的身份信息。（标准格式：龙信）
 2、请问机主共转多少费用用于数据查询。（标准格式：1000）
 3、机主查询的信息中共有多少男性。（标准格式：阿拉伯数字）
 
  ○ 计算机取证
 基本信息
 1、计算机系统的安装日期是什么时候。（标准格式：20240120）
 系统痕迹
 1、请问机主最近一次访问压缩包文件得到文件名称是什么。（标准格式：1.zip）
 数据库分析
 1、还原数据库，请分析root用户最后一次更改密码的时间是什么时候。（标准格式：2024-01-20.12:12:12)
 2、请问mysql数据库中共存在多少个数据库。（标准格式：阿拉伯数字）
 3、员工编号为204200的员工总工资为多少元。（标准格式：阿拉伯数字）
 4、Finance部门中在1999年1月1日当天和之后入职的人员数量是多少名。（标准格式：阿拉伯数字）
 邮箱服务器
 1、请问邮箱服务器的登录密码是多少。（标准格式：admin）
 2、邮件服务器中共有多少个账号。（标准格式：阿拉伯数字）
 3、邮件服务器中共有多少个域名。（标准格式：阿拉伯数字）
 4、请问约定见面的地点在哪里。（标准格式：太阳路668号）
 
  ○ apk分析
 1、APP包名是多少。（标准格式：com.xxx.xxx）
 2、apk的主函数名是多少。（标准格式：comlongxin）
 3、apk的签名算法是什么。（标准格式：xxx）
 4、apk的应用版本是多少。（标准格式：1.2）
 5、请判断该apk是否需要联网。（标准格式：是/否）
 6、APK回传地址？（标准格式：127.0.0.1:12345）
 7、APK回传数据文件名称是什么。（标准格式：1.txt）
 8、APK回传数据加密密码是多少。（标准格式：admin）
 9、APK发送回后台服务器的数据包含以下哪些内容？（多选）
A．手机通讯录B.手机短信C.相册D.GPS定位信息E.手机应用列表
```



## 一、手机备份包

### 手机基本信息

### 1.1、 IOS手机备份包是什么时候开始备份的。（标准格式：2024-01-20.12:12:12)

> 答案：`2024-01-15.14:19:44`

压缩文件解压后的文件夹名即为答案：

<img src="D:\Desktop\新建文件夹\2024獬豸杯\image\IOS备份\备份日期.png" style="zoom:75%;" />

或

查看log.txt日志文件，得到`14:19:44`的时间点

<img src=".\images\image-20240129091822608.png" alt="image-20240129091822608" style="zoom:75%;" />

### 1.2、请分析，该手机共下载了几款即时通讯工具。（标准格式：阿拉伯数字）

> 答案：`3`
>
> 工具：
>
> 1、`iBackup Viewer`：https://www.imactools.com/iphonebackupviewer/

`iBackup Viewer` 是一个适用于 Windows 和 macOS 的免费工具。

使用该工具打开文件夹`**\2024年01月15日_14时19分44秒_iPhone\38eb9848d19c02cab32ca7c125c5e834f298c416`

可以看到安装了三款通讯工具：

<img src=".\images\image-20240129094530563.png" alt="image-20240129094530563" style="zoom:50%;" />

### 1.3、手机机主的号码得ICCID是多少。（标准格式：阿拉伯数字）

> 答案：`89860320245121150689`
>
> 1、`iTunes-Backup-Explorer`：https://github.com/MaxiHuHe04/iTunes-Backup-Explorer
>
> 2、`iTunesBackupTransfer`：https://github.com/WXjzcccc/iTunesBackupTransfer

`iBackup Viewer` 并不能通用的解决所有问题，分析备份包的根源还是解析文件目录。

笔者在比赛时使用`iTunes-Backup-Explorer`工具（**java -jar 执行，需要jdk11以上**），工具打开`Manifest.plist`或`Manifest.db`文件即可解析。

> ps：该备份包是没有密码的，否则需要其他方式获取秘密

<img src=".\images\image-20240129092620705.png" alt="image-20240129092620705" style="zoom:50%;" />

>  除了`iTunes-Backup-Explorer`工具解析，赛后学习到了大佬的新工具`iTunesBackupTransfer`

导出所有文件后即可进行后续分析。

使用VS code打开目录后搜索`ICCID`得到答案。

<img src=".\images\image-20240129095754193.png" alt="image-20240129095754193" style="zoom:50%;" />

> ps：查阅资料得知相关信息应存储于备份文件夹下的的`info.plist`文件，但没找到。
>
> <img src=".\images\image-20240129100005863.png" alt="image-20240129100005863" style="zoom:50%;" />
>
> > 实际该`info.plist`文件也可获得软件安装信息。

### 1.4、手机机主登录小西米语音的日期是什么时候。（标准格式：20240120）

> 答案：`20240115`

小西米语音app相关目录位于`**\AppDomain-com.titashow.tangliao\`

可以通过查看Library目录下的文件信息得到。   

该题目的日期精确到day，且在log中所有的信息都是0115的记录。（或文件的修改日期）

<img src=".\images\image-20240129100510450.png" alt="image-20240129100510450" style="zoom:50%;" />

### 地图数据

### 1.5、 请问嫌疑人家庭住址在哪个小区。（标准格式：松泽家园）

> 答案：天铂华庭
>
> 1、`sqlitebrowser`：https://github.com/sqlitebrowser/sqlitebrowser
>
> 2、`ForensicsTool`：https://github.com/WXjzcccc/ForensicsTool

本题为赛后学习得到。

根据提示（**地图数据**）及`IBackup Viewer`工具显示存在高德地图app，可以大致将解题方向指向获取高德数据记录。

<img src=".\images\image-20240129100957181.png" alt="image-20240129100957181" style="zoom:50%;" />

高德app数据位置位于`AppDomain-com.autonavi.amap`目录，记录通常使用SQlite格式保存，可使用`sqlitebrowser`或`Navicat`工具查看。

该题目中，高德数据是加密的，赛后学习重要文件是`girf_sync.db`。`everything`工具搜索得到文件位于以下目录：

`**\AppDomain-com.autonavi.amap\Documents\cloundSyncData`

使用`ForensicsTool`工具可解密，命令（自行参考github仓库）：`python ForensicsTool.py -m 1 -t 4 -f girf_sync.db`

<img src=".\images\image-20240129102822235.png" alt="image-20240129102822235" style="zoom:50%;" />

解密后的文件`girf_sync_dec.db`使用`sqlitebrowser`打开，可看到`天铂华庭`

- `SEARCH_SNAPSHOT`表保存搜索记录 
- `ROUTE_HISTORY_V2_SNAPSHOT`保存了导航历史

<img src=".\images\image-20240129103355396.png" alt="image-20240129103355396" style="zoom:50%;" />

### 浏览器

### 1.6、Safari浏览器书签的对应数据库名称是什么。（标准格式：sqltie.db)

> 答案：`Bookmarks.db`

没什么好说的，知识题，可直接搜或问GPT。

<img src=".\images\image-20240129103715492.png" alt="image-20240129103715492" style="zoom:50%;" />

> iOS 设备上使用的 Safari 浏览器允许用户为自己喜欢的网站添加书签。`Bookmarks`数据库可以在`/HomeDomain/Library/Safari/Bookmarks.db`找到。书签数据可以通过一个非常简单的查询提取出来，或`sqlitebrowser`查看。

### 1.7、手机机主计划去哪里旅游。（标准格式：苏州）

> 答案：`拉萨`
>
> 1、`Autopsy`：https://github.com/sleuthkit/autopsy

主要是解析浏览器搜索历史，`iBackup Viewer`的History为空，换其他工具。

#### 解法1、Autopsy综合取证（类似取证大师）

> 类似取证大师，但免费开源，使用教程自行百度

新建case之后，在`Select Data Source Type`选择`Logical Files`添加**解析后（1.3节）**的ios目录，并且在`Ingest Modules`时选择`iOS Analyzer(iLEAPP)`

<img src=".\images\image-20240129110703470.png" alt="image-20240129110703470" style="zoom:50%;" />

分析完成后，在Reports中找到对应报告双击打开，即可看到`Safari`搜集历史：15日搜索了`拉萨有高原反应吗`。

<img src=".\images\image-20240129110828327.png" alt="image-20240129110828327" style="zoom:50%;" />

<img src=".\images\image-20240129110947738.png" alt="image-20240129110947738" style="zoom:40%;" />

> 此处主要使用Autopsy工具的`iOS Analyzer(iLEAPP)`分析，是内置的插件。在github上有源码（https://github.com/markmckinnon/iLEAPP），但直接运行尚存在问题，未解决。

#### 解法2、文件解析

查询资料可知，safari浏览历史可以在`History.db`中找到，在`/HomeDomain/Library/Safari/`处。关于被访问网站最重要的信息可以从`history_items`和`history_visits`表中提取。

但此备份中不存在相关的`History.db`，（应该也是`iBackup Viewer`中History记录为空的原因）

除了`History.db`文件，在`**\AppDomain-com.apple.mobilesafari\Library\Preferences`目录下存在`com.apple.mobilesafari.plist`文件，虽无法直接查看，但可使用脚本解析。

> ps：`com.apple.mobilesafari.plist`是`iOS Analyzer(iLEAPP)`工具解析的文件。

```python
import plistlib
plist_path = '/Users/your_username/Library/Preferences/com.apple.mobilesafari.plist'
with open(plist_path, 'rb') as fp:
    plist_data = plistlib.load(fp)

# 现在 plist_data 包含了 plist 文件的内容，您可以通过字典的方式访问其中的键值对
print(plist_data)
```

将结果格式化显示后，得到`RecentWebSearches`

<img src=".\images\image-20240129111945331.png" alt="image-20240129111945331" style="zoom:50%;" />

 ### 即时通讯
### 1.8、手机机主查询过那个人的身份信息。（标准格式：龙信）

> 答案：`龙黑`

根据提示的`即时通讯`，结合1.2的三款通讯工具，找到小西米聊天记录数据库（在目录中AppDomain-com.titashow.tangliao翻一翻文件是可以看到的）

`/AppDomain-com.titashow.tangliao/Documents/IM5_CN/9031bc3c805ac5e55ecaa151092c2c4b/IM5_storage/1407383114858132610/im5db`

使用`sqlitebrowser`打开，在`message`表中，可以看到聊天记录。显示机主查过手机号`17712680573`的号码姓名，回复的是`龙黑`。

<img src=".\images\image-20240129133910432.png" alt="image-20240129133910432" style="zoom:50%;" />

在`iBackup Viewer`相册中，也能看到机主询问过`17712680573`的号码姓名。

<img src=".\images\image-20240129134048057.png" alt="image-20240129134048057" style="zoom:50%;" />

 ### 1.9、请问机主共转多少费用用于数据查询。（标准格式：1000）

> 答案：`1100`

同上题，除龙黑外，又查询了10个数据，共计费用1100。

### 1.10、机主查询的信息中共有多少男性。（标准格式：阿拉伯数字）

> 答案：`4`

在`iBackup Viewer`可以看到短信发送的10个数据信息，包括身份证号。

思路是通过身份证号的第17位识别男女，奇数为男性（在解题中没有正确区分出男女，题目不严谨）

<img src=".\images\image-20240129134707256.png" alt="image-20240129134707256" style="zoom:50%;" />

> 张二、李四、江三、王也

 ## 二、计算机取证

 ### 基本信息

 ### 2.1、计算机系统的安装日期是什么时候。（标准格式：20240120）

> 答案：`20240112`

`Autopsy`新建`case`，选择`Disk Image or VM File`数据源，选择`Recent Activity`的插件即可（不推荐全选，费时，且后续可根据需求运行相关插件）。

对于计算机系统的安装日期，记录于系统的注册表中，参考如下：

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion`的`InstallDate`子键

windows注册表位于：`c:/Windows/System32/config`目录下，`Autopsy`工具可直接查看注册表（或导出借助其他工具查看）：

选择SOFTWARE注册表，依次找到子键`\Microsoft\Windows NT\CurrentVersion\InstallDate`

<img src=".\images\image-20240129145959128.png" alt="image-20240129145959128" style="zoom:67%;" />

将时间戳解析为日期得到`1705045256`的日期格式为：`2024-01-12 07:40:56 UTC`

<img src=".\images\image-20240129150101453.png" alt="image-20240129150101453" style="zoom: 50%;" />

> 本题的答案，为`2024-01-12 07:40:56 UTC`，如果精确到秒，注意UTC转为北京时间格式要加8h，即
>
> 对应的北京时间：`2024-01-12 15:40:56`

### 系统痕迹

### 2.2、请问机主最近一次访问压缩包文件得到文件名称是什么。（标准格式：1.zip）

> 答案：`data.zip`

在`Autopsy`中`Recent Documents`可以看到`data.zip`

<img src=".\images\image-20240129150543255.png" alt="image-20240129150543255" style="zoom: 67%;" />

### 数据库分析

> 菜鸡卡在了这里，比赛时没做出来，只能是赛后复现了

### 1.3、还原数据库，请分析root用户最后一次更改密码的时间是什么时候。（标准格式：2024-01-20.12:12:12)

> 答案：`2021-03-17 15:49:52`

接上题，将`data.zip`导出，可看出是mysql数据库数据文件，且压缩包有秘密（**卡在了这里！**）。

首先溯源`data.zip`是从哪来的：`Tools`工具进行`File Search`搜索得到文件

<img src=".\images\image-20240129151138772.png" alt="image-20240129151138772" style="zoom:50%;" />

右键选择`View File in Directory`定位文件在`/img_计算机像.dd/vol_vol6/Users/Administrator/Desktop/data.zip`。

在`Recent Documents`记录中，时间相邻的还有`待会见.jpg`可疑图片。

- 实际上，在iOS备份中，`iBackup Viewer`看到照片中已存在提示。

<img src=".\images\image-20240129152328078.png" alt="image-20240129152328078" style="zoom:50%;" />

同样搜索`待会见.jpg`得到位置，明显看出是`Foxmail7`邮箱记录。

`/img_计算机镜像.dd/vol_vol6/Users/Administrator/AppData/Roaming/Foxmail7/Temp-5468-20240112163032/Attach/待会见.jpg`

点击同级目录的html文件即可预览到邮件历史，可知密码为尾号555的手机号码。（data.zip的哈希值也匹配）

<img src=".\images\image-20240129152547301.png" alt="image-20240129152547301" style="zoom:50%;" />

> 猜测剧情是这里给了酬金，并且见了面，前面手机备份也查了黑哥的个人信息

掩码爆破，得到解压密码：`15566666555`

解压后，在仅有的.err文件中可知，mysql版本号为5.7.26，且使用phpstudy_pro软件。由于此处仅有data目录，无运行日志文件，只能还原数据库。

<img src=".\images\image-20240129153706856.png" alt="image-20240129153706856" style="zoom:50%;" />

> **没有仿真工具的痛**
>
> 参考资料：https://mp.weixin.qq.com/s?__biz=MzUyOTcyNDg1OA==&mid=2247483966&idx=1&sn=b5a5895e582f329abceb266b0c3e138d&chksm=fa5de6ebcd2a6ffdccfc2f2859224547d9e2d5f67e6e13df803685cd28e2bb3f58d49b719f5a&mpshare=1&scene=1&srcid=01242dz0URlxLlHuA7z4DhbW&sharer_shareinfo=9dfefe1227ce1a82f26b4ac93be98989&sharer_shareinfo_first=eb93aee8a905fa1c6af5c4789b9fdb38#rd

在mysql库的user表中，保存了用户密码更新时间

![image-20240129160429495](.\images\image-20240129160429495.png)

### 2.2、请问mysql数据库中共存在多少个数据库。（标准格式：阿拉伯数字）

> 答案：`5`

![image-20240129160610303](.\images\image-20240129160610303.png)

### 2.3、员工编号为204200的员工总工资为多少元。（标准格式：阿拉伯数字）

> 答案：`488313`

<img src=".\images\image-20240129161127851.png" alt="image-20240129161127851" style="zoom:67%;" />

### 2.4、Finance部门中在1999年1月1日当天和之后入职的人员数量是多少名。（标准格式：阿拉伯数字）

> 答案：`1486`

`team_list`表中可得`Finance`部门对应`dept_no`为`d002`。

<img src=".\images\image-20240129161506596.png" alt="image-20240129161506596" style="zoom:67%;" />

时间大于等于`'1999-01-01'`

<img src=".\images\image-20240129161806945.png" alt="image-20240129161806945" style="zoom:80%;" />

###  邮箱服务器

### 2.5、请问邮箱服务器的登录密码是多少。（标准格式：admin）

> 答案：`900110`

根据前面题目可知，磁盘存在BitLocker加密（手机照片显示，或Recent Document中存在BitLocker 恢复密钥文件），以及FoxMail邮箱。

手机备份中显示BitLocker 密码为：`Longxin@123`

<img src=".\images\image-20240129163135489.png" alt="image-20240129163135489" style="zoom:80%;" />

支持使用`Passware Kit Forensic`或`DiskGenius`工具解密BitLocker：

<img src=".\images\image-20240129163451784.png" alt="image-20240129163451784" style="zoom:80%;" />

或`DiskGenius`工具：右键镜BitLock管理

<img src=".\images\image-20240129163551553.png" alt="image-20240129163551553" style="zoom:67%;" />

找到`hMailServer`的配置文件`/hMailServer/Bin/hMailServer.INI`

<img src=".\images\image-20240129163935798.png" alt="image-20240129163935798" style="zoom: 67%;" />

md5解码：得到`900110`

<img src=".\images\image-20240129164000892.png" alt="image-20240129164000892" style="zoom:80%;" />

### 2.6、邮件服务器中共有多少个账号。（标准格式：阿拉伯数字）

> 答案：`3`

`hMailServer\Data\longxin.com`目录 下有个文件夹，对应三个账号

<img src=".\images\image-20240129164338499.png" alt="image-20240129164338499" style="zoom:80%;" />

### 2.7、邮件服务器中共有多少个域名。（标准格式：阿拉伯数字）

> 答案：`3`

暂不能复现

 ### 2.8、请问约定见面的地点在哪里。（标准格式：太阳路668号)

> 答案：`中国路999号`

`待会见.jpg`搜索16进制数值FFC0修改图片高度

![image-20240129172142786](.\images\image-20240129172142786.png)

<img src=".\images\image-20240129172202969.png" alt="image-20240129172202969" style="zoom: 67%;" />



 ## 三、apk分析
### 3.1、APP包名是多少。（标准格式：com.xxx.xxx）

> 答案：`com.example.readeveryday`
>
> > 1、`AndroidKiller`：https://github.com/liaojack8/AndroidKiller

使用`AndroidKiller`打开`实操1.apk`文件，在工程信息窗口可以查看答案。

<img src=".\images\image-20240129135720507.png" alt="image-20240129135720507" style="zoom:50%;" />

### 3.2、apk的主函数名是多少。（标准格式：comlongxin）

> 答案：`StartShow`

同上题，`入口：StartShow`

### 3.3、apk的签名算法是什么。（标准格式：xxx）

> 答案：`SHA1withRSA`
>
> 1、`jadx`：https://github.com/skylot/jadx

`jadx`工具打开`实操1.apk`，显示签名算法。

<img src=".\images\image-20240129140759669.png" alt="image-20240129140759669" style="zoom:50%;" />

### 3.4、apk的应用版本是多少。（标准格式：1.2）

> 答案：`1.0`

同上，在`AndroidKiller`的工程信息中，存在`版本信息：Ver：1.0`的描述。

具体描述在`资源文件/AndroidManifest.xml`中，存在`android:versionName="1.0"`

### 3.5、请判断该apk是否需要联网。（标准格式：是/否）

> 判断题：`是`。 仅一次机会

####  解法1、主函数StartShow分析

在函数中，可以看到存在联网权限：

<img src=".\images\image-20240129141633657.png" alt="image-20240129141633657" style="zoom: 67%;" />

#### 解法2、在线沙箱分析

> 奇安信平台：https://ti.qianxin.com/
>
> 注册即可

在分析报告中可以看到应用权限允许网络访问：

<img src=".\images\image-20240129141939057.png" alt="image-20240129141939057" style="zoom:67%;" />

除此之外，报告中的**APK文件元数据**也可看到包名、主函数、版本号等信息。

<img src=".\images\image-20240129142133424.png" alt="image-20240129142133424" style="zoom:67%;" />

#### 解法3、AndrordManifest.xml权限列表

`AndrordManifest.xml`是非常重要的文件，它是Android的清单文件，存放了许多Apk配置信息，记录着包括软件包名、版本号、应用权限、组件配置等。

> 文件是被加密存储的，直接解压不可读，通过`jadx-gui`工具打开可以看到

<img src=".\images\image-20240131092909023.png" alt="image-20240131092909023" style="zoom:50%;" />

应用权限解读：

```
android.permission.READ_CONTACTS			允许访问联系人通讯录信息	
android.permission.READ_SMS					接收短信
android.permission.WRITE_EXTERNAL_STORAGE	写外部存储器（如：SD卡）
android.permission.INTERNET					连接网络
```

因此，根据权限apk需要联网。

### 3.6、APK回传地址？（标准格式：127.0.0.1:12345）

> 答案：`10.0.102.135:8888`

在`jadx`中可以看到源码文件，文件内容不多，`StartShow`是入口，除外就是`MainActivity`，仔细翻一翻即可：

<img src=".\images\image-20240129142546135.png" alt="image-20240129142546135" style="zoom:67%;" />

> 除了`jadx`反编译，在`AndroidKiller`中存在内置`jd-gui`也可看到源码
>
> <img src=".\images\image-20240129142914420.png" alt="image-20240129142914420" style="zoom:67%;" />

### 3.7、APK回传数据文件名称是什么。（标准格式：1.txt）

> 答案：`Readdata.zip`

同上题

### 3.8、APK回传数据加密密码是多少。（标准格式：admin）

> 答案：`19_08.05r`

继续看源码，在`EncryFile`函数中看到`setPassword("19_08.05r".toCharArray())`。

或直接搜索`password`也可找到

<img src=".\images\image-20240129143236328.png" alt="image-20240129143236328" style="zoom:50%;" />

### 3.9、APK发送回后台服务器的数据包含以下哪些内容？（多选）

> A.手机通讯录
>
> B.手机短信
>
> C.相册
>
> D.GPS定位信息
>
> E.手机应用列表
>
> 
>
> 答案：ABE

`XmlWrite`方法中可以看到`AppInfo`、`ContactRecord`、`SMSRecord`的调用，或可以使用排除法，相册、GPS均未出现过。

<img src=".\images\image-20240129143513578.png" alt="image-20240129143513578" style="zoom: 67%;" />