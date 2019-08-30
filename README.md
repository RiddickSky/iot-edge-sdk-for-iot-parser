百度物联网物解析网关
====================

介绍
----
百度物联网物解析网关可以帮助用户采集Modbus/BACNet协议数据，并且通过百度物联网的MQTT协议上传到云端，然后可以在云端进行处理、归档、入库以及可视化。
网关需要运行在与你的Modbus/BACNet设备相连或者想通的计算机或者开发板上，以便其能采集到相关数据。目前支持Linux操作系统，并且提供ubuntu的一键安装脚本。

网关工作原理
------------
网关从本地配置文件读取MQTT连接信息，并且订阅一个指定的MQTT主题，以接受数据采集策略。采集策略包括采集哪些设备的哪些数据、采集频率多少等等。数据采集到后，通过另外一个MQTT主题发布到物接入。

目录结构
--------
 - modbus: modbus网关
 - bacnet: bacnet网关

安装
----
两个网关需要分别编译，安装步骤请参考相关的ubuntu-install*.sh文件。