# HT-M00双通道LoRa网关快速入门
[English](https://heltec-automation-docs.readthedocs.io/en/latest/gateway/ht-m00/qucik_start.html)

## 摘要

HT-M00是一个小体积、低成本的双通道LoRa网关，使用Type-C接口。HT-M00网关基于ESP32驱动两个SX1276芯片。我们编写了软件混频器（基带仿真程序），以实现对125KHz SF7~SF12扩频因子的监听 。HT-M00的主要功能是为1500~2000平方米的大型房屋提供LoRaWAN网络，或弥补SX1301网关信号无法覆盖的区域中信号的盲点。

```Tip:: 当使用HT-M00网关时，使用本公司CubeCell系列以外的节点，需要将节点的发射前导码长度更改为16（默认是8）。如果没有修改前导码长度为16，则只能收到SF7。

```

![](img/quick_start/08.png)

如上图所示修改该函数中的前导码长度为16。

&nbsp;

## 配置网关

HT-M00网关在出厂时已经烧录好了相关程序，只需进行一些简单的操作就能使用。

![](img/quick_start/01.png)

- 通过Type-C数据线给网关通电后，一直按住"CFG"按键，按下"RST"按键，然后松开"RST"按键，待网关进入下图所示界面后松开"CFG"按键。

![](img/quick_start/02.png)

- 此时找到名字为"M00_XXXX"的WiFi，并通过密码"heltec.org"连接上WiFi，然后进入"192.168.4.1"。

![](img/quick_start/03.png)

- 在上图所示页面配置HT-M00需要连接的WiFi信息，网关通道频率，扩频因子，服务器地址及端口，时区，配置完成后点击"Submit"。同时我们会将HT-M00的相关固件放到该网页，点击"Firmware Update"可进行相应更新。

- 配置完成并提交后网关将重启。网关开机时将会自动连接配置好的WiFi，如果连接失败，将再次重启，直至连接成功。

![](img/quick_start/04.png)

- WiFi连接成功后，网关将进入下图所示界面。

![](img/quick_start/05.png)

- 按下“STA"按键，可切换显示屏显示内容。

  ![](img/quick_start/06.png)

- 通过按下“STA"按键，可切换显示内容。可查看时间，最近收发时间，网关ID，服务器地址，通道频率等信息。

![](img/quick_start/07.png)
