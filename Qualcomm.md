# 高通系机型教程

* 注意：在食用教程前，请先确保你设备

## X1Pro

* 文件：files/firehoses/x1pro/

## X3 5G或者P30 5G

### 具体过程

#### 解BL

* 装[9008驱动](https://kdxf.work/%E9%AB%98%E9%80%9A%E6%9C%BA%E5%9E%8B/x3-5G/%E9%A9%B1%E5%8A%A8)
* 进入9008模式(关机完，按住音量上再插上数据线，然后就进去了)
* 使用 **firehose文件（files下有）** 和 [酷安@某贼 开发的《高通工具箱》](https://syxz.lanzoue.com/b01g1c7ve "（密码bulf）")读取出boot相关分区及vbmeta分区，将unlock_bl目录下的frp.img刷入到frp分区，misc.img刷入到misc分区，然后重启板子
  重启后会默认进入fastbootd，你需要用adb工具或者各种工具箱重启到bootloader，或者输入 `fastboot reboot bootloader` 然后再执行 `fastboot flashing unlock`就进入了经典的高通解锁选择题。自行翻译自行选择就行，我相信你能做到。

#### 刷REC

都解好BL了，那就该刷TWRP（这里用的是一个美化过的分支，叫OFRP）了

刷OFRP，可以从这个链接的Releases里下载到OFRP包，你可以通过fastboot（bootloader）来临时启动OFRP，然后使用OFRP安装下载的包

#### 刷Root

得确保你已经刷了REC了，然后下载Magisk安装包并使用OFRP安装到boot，然后就没了

#### 刷回联想官方系统养老

去[这个网站](https://mirrors-obs-1.lolinet.com/firmware/lenowow/2021/Tab_P11_5G/TB-J607Z/)下载原版的9008包，拿高通工具箱先把全机除cache/userdata以外的所有分区全部备份，然后把9008包里面那一堆分区刷进去再重启就行了，如果砖了刷回你备份的分区。
