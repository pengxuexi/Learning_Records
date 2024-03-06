# Readme

pengxuexi's learning records——Timeline

---

- [Readme](#readme)
  - [1、元器件焊接练习](#1元器件焊接练习)
  - [2、stm32评估板](#2stm32评估板)
  - [3、stm32评估板 2.0](#3stm32评估板-20)
  - [4、esp32验证板](#4esp32验证板)
  - [5、复刻稚晖君的ElectronBot](#5复刻稚晖君的electronbot)
  - [6、复刻ST-Link-Nano](#6复刻st-link-nano)
  - [7、复刻Planck-Pi](#7复刻planck-pi)
  - [8、跨阻放大器外围电路设计](#8跨阻放大器外围电路设计)
  - [9、开发板学习记录](#9开发板学习记录)

---


1. 原理图设计
2. PCB布局布线
3. BOM表的整理
4. 元器件采购
5. 元器件焊接
6. 板卡测试
7. stm32软件编程
8. PCB设计软件：allegro designer、kicad和cadence allegro都有学习，allegro designer使用的最多，我的理解是kicad开源轻便，cadence allegro适合大型工程的分组分工

涉及知识：

1. 信号完整性和电源完整性

## 1、元器件焊接练习

包括0805电容电阻，0603电容电阻、0402电阻，二极管，QFP封装芯片、排阻

<img src="Readme.assets/image-20240228080039183.png" alt="image-20240228080039183" style="zoom:67%;" />

## 2、stm32评估板

主控用的是stm32f103c8t6，想制作设计一个简单的小系统评估板，参考网上的一些设计，比如电源电路，晶振，复位，SD卡，eeporm等，但这是一款有问题的设计

![image-20240228081451367](Readme.assets/image-20240228081451367.png)

设计制作好PCB，导出Gerber文件，打板，BOM表整理，采购，焊接、测试

<img src="Readme.assets/image-20240228081639361.png" alt="image-20240228081639361" style="zoom: 50%;" />

![image-20240228081705968](Readme.assets/image-20240228081705968.png)

## 3、stm32评估板 2.0

吸取上一次的教训，重新设计评估板，加上之前测试好的ips模块，总体包括：晶振电路、复位电路、按键、LED、USB、IPS、电源稳压电路，后面发现USB电路还是有问题的，应该转电平

![image-20240228082413555](Readme.assets/image-20240228082413555.png)

![image-20240228083259470](Readme.assets/image-20240228083259470.png)

打板，BOM表整理，采购，焊接、测试

<img src="Readme.assets/image-20240228082622727.png" alt="image-20240228082622727" style="zoom: 50%;" />

<img src="Readme.assets/image-20240228082652079.png" alt="image-20240228082652079" style="zoom:50%;" />

<img src="Readme.assets/image-20240228082708481.png" alt="image-20240228082708481" style="zoom: 50%;" />

![image-20240228082934337](Readme.assets/image-20240228082934337.png)

用cubemx生成stm32初始化代码，使用clion编辑led验证代码并编译烧录，验证无误

<img src="Readme.assets/image-20240228082917973.png" alt="image-20240228082917973" style="zoom: 50%;" />

![image-20240228083015215](Readme.assets/image-20240228083015215.png)

编写代码，点亮ips：

![image-20240228083156511](Readme.assets/image-20240228083156511.png)

<img src="Readme.assets/image-20240228083118164.png" alt="image-20240228083118164" style="zoom: 33%;" />

<img src="Readme.assets/image-20240228083126820.png" alt="image-20240228083126820" style="zoom: 33%;" />

## 4、esp32验证板

不论是网上的已经验证的开发板焊接，还是自己设计的板卡程序烧录都有问题，主要收获就是QFN的焊接，探索了一下，积累了很多焊接经验

<img src="Readme.assets/image-20240228091219603.png" alt="image-20240228091219603" style="zoom: 50%;" />

![image-20240228091043105](Readme.assets/image-20240228091043105.png)

打板，BOM表整理，采购，焊接、测试

<img src="Readme.assets/image-20240228091314384.png" alt="image-20240228091314384" style="zoom:50%;" />

<img src="Readme.assets/image-20240228091241987.png" alt="image-20240228091241987" style="zoom:50%;" />

![image-20240228091303951](Readme.assets/image-20240228091303951.png)

![image-20240228091424063](Readme.assets/image-20240228091424063.png)

<img src="Readme.assets/image-20240228091414896.png" alt="image-20240228091414896" style="zoom:67%;" />

## 5、复刻稚晖君的ElectronBot

[peng-zhihui/ElectronBot (github.com)](https://github.com/peng-zhihui/ElectronBot)

是一个非常有意思的桌面级小机器工具人，但是复刻到后面舵机的控制一直不顺利，至今还未完成，主要涉及打板，焊接，烧录，测试，组装等

![image-20240228093317664](Readme.assets/image-20240228093317664.png)

![image-20240228093347873](Readme.assets/image-20240228093347873.png)

![image-20240228093354480](Readme.assets/image-20240228093354480.png)

![image-20240228093401759](Readme.assets/image-20240228093401759.png)

![image-20240228093408431](Readme.assets/image-20240228093408431.png)

![image-20240228093414241](Readme.assets/image-20240228093414241.png)

<img src="Readme.assets/image-20240228093420433.png" alt="image-20240228093420433" style="zoom:150%;" />

![image-20240228093427170](Readme.assets/image-20240228093427170.png)

![image-20240228093438659](Readme.assets/image-20240228093438659.png)

## 6、复刻ST-Link-Nano

是一个超迷你的ST-Link模块，相较于市面上的stlink，有typec的接口，并且非常mini，成本低，复刻很成功，焊接注意细节就好。验证烧录也没有问题

![image-20240228093757062](Readme.assets/image-20240228093757062.png)

![image-20240228093805312](Readme.assets/image-20240228093805312.png)

![image-20240228093811029](Readme.assets/image-20240228093811029.png)

![image-20240228093819379](Readme.assets/image-20240228093819379.png)

## 7、复刻Planck-Pi

[peng-zhihui/Planck-Pi: Super TINY & Low-cost Linux Develop-Kit Based On F1C200s. (github.com)](https://github.com/peng-zhihui/Planck-Pi)

本项目是一个基于全志F1C200s芯片的超迷你&低成本的Linux开发板，复刻进度止于登录进Linux开发板，软件层面未作探索

仅复刻硬件就踩了不少坑，密集管脚的QFN芯片焊接手法要更加细腻，烧录系统也需要选择好合适的软件和SD卡，耗时较长的项目复刻

登录系统没问题

![image-20240228140015159](Readme.assets/image-20240228140015159.png)

![image-20240228140021371](Readme.assets/image-20240228140021371.png)

![image-20240228140052324](Readme.assets/image-20240228140052324.png)

![image-20240228140057397](Readme.assets/image-20240228140057397.png)

![image-20240228140103049](Readme.assets/image-20240228140103049.png)

![image-20240228140111229](Readme.assets/image-20240228140111229.png)

![image-20240228140116579](Readme.assets/image-20240228140116579.png)

![image-20240228140043222](Readme.assets/image-20240228140043222.png)

![image-20240228140032136](Readme.assets/image-20240228140032136.png)

## 8、跨阻放大器外围电路设计

该项目不方便开放，主要是一款跨阻的外围电路设计，涉及高频信号线的处理，对比官方的评估板卡，我设计的板卡在高频点总是有一个噪声的尖峰，板卡迭代数次均未消除，后面将板卡的材料换成高频PCB，即特氟龙材料才得到大大改善，但是带宽依旧不能达到芯片标称的750MHz，随后想找出问题，接触到信号完整性问题

去跟成都的一家硬件公司的工程师做过交流，问题应该还是出在阻抗上面，电源带来的噪声不会那么稳定

另外工程师提到，普通的FR4板材的PCB板卡是可以做到8GHz的，我知道多层板的内部，有良好的参考平面对于重要的信号线是非常友好的，但是换层也意味着阻抗的失配，高频板为什么能消除那个高频的噪声是因为高频材料的平面非常平整，阻抗连续性很好，FR4材料的表面就像衣服的纤维一样，非常粗糙，阻抗连续性比较差，所以信号的带宽越高，信号的失真就越严重，引起的各种信号反射叠加等也会越严重

## 9、开发板学习记录

学过的开发板比较多，有自己买的，也有比赛用的，记录一下

<img src="Readme.assets/image-20240302101919886.png" alt="image-20240302101919886" style="zoom:160%;" />

![image-20240302101928766](Readme.assets/image-20240302101928766.png)

<img src="Readme.assets/image-20240302101955774.png" alt="image-20240302101955774" style="zoom:110%;" />

<img src="Readme.assets/image-20240302102024861.png" alt="image-20240302102024861" style="zoom:180%;" />

<img src="Readme.assets/image-20240302101945422.png" alt="image-20240302101945422" style="zoom:53%;" />

![image-20240302102008125](Readme.assets/image-20240302102008125.png)











































