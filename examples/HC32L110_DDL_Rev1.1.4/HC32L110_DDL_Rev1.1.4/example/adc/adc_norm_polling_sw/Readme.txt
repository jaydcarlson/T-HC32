﻿================================================================================
                                样例使用说明
================================================================================
版本历史 
日期        版本    负责人         IAR     MDK   描述
2018-09-12  0.2     Husj           7.70    5.16a first version
================================================================================
功能描述
================================================================================
本样例主要展示ADC 单次采样示例，使用轮询方式获取ADC运行状态。
说明：
    配置ADC并开始采样，轮询ADC状态，转换完成时读取转换结果(每1000毫秒一次）

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
1）编译下载
2）使用内部2.5参考电压
3）ADC使用通道0，P24和通道1，P26。
4）在IAR的livewatch或KEIL的Watch窗口观察变量u16AdcResult的值


================================================================================
注意
================================================================================
1）内置电压跟随器使能可以采样外部高阻信号，但是BUFEN使能后，最高SPS采样速率 <= 200K

2）参考电压:内部2.5V(Vcc > 2.8V,SPS <= 200kHz)  

3）参考电压:内部1.5V(Vcc > 1.8V,SPS <= 200kHz)  

4）SPS速率 = ADC时钟 / (采样时钟 + 16CLK) 
================================================================================
