# STM32与ESP8266相互通信项目

## 项目描述

本项目展示了如何使用两个STM32F103C8T6微控制器通过ESP8266模块进行相互通信，并根据接收到的数据执行相应的指令。具体来说，一个STM32通过串口（PA9）连接到ESP8266（作为服务器）发送数据，例如：`LED1_ON`、`LED2_ON`、`LED3_ON`、`LED1_OFF`、`LED2_OFF`、`LED3_OFF`（数据可以根据需求自定义）。另一个STM32通过串口连接到ESP8266（作为客户端）接收数据，并根据接收到的指令执行相应的动作。

## 项目功能

1. **数据发送**：一个STM32通过串口向ESP8266发送指令数据。
2. **数据接收**：另一个STM32通过串口从ESP8266接收指令数据。
3. **指令执行**：接收数据的STM32根据接收到的指令控制相应的LED灯（或其他外设）。

## 硬件连接

- **STM32与ESP8266连接**：
  - STM32的串口（PA9）连接到ESP8266的TX端。
  - STM32的串口（PA10）连接到ESP8266的RX端。
  - ESP8266的VCC和GND分别连接到STM32的3.3V和GND。

- **两个STM32之间的连接**：
  - 两个STM32通过ESP8266进行无线通信。

## 软件实现

1. **服务器端（发送数据）**：
   - 初始化串口通信。
   - 通过串口发送指令数据到ESP8266。

2. **客户端（接收数据）**：
   - 初始化串口通信。
   - 通过串口接收来自ESP8266的指令数据。
   - 根据接收到的指令执行相应的操作（如控制LED灯的开关）。

## 使用说明

1. **硬件准备**：
   - 准备两个STM32F103C8T6开发板。
   - 准备两个ESP8266模块。
   - 按照硬件连接图进行连接。

2. **软件配置**：
   - 将服务器端和客户端的代码分别烧录到两个STM32开发板上。
   - 配置ESP8266的网络参数，确保两个ESP8266在同一网络下。

3. **运行测试**：
   - 启动两个STM32开发板，观察LED灯的状态变化，验证通信和指令执行是否正常。

## 注意事项

- 确保ESP8266的固件版本支持TCP/IP通信。
- 在配置ESP8266时，注意网络参数的设置，确保两个ESP8266能够正常通信。
- 在调试过程中，可以使用串口调试助手查看数据的发送和接收情况。

## 贡献

欢迎大家提出改进建议或提交代码优化，共同完善这个项目。

## 下载链接
[STM32与ESP8266相互通信项目](https://pan.quark.cn/s/561ecbd91580) 

(备用: [备用下载](https://pan.baidu.com/s/1PYxcDm1qi5sdeBjBO-liBw?pwd=1234))

## 说明

该仓库仅用于学习交流，请勿用于商业用途。
