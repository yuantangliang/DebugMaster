# ProtocolMaster
协议大师可以解析各种协议，支持各种信道，并且易于扩展。
 
本项目的目的就是设计一款上位机，可以解析各种协议。帮助人员从日常繁琐的解析报文的工作中解脱出来。

## 主要特点
1. 通用UI。  UI为通用的，可以方便的将数据通过不同的UI展示出来。
2. 可扩展协议。 协议大师可以非常方便的扩展调试协议。
3. 可扩展信道。 协议大师在编写的时候就已经考虑到扩展信道的功能，用户可以非常方便的扩展信道。
4. 支持事物。 对于上位机调试过程中，经常会有统计成功率，升级等一系列固定要求序列的报文要求，在此上位机中使用事物来抽象这种需求。
5. 面向设备。 设备为协议+UI+信道+日常routine的集合。通过设备用户可以非常方便的创建配置，调试。

## 主要设计方案对比：
1. 使用qt编写所有功能。 优点：代码简单。 缺点：扩展比较麻烦，需要重新编译代码。
2. 使用qt编写界面，qtlua进行协议解析。 优点：扩展灵活  缺点：qt和lua需要定义交互接口。
3. 使用pyqt编写。 扩展和编写都比较简单。（采用此方案）

## 计划支持的协议：
1. 645协议
2. ymodem
3. http

## 计划支持的信道：
1. 串口
2. TCP
3. UDP
4. JLink RTT 
5. 复制和黏贴

## 计划支持logger
1. logger到文件
2. logger到数据库
3. logger调试窗口

## 计划支持显示格式：
1. 图像 raw  jpeg bmp
2. 文本
3. 16进制

## 计划支持的事务
1. sequenc事务 定义一系列相关报文的收发，主要用于设备升级。
2. repeat事务  定义重发收发的报文，主要用于设备成功率统计、收集设备状态。

# 计划支持平台
1. iOS、安卓、windows、linux
