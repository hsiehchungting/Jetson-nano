# Jetson_nano

<p align="center">
  <img src="https://github.com/hsiehchungting/Jetson-nano/blob/master/Driver/EW-7811Un_V2_Linux_Driver_1.0.0.3/rtl8188EUS_linux_v5.3.9_28540.20180627//EW-7811Un_v2.jpg" width="280">
</p>

# Jetson-nano-basic-install
This is about my jetson nano install information (wifi 、camera)

HARDWARD
WIFI :EW-7811un V2

https://shopee.tw/%E3%80%903CTOWN%E3%80%91%E9%99%90%E9%87%8F-%E5%90%AB%E7%A8%85%E9%99%84%E7%99%BC%E7%A5%A8-EDIMAX%E8%A8%8A%E8%88%9F-EW-7811Un-N150-%E9%AB%98%E6%95%88%E8%83%BD%E9%9A%B1%E5%BD%A2USB%E7%84%A1%E7%B7%9A%E7%B6%B2%E8%B7%AF%E5%8D%A1-i.26185755.648623767

DRIVER
https://www.edimax.com/edimax/download/download/data/edimax/global/download/product/wireless_adapters/wireless_adapters_n150/ew-7811un_v2/

*** Here has a point notice the wifi tool has two vision and then there driver is different*****
### Installation of Driver
make sure your system is update
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
```

download your wifi driver(top has my wifi driver web)

open your terminal
```
cd Download(find out your driver zip file)
```

make your file
```
make
(now maybe your will get error. you can use nano editor your Makefile)
```
<p align="center">
  <img src="https://github.com/hsiehchungting/Jetson-nano/blob/master/Driver/EW-7811Un_V2_Linux_Driver_1.0.0.3/rtl8188EUS_linux_v5.3.9_28540.20180627/error1.jpg" width="200">
</p>

```
nano Makefile 
ADD the sentence
 “export ARCH=arm64”
```

successly make your file
```
sudo make install
```

restart your jetson nano
```
sudo reboot
```
