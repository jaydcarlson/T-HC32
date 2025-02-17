﻿================================================================================
                                样例使用说明
================================================================================
版本历史 
日期        版本    负责人         IAR     MDK   描述
2018-09-12  0.2     Husj	   7.70    5.16a first version
================================================================================
功能描述
================================================================================
本样例主要展示ADC 多通道扫描采样示例，使用中断方式读取取ADC的采样值
说明：
    配置ADC并开始采样，ADC中断内读取各通道转换结果

================================================================================
测试环境
================================================================================
测试用板:
---------------------
HC32L110_STK

辅助工具:
---------------------
示波器
电源

辅助软件:
---------------------
无

================================================================================
使用步骤
================================================================================
1）ADC使用AIN0(P24)、AIN1(P26)、AIN2(P32)、AIN3(P33)、AIN4(P34)、AIN6(P36)
2）编译下载
3）在IAR的livewatch或KEIL的Watch窗口观察变量数组u16ScanResult[]的值。



================================================================================
注意
================================================================================
1）内置电压跟随器使能可以采样外部高阻信号，但是BUFEN使能后，最高SPS采样速率 <= 200K

2）参考电压:内部2.5V(Vcc > 2.8V,SPS <= 200kHz)  

3）参考电压:内部1.5V(Vcc > 1.8V,SPS <= 200kHz)  

4）SPS速率 = ADC时钟 / (采样时钟 + 16CLK) 

5）通道8（AIN8）不能用于扫描采样通道

================================================================================
