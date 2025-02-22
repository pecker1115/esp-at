.. include:: ../../inline_substitutions

ESP-AT 固件差异
====================

:link_to_translation:`en:[English]`

本文档比较了同一 ESP 系列的 AT 固件在支持的命令集、硬件、模组方面的差异。

ESP32 系列
------------

本节介绍以下 ESP32 系列 AT 固件的区别：

- ESP32-WROOM-32_AT_Bin（本节简称为 **WROOM Bin**）
- ESP32-WROVER-32_AT_Bin（本节简称为 **WROVER Bin**）
- ESP32-PICO-D4_AT_Bin（本节简称为 **PICO-D4 Bin**）
- ESP32-SOLO-1_AT_Bin（本节简称为 **SOLO-1 Bin**
- ESP32-MINI-1_AT_Bin（本节简称为 **MINI-1 Bin**）
- ESP32-D2WD_AT_Bin（本节简称为 **D2WD Bin**）
- ESP32-QLOUD_AT_Bin（本节简称为 **QCLOUD Bin**）

支持的命令集
^^^^^^^^^^^^

下表列出了官方适配的 ESP32 系列 AT 固件默认支持哪些命令集（用 |icon-green-check| 表示）、默认不支持但可以在配置和编译 ESP-AT 工程后支持的命令集（用 |icon-orange-check| 表示）、完全不支持的命令集（用 |icon-red-cross| 表示），下表没有列出的命令集也为完全不支持的命令集。正式发布的固件见 :doc:`../AT_Binary_Lists/index`，已适配但未发布的模组固件，需要自行编译。自行编译的固件无法从乐鑫官方服务器进行 OTA 升级。

.. list-table::
   :header-rows: 1

   * - 命令集
     - WROOM Bin
     - WROVER Bin
     - PICO-D4 Bin
     - SOLO-1 Bin
     - MINI-1 Bin
     - D2WD Bin
     - QCLOUD Bin
   * - base
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
   * - user
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
   * - wifi
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
   * - net
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
   * - MDNS
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
   * - WPS
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
   * - smartconfig
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
   * - ping
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
   * - MQTT
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
   * - http
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
   * - ble
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
   * - ble hid
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
   * - blufi
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
   * - bt spp
     - |icon-orange-check|
     - |icon-green-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
   * - bt a2dp
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
   * - ethernet
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
   * - FS
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
   * - driver
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
   * - WPA2
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
   * - WEB
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
   * - OTA
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-green-check|
   * - qcloud IoT
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-orange-check|
     - |icon-green-check|

硬件差异
^^^^^^^^

