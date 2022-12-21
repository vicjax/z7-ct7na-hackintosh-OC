# z7-ct7na-Hackintosh-OC

# 当前版本

- OpenCore v0.8.7-release
- MacOs Monterey 12.6

# 摘要

- 平台：神舟z7-ct7na

|        项目         |               型号                | 支持MacOs版本 |
| :-----------------: | :-------------------------------: | :-----------: |
|         CPU         |          Inter i7-9750H           |   10.12.6~    |
|     Motherboard     | Clevo NH5x_7xRCx,RDx(Inter HM370) |   10.12.6~    |
|        iGPU         |           Inter UDH 630           |   10.12.6~    |
|         GPU         |         Nvidia GTX 1660Ti         |      N/A      |
|  Wired Networking   |       Realtek RTL8168/8111        |       ~       |
| Wireless Networking |     Intel(R) Wireless-AC 9462     |      N/A      |
|       Storage       |      WDC PC SA530 SDASN8Y512      |       ~       |
|     Audio Codec     |          Realtek ALC293           |       ~       |

舍弃Clover，并重新基于Opencore创建，更新系统版本，当前已支持macOs Monterey 12.6(已测)。

- 编译SSDTs,已修复电源支持；

- Usb 已定制，已修复摄像头；

- 无线网卡已驱动，支持无线网、蓝牙连接

  > ❗​暂不支持隔空投送；

- 修复miniDP，支持外接显示器

  > ❗若要使用miniDP（核显驱动）外接显示器，请勿加载`SSDT-dGPU-Off`，默认关闭；如无外接显示器需求，建议加载`SSDT-dGPU-Off`,否则会出现睡眠问题。
  
  > ❗外接显示器时内置显示器的亮度调节功能会失效

- 加载usb总线睡眠唤醒功能，支持键盘鼠标等usb设备睡眠唤醒

  > ❗盒盖长时间会出现无法唤醒情况，不建议盒盖睡眠，外接显示器时会出现睡眠不稳定的问题。

# :bookmark: Note

 假定已大致了解黑苹果及Opencore的相关知识

- 直接下载Release压缩包

- 使用前请务必修改三码！！！！使用前请务必修改三码！！！！使用前请务必修改三码！！！！

# 附：关于此类机型的睡眠问题！！！

睡眠问题总是很恼人，除了现实中，也包括黑苹果！！！当然最好的办法就是不睡眠（终归要踏上修仙之路👻）💤

## 不睡眠的办法

- 现实中（一般不建议）

- 黑苹果

   -  系统偏好设置 -> 电池 -> 电池 -> 此时间段后关闭显示器 ：进度条拉到最右
   
   -  系统偏好设置 -> 电池 -> 电源适配器 -> 此时间段后关闭显示器 ：进度条拉到最右

## 关闭睡眠之后如何关闭显示器以节电

通过组合键Fn+F2（具体按键方式视笔记本型号而定）组合键可以实现关闭显示器的功能，这样无疑是当下最好的解决方式。
