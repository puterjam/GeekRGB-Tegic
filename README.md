# Geek RGB Firmware v2 for Tegic Framism 

![Tegic](https://i.imgur.com/qhNb7zi.png)

# 固件特性
* 同时支持 VIA + SignalRGB + openRGB
* 独立按键灯效配置，游戏场景联动
* 增加两个自定义按键，用于切换 SignalRGB 和 openRGB 灯效。默认按键 FN+F1，FN+F2


# 如何安装
## 1. 安装固件工具
下载 QMK 键盘刷固件工具 qmk_toolbox
下载地址：https://github.com/qmk/qmk_toolbox/releases

## 2. 进入键盘 bootloader 模式
拔掉USB线 - 长按 ESC 键（不松开）- 插上USB线 即进入键盘的 bootloader 模式。

也可以通过在键盘布局中设置一个 QK_BOOT 按键一键进入。

## 3. 刷写固件
把固件文件 melgeek_tegic_rev2_via_20221127.hex，拖拽到 qmk toolbox 的输入框, 点击 Flash 即可

# 目录说明
- Firmware - 键盘固件
- config - 调整后的via配置
- plugins - 一些软件配套的键盘插件

# 其他事项
## 1. 通过via修改按键布局
* 只能在非OpenRGB模式下，才能通过via连接键盘进行设置
* via 读取的键位布局后，会丢失自定义按键码，需要手动添加

## 2. 两个自定义按键码是多少？
* 0x5db1 -> 切换 OpenRGB 灯效
* 0x5db2 -> 切换 SignalRGB 灯效

## 3. 相对官方固件做了哪些调整
* 调整了默认键盘第二层布局，刷固件后，打开via可以查看

![Tegic in VIA](https://i.imgur.com/nBY9cX7.png)


* 因为固件体积关系，去掉了部分QMK特效。（软件可以自定义灯效了，默认灯效意义不大）
* 基于官方rev1版本，调整led灯位，可以让openRGB正常读取键位

## 4. 固件源码在哪？
https://github.com/puterjam/qmk_firmware/tree/GeekRGBRelease_2.0