.. list-table::
   :header-rows: 1

   * - 硬件
     - WROOM Bin
     - WROVER Bin
     - PICO-D4 Bin
     - SOLO-1 Bin
     - MINI-1 Bin
     - D2WD Bin
     - QCLOUD Bin
   * - Flash
     - 4 MB
     - 4 MB
     - 4 MB
     - 4 MB
     - 4 MB
     - 2 MB
     - 4 MB
   * - PSRAM
     - |icon-red-cross|
     - 8 MB
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-red-cross|
   * - UART 管脚 [#one]_
     - | TX: 17
       | RX: 16
       | CTS: 15
       | RTS: 14
     - | TX: 22 
       | RX: 19 
       | CTS: 15
       | RTS: 14
     - | TX: 22 
       | RX: 19 
       | CTS: 15
       | RTS: 14
     - | TX: 17 
       | RX: 16 
       | CTS: 15 
       | RTS: 14
     - | TX: 22 
       | RX: 19 
       | CTS: 15
       | RTS: 14
     - | TX: 22 
       | RX: 19 
       | CTS: 15
       | RTS: 14
     - | TX: 17 
       | RX: 16 
       | CTS: 15 
       | RTS: 14

.. [#one] UART 管脚可自定义，详情请参考 :doc:`How_to_set_AT_port_pin`。

支持的模组
^^^^^^^^^^

下表列出了 ESP32 系列 AT 固件支持的模组或芯片。

.. list-table::
   :header-rows: 1

   * - 模组/芯片
     - WROOM Bin
     - WROVER Bin
     - PICO-D4 Bin
     - SOLO-1 Bin
     - MINI-1 Bin
     - D2WD Bin
     - QCLOUD Bin
   * - ESP32-WROOM-32E
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-green-check|
   * - ESP32-WROOM-32UE
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-green-check|
   * - ESP32-WROOM-32D
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-green-check|
   * - ESP32-WROOM-32U
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-green-check|
   * - ESP32-WROOM-32
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-green-check|
   * - ESP32-WROOM-32SE
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-red-cross|
   * - ESP32-WROVER-E
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-red-cross|
   * - ESP32-WROVER-IE
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-red-cross|
   * - ESP32-WROVER-B
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-red-cross|
   * - ESP32-WROVER-IB
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-red-cross|
   * - ESP32-WROVER
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-red-cross|
   * - ESP32-WROVER-I
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-red-cross|
   * - ESP32-SOLO-1
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-green-check|
   * - ESP32-D2WD
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-red-cross|
   * - ESP32-MINI-1
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-red-cross|
   * - ESP32-PICO-D4
     - |icon-red-cross|
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-red-cross|
     - |icon-green-check|
     - |icon-green-check|
     - |icon-red-cross|

ESP32-C3 系列
----------------

本节介绍以下 ESP32-C3 系列 AT 固件的区别：

- ESP32-C3-MINI-1_AT_Bin（本节简称为 **MINI-1 Bin**）
- ESP32-C3-QCLOUD_AT_BIN（本节简称为 **QCLOUD Bin**）

支持的命令集
^^^^^^^^^^^^

下表列出了官方适配的 ESP32-C3 系列 AT 固件默认支持哪些命令集（用 |icon-green-check| 表示）、默认不支持但可以在配置和编译 ESP-AT 工程后支持的命令集（用 |icon-orange-check| 表示）、完全不支持的命令集（用 |icon-red-cross| 表示），下表没有列出的命令集也为完全不支持的命令集。正式发布的固件见 :doc:`../AT_Binary_Lists/index`，已适配但未发布的模组固件，需要自行编译。自行编译的固件无法从乐鑫官方服务器进行 OTA 升级。

.. list-table::
   :header-rows: 1

   * - 命令集
     - MINI-1 Bin
     - QCLOUD Bin
   * - base
     - |icon-green-check|
     - |icon-green-check|
   * - user
     - |icon-green-check|
     - |icon-green-check|
   * - wifi
     - |icon-green-check|
     - |icon-green-check|
   * - net
     - |icon-green-check|
     - |icon-green-check|
   * - MDNS
     - |icon-green-check|
     - |icon-green-check|
   * - WPS
     - |icon-green-check|
     - |icon-green-check|
   * - smartconfig
     - |icon-green-check|
     - |icon-green-check|
   * - ping
     - |icon-green-check|
     - |icon-green-check|
   * - MQTT
     - |icon-green-check|
     - |icon-green-check|
   * - http
     - |icon-green-check|
     - |icon-green-check|
   * - FS
     - |icon-orange-check|
     - |icon-orange-check|
   * - driver
     - |icon-orange-check|
     - |icon-orange-check|
   * - WPA2
     - |icon-orange-check|
     - |icon-orange-check|
   * - WEB
     - |icon-orange-check|
     - |icon-orange-check|
   * - OTA
     - |icon-green-check|
     - |icon-green-check|
   * - qcloud IoT
     - |icon-orange-check|
     - |icon-green-check|

硬件差异
^^^^^^^^

.. list-table::
   :header-rows: 1

   * - 硬件
     - MINI-1
     - QCLOUD
   * - Flash
     - 4 MB
     - 4 MB
   * - PSRAM
     - |icon-red-cross|
     - |icon-red-cross|
   * - UART 管脚 [#two]_
     - | TX: 7
       | RX: 6
       | CTS: 5
       | RTS: 4
     - | TX: 7
       | RX: 6
       | CTS: 5
       | RTS: 4

.. [#two] UART 管脚可自定义，详情请参考 :doc:`How_to_set_AT_port_pin`。

支持的模组
^^^^^^^^^^

下表列出了 ESP32-C3 系列 AT 固件支持的模组或芯片。

.. list-table::
   :header-rows: 1

   * - 模组/芯片
     - MINI-1 Bin
     - QCLOUD Bin
   * - ESP32-C3-MINI-1
     - |icon-green-check|
     - |icon-green-check|