---
title: 两个有用的脚本, 测试接口每秒通过的数据包和测试网络带宽
layout: post
tags:
- code
- pyhon
- c language
- java
- rails
- ruby
- linux command
- Shell Script
---

测试接口每秒通过的数据包

```bash
#!/bin/bash
# 文件名: Test_pkts
# 测试接口每秒通过的数据包
# 使用方法: $./Test_pkts eth0
#
INTERVAL="1"  
if [ -z "$1" ]; then
          echo
          echo usage: $0 'network-interface'
          echo
          echo e.g. $0 eth0
          echo
          echo shows packets-per-second
          exit
fi

IF=$1

while true
do
          R1=`cat /sys/class/net/$1/statistics/rx_packets`
          T1=`cat /sys/class/net/$1/statistics/tx_packets`
          sleep $INTERVAL
          R2=`cat /sys/class/net/$1/statistics/rx_packets`
          T2=`cat /sys/class/net/$1/statistics/tx_packets`
          TXPPS=`expr $T2 - $T1`
          RXPPS=`expr $R2 - $R1`
          echo "TX $1: $TXPPS pkts/s RX $1: $RXPPS pkts/s"
done

```

```bash
#!/bin/bash
# 文件名: Test_kbs
# 测试网络带宽
# 使用方法: $./Test_kbs eth0
#
INTERVAL="1"

if [ -z "$1" ]; then
          echo
          echo usage: $0 'network-interface'
          echo
          echo e.g. $0 eth0
          echo
          exit
fi

IF=$1

while true
do
          R1=`cat /sys/class/net/$1/statistics/rx_bytes`
          T1=`cat /sys/class/net/$1/statistics/tx_bytes`
          sleep $INTERVAL
          R2=`cat /sys/class/net/$1/statistics/rx_bytes`
          T2=`cat /sys/class/net/$1/statistics/tx_bytes`
          TBPS=`expr $T2 - $T1`
          RBPS=`expr $R2 - $R1`
          TKBPS=`expr $TBPS / 1024`
          RKBPS=`expr $RBPS / 1024`
          echo "TX $1: $TKBPS kb/s RX $1: $RKBPS kb/s"
done

```
