# Readme

pengxuexi's learning records——Timeline

---

涉及技能：

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

![image-20240228093420433](Readme.assets/image-20240228093420433.png)

![image-20240228093427170](Readme.assets/image-20240228093427170.png)

![image-20240228093438659](Readme.assets/image-20240228093438659.png)

## 6、复刻ST-Link-Nano

是一个超迷你的ST-Link模块，相较于市面上的stlink，有typec的接口，并且非常mini，成本低，复刻很成功，焊接注意细节就好。验证烧录也没有问题

![image-20240228093757062](Readme.assets/image-20240228093757062.png)

![image-20240228093805312](Readme.assets/image-20240228093805312.png)

![image-20240228093811029](Readme.assets/image-20240228093811029.png)

![image-20240228093819379](Readme.assets/image-20240228093819379.png)

## 7、



































