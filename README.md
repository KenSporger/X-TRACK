# X-TRACK复刻版
> 开源GPS自行车码表。
> 
> 拥有可显示实时位置的离线地图。
> 
> 支持记录和显示实时轨迹以及导出标准GPX格式的轨迹文件。
> 
> 全新设计的["页面生命周期管理"](https://github.com/FASTSHIFT/X-TRACK/tree/main/Software/X-Track/USER/App/Utils/PageManager)和["消息订阅发布框架"](https://github.com/FASTSHIFT/X-TRACK/tree/main/Software/X-Track/USER/App/Utils/DataCenter)。
>
> 演示视频：https://www.bilibili.com/video/BV1GB4y1K7VV

![image](https://github.com/FASTSHIFT/X-TRACK/blob/main/Images/%E5%9C%B0%E5%9B%BE.jpg)

## GUI
> [LVGL V8](https://github.com/lvgl/lvgl)

## 硬件配置
* 1.主控: AT32F435CGU7 (主频:288MHz RAM:512KB ROM:1MB)
* 2.屏幕: ST7789 IPS 1.54inch SPI接口 240x240分辨率 60Hz刷新率
* 3.储存器: Micro SD CARD 32GB 
* 4.输入设备: 旋转编码器
* 5.RTC: MCU内置RTC时钟
* 6.加速度计: LSM6DSM (支持硬件计步输出)
* 7.地磁计: LIS3MDL
* 8.GPS: ATGM336H (BDS + GPS + GLONASS + GALILEO + QZSS + SBAS)
* 9.电池: Li-ion 3.7V 683030 700mAh
* 10.电源管理: LP5907-3.3 + MCP73831
* 11.外壳: 3D打印 光固化

| 名称                                                         | 说明                                    | 个数 | 价格/元 |
| ------------------------------------------------------------ | --------------------------------------- | ---- | ------- |
| [AT32F403ACGU7](https://item.taobao.com/item.htm?spm=a230r.1.14.42.21e23d645o0kTc&id=688717523590&ns=1&abbucket=4#detail) | 国产雅特力芯片，QFN48(6*6)              | 1    | 10      |
| [中景园 ST7789 IPS 1.54inch屏幕](https://item.taobao.com/item.htm?id=600467790218&ali_refid=a3_430673_1006:1151926661:N:RJwpqEZSBeef9oplU%2FG0erdQXHNUIGLMbjxUjePoUps%3D:c5e666e29cd76924d1848b0193797d52&ali_trackid=1_c5e666e29cd76924d1848b0193797d52&spm=a2e0b.20350158.31919782.1) | SPI接口 240x240分辨率 60Hz刷新率 焊接式 | 1    | 13.5    |
| [中景园 ST7789 IPS 1.54inch屏幕](https://item.taobao.com/item.htm?spm=a1z10.3-c-s.w4002-23991449512.17.1768703bH4HJ05&id=674857510309) + [12pin FPC插座](https://item.taobao.com/item.htm?spm=2013.1.0.0.6d085ccaXaBTl1&id=565131541304&scm=1007.12144.95220.42296_0_0&pvid=1c2a199b-1f2d-433a-87e7-73e39c1c54f5&utparam=%7B%22x_hestia_source%22%3A%2242296%22%2C%22x_object_type%22%3A%22item%22%2C%22x_hestia_subsource%22%3A%22default%22%2C%22x_mt%22%3A0%2C%22x_src%22%3A%2242296%22%2C%22x_pos%22%3A1%2C%22wh_pid%22%3A-1%2C%22x_pvid%22%3A%221c2a199b-1f2d-433a-87e7-73e39c1c54f5%22%2C%22scm%22%3A%221007.12144.95220.42296_0_0%22%2C%22x_object_id%22%3A565131541304%7D) | SPI接口 240x240分辨率 60Hz刷新率 插接式 | 1    | 18.7    |
| [6轴IMU LSM6DSM](https://item.taobao.com/item.htm?spm=a230r.1.14.1.5111601fNoKlFT&id=681603401815&ns=1&abbucket=1#detail) | 丝印LGA-14，注意安装方向                | 1    | 12      |
| [地磁计 LIS3MDL](https://item.taobao.com/item.htm?spm=a230r.1.14.1.313a4d8fZxrJbg&id=671364707030&ns=1&abbucket=1#detail) | 丝印LGA-12，注意安装方向                | 1    | 11.8    |
| [中科微HT1818Z3G5L GPS芯片flash版](https://item.taobao.com/item.htm?spm=a230r.1.14.27.22387a54XGjRUT&id=669752725912&ns=1&abbucket=4#detail) | 中科微GPS                               | 1    | 18.9    |
| [MITSUMI美上美拨轮编码器](https://item.taobao.com/item.htm?spm=a230r.1.14.1.2fb54f9eec557f&id=596202182869&ns=1&abbucket=4#detail) | 封装SIQ-02FVS3，开关15定位              | 1    | 7       |
| [自弹式TF卡座](https://detail.tmall.com/item.htm?ali_refid=a3_430582_1006:1104520036:N:iHEpUPPUKN1OQUgmeL6hRicPE%20jb6TeW:705b802e5b23b0509e3d23057cf767c7&ali_trackid=1_705b802e5b23b0509e3d23057cf767c7&id=20693027604&spm=a230r.1.14.1&skuId=3807453352314) | 14.75mm*14.50mm，焊脚间距1.1mm          | 5    | 2.37    |
|                                                              |                                         |      |         |



## 功能
* 1.支持速度、距离、时间、卡路里、航向显示
* 2.拥有**离线地图**，支持显示实时位置，支持缩放
* 3.支持计步
* 4.支持经纬度、海拔显示
* 5.支持RTC自动根据GPS校准
* 6.支持记录轨迹，可导出[GPX格式](https://zh.wikipedia.org/wiki/GPX)的文件
* 7.支持掉电自动保存数据(JSON格式文件)
* 8.四小时续航 (持续工作，始终亮屏)
* 9.支持在[PC模拟器](https://github.com/FASTSHIFT/X-TRACK/tree/main/Software/X-Track/Simulator)模拟，脱离硬件调试(配置为**Release x86**)
* 10.支持显示实时轨迹
* 11.待续...

## 实物演示
### 测速
https://user-images.githubusercontent.com/26767803/120889722-1f8d8e80-c631-11eb-8294-df79f151dedb.mp4

### 历史轨迹显示([GPXSee](https://github.com/tumic0/GPXSee))
![image](https://github.com/FASTSHIFT/X-TRACK/blob/main/Images/%E8%BF%90%E5%8A%A8%E8%BD%A8%E8%BF%B9.png)

## 致谢
> 感谢[@FASTSHIFT](https://github.com/FASTSHIFT)开源的[X-TRACK项目](https://github.com/FASTSHIFT/X-TRACK)。
