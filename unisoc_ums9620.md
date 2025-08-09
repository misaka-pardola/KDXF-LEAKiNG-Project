---
byleaking-iflytek 请遵循协议使用
---

# ums9620机型破解
## 1.简介原理

其实也挺简单的 紫光终于在9620机型(t30lite等等等)上完善了avb 同时spdump也增加了avb开关 但是不知道为啥 解锁之后avb并没有关闭 所以我们需要解锁之后手动关闭avb 之后刷入magisk之后打模块安装安装器并且开启adb \[真是感谢新云控和给官方提供限制思路的某前群主啊 不是他的提醒开发者选项根本不会禁用的]
## 2.操作前准备
> **必须的** 电脑一台 同时至少windows7以上或是linux\[不要xp啊喂 这东西都快入土了] 
> USB线ctoa一条 (当然你电脑有c口拿ctoc当我没说) 
> leaking群内的文件包
> 安卓手机一台 并且可以随便安装应用
> 以及白天的时间 基本的电脑操作常识 以及基本的耐心
> **不太必须的** 群内大佬的联系方式
> **强烈建议仔细看完教程再进行操作**
> **本教程必然丢失数据 请注意备份**
## 3.let start
### 1.电脑上安装紫光驱动
1解压文件包 看向driver文件夹 直接双击64install.exe(应该大概现在的电脑都是64位的电脑吧 如果打不开你双击32install.exe试试？)
2.按照流程走完安装程序
### 2.解锁bootloader
我们利用CVE-2022-38694\_unlock\_bootloader解锁bootloader 并不需要进入开发者选项 只需要
1.平板关机
2.usb连接上电脑
3.等待充电动画消失
4.电脑上打开unlock\_autopatch\_9620.bat (linux环境下就是sh 应该不用我教怎么给它运行权限吧)
同时按住学习机电源 音量上 音量下 等待程序开始跑日志
当学习机开始提示清除数据时 bootloader就已经解锁了
> tips:bootloader解锁后开机时会出现两行提示
> info:lock flag is unlock!!! 
> warring lock flag is unlock,skip verify!!! 
> 无需在意 按电源键两次或等待几秒便会开机
### 3.关闭avb校验
*~~不关刷不了boot勒~~*

1.平板关机 等待充电动画消失
2.电脑进入文件夹内
1. win11可以直接右键打开终端
2. win10 win8 win7请清空地址栏 输入cmd
3. linux 你都装linux了应该知道怎么打开终端的对吧

输入spd\_dump按tab补全
3同时在学习机上按下电源键 音量上 音量下 直到cmd窗口出现
brom>
输入fdl fdl1-dl.bin 0x65000800回车 等待提示符变为fdl1>
输入fdl fdl2-dl.bin 0xb4fffe00回车 再输入exec 回车 等待输出分区表并且提示符变为fdl2>
输入verifly 0 回车
大概操作过程长这样(完整命令展示)
```
brom>fdl fdl1-dl.bin 0x65000800
fdl1>fdl fdl2-dl.bin 0xb4fffe00
fdl1>exec
fdl2>verifly 0
```
这个时候会开始自动读取并且修改vbmeta
当提示符fdl2>重新出现时 avb便已经关闭
> **不要关闭这个窗口否则你需要重新进入fdl2**
### 4.刷写boot
1.备份boot 在上面打开的窗口中输入 r boot\_a 回车
2.在目录下会多一个文件 名称应该为boot\_a.bin
将文件后缀名更名为.img
3.看向文件包 里面应该有一个已经提前被我们修补好的boot(基于1.01.8版本)
输入 w boot\_a boot\_patched.img
等待提示符重新出现
输入 reset
平板应该会正常开机 **如果没有开机 请看救砖一节或者联系管理员**
完整代码展示

```
fdl2>r boot_a
fdl2>w boot_patched.img
fdl2>reset
```
### 开机安装模块
截止教程编写完成 只有模块法 只是 模块需要magisk管理器正常工作才能安装 所以你需要手机在家长端解除magisk管理器的时间限制
直接点击桌面上的alpha安装alpha
> 网速不好可以这样操作

1. 将工具包内的alpha.apk复制出来
2. 学习机开机情况连接电脑并且在家长端解除usb限制 通知选择传输文件
3. 学习机设置 文档 选择用文件打开 左边会出现一个设备名 点击里面的alpha.apk
    直接安装

进入alpha之后补全运行库
最后 将模块与上方alpha安装包一样的方式拷贝进学习机
alpha管理器中点击模块 从本地安装
搜索 a13\_a12 找到模块
安装之后打开爱玩机锁定爱玩机为默认安装器就可以安装apk了



























> the end。




TldFMlpUWmFiVVkxVEdsTFNVOWxibXRsVjJ0d0sybDFjaXR0YW01MVpXRm9UMWMyYkU5bFZYRlBiVnByVDFkSmRIVnRSbXBsWlRseWRXRlhhQ3RUTjNSMVYyWjFkVk0yYW01T2VHSkRSR3h5V21wdGJFdzNhM1Z2TkhaYVIwWXdXVk01YUdOSVFYWmlWMUowTlhCNVNqVlpWM28xTlhGRk5UVjFkVFZpTWxZMVRHbDBTVTlUTDNKMVlWVjFaVmRHZEhWVEszWXJWMUJ5SzFNM2NHVlhkV3BQWVVsclQybHVieXR0V25CUFZ6WnNUMlZWY1U5dFdtdFBWMGwwWnowOQ==












l






e





a













k






i





n






g
