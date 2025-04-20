# IFLYTEK-LEAKING：玩机教程开源计划（继承自原来BOOM的studentpad-research项目）

# 教程编写团队的简单介绍+入群流程

* 本团队由原BOOM与LMC团队合并以及加入的DECODE（好吧这个已经死了）的几位大佬形成，皆在解决新版本机型的破解问题(走的是修改系统分区流派)
* 如果你有兴趣为我们提供思路的话，欢迎开issue or 进我们群（在后面我们也会简述学习机的情况）交流群聊：1027759100（审核群）
* 我们的所有资源都是免费的，也欢迎给我们为爱发电，研发某些小东西（比如UEFI啥的），如发现没有标识出处乱发布我们团队文件的（致敬某团队传奇成员自己团队的偷了还偷我们的），欢迎举报
* 欢迎各位大佬（愿意提供研究、开发、测试方面帮助的）来我们团队玩
* 因不可抗力因素，我们不能提供具体的破解思路，敬请各位谅解

# 风险提醒

* ！！！Warning！！！刷过机的都知道，刷机前要解锁BootLoader，这会清空你学习机的所有数据，因此请你进行备份后再操作
* 下面的这些行为都超过了《科大讯飞AI学习机AI学习软件服务用户协议》

> 用户若对学习机进行刷机行为，包括但不限于获取root权限，刷入第三方ROM等，则本机将会从科大讯飞AI学习机官方技术支持和软件保修服务中被移除

* 如您知晓以上风险，那么请随时准备好￥60（官方救砖费用），就请继续往下看，我们不会对下列的行为承担法律责任，我们仅仅提供资源和教程（教程仅公开可能能永久使用的部分）

## 展讯系列机型破解教程

请参照[Unisoc.md内容](./Unisoc.md)进行

### 适用机型

校园版（因不可抗力因素无法提供支持）：

CB-C6s-STU、CB-C8Air-STU、CB-C8hPro-STU、CB-C8Pro-STU、CB-C8-STU、CB-Q1-ETOrg、CB-C6-STU、ZK-MAN、

零售版：

T710机型(ud710)：

chip0-ud710:Z1/X2/X2Pro/X3Pro

chip1-ud710:T20/T10

chip2-ud710:A10（仅原理适用，未实验 | chip2机型暂无合适的fdl文件来进入fdl1，因此无法救砖）

T760机型(ums9620)：Lumie10Pro/T30Lite（仅能进入fdl2模式，但未适配安卓13系统的修改教程）

T310机型(ums312):Q10

## 高通系列机型破解教程

请参照[Qualcomm.md内容](./Qualcomm.md)进行

### 适用机型

联想平板TB-J607Z改的机型（骁龙750G）：P30_5G/X3_5G

课堂版/零售版X1Pro（代号为TYE100，骁龙625，安卓8.1）

Tips:课堂版因不可抗力因素无法提供支持

## 瑞芯微系列机型破解教程

请参照[rockchip.md内容](./rockchip.md)进行

### 适用机型

T20 Pro，T30 Pro，T30 Ultra（都是停留在理论上）

## Contributors | 贡献者名单

[@KawaiiSparkle](https://github.com/KawaiiSparkle)/[@qwqlemon2333](https://github.com/qwqlemon2333)/[@WalleoAndrew](https://github.com/WalleoAndrew)一起编写了伪造apk更新包教程+Root教程  

[@Tomking062](https://github.com/Tomking062)提供了Root的思路(system-root for android 9-10)、spd_dump工具(改进版本)  

[@whhh233](https://github.com/whhh233)为我们免费提供了网盘来存放文件，但现已停止运行  

[@WalleoAndrew](https://github.com/WalleoAndrew)最初开始搞科大AI学习机解除安装限制的人：[他的B站专栏](https://www.bilibili.com/opus/645517873680220178)  

[@YedLeo1](https://github.com/YedLeo1)负责T20Pro机型破解（当然还没搞出来就对了）

[@KawaiiSparkle](https://github.com/KawaiiSparkle)/[@LYao2514](https://github.com/LYao2514)创作了一键自动patch系统分区的脚本  

[@ig25138](https://github.com/ig25138)负责T30Pro机型破解（当然还没搞出来就对了） 

[@misaka_pardola](https://github.com/misaka_pardola) ig25138背后的男人

[酷安@某贼](http://www.coolapk.com/u/3463951)负责将我们备份好的资源上传到[萤火虫资源站](https://yhcres.top)，让很多人能救砖
