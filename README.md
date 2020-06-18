# Jetson_nano

<p align="center">
  <img src="https://github.com/hsiehchungting/Jetson-nano/blob/master/jetson nano.jpg" width="280">
</p>

# Jetson-nano-basic-install
This is about my jetson nano install information (wifi 、camera)

HARDWARD
WIFI :EW-7811un V2

https://shopee.tw/%E3%80%903CTOWN%E3%80%91%E9%99%90%E9%87%8F-%E5%90%AB%E7%A8%85%E9%99%84%E7%99%BC%E7%A5%A8-EDIMAX%E8%A8%8A%E8%88%9F-EW-7811Un-N150-%E9%AB%98%E6%95%88%E8%83%BD%E9%9A%B1%E5%BD%A2USB%E7%84%A1%E7%B7%9A%E7%B6%B2%E8%B7%AF%E5%8D%A1-i.26185755.648623767

DRIVER
https://www.edimax.com/edimax/download/download/data/edimax/global/download/product/wireless_adapters/wireless_adapters_n150/ew-7811un_v2/

*** Here has a point notice the wifi tool has two vision and then there driver is different*****


# Jetson-nano-virtual environment

building a virtual environment on Jetson nano


install virtual environment
```
sudo apt-get install virtualenv -y
```

```
mkdir envs
```

```
cd envs
```
building a virtual environment name(testenv)
```
virtualenv –p python3 testenv
```
activate testenv
```
source ~/envs/testenv/bin/activate
```
writing your virtual environment into your bashrc (restart your nano don't disappear)
``` 
echo ' source ~/envs/testenv/bin/activate ' >> ~/.bashrc
```

OPENCV is already install but need to link to your environment
```
sudo find / -name "cv2*"
```
find out cv2 path (aarch64-linux-gnu.so)
```
find: ‘/run/user/1000/gvfs’: Permission denied

/usr/lib/python2.7/dist-packages/cv2.so

**/usr/lib/python3.6/dist-packages/cv2.cpython-36m-aarch64-linux-gnu.so**
```

```
cd ~/envs/AI/lib/python3.6/site-packages/
```
linking your path 
```
ln -s /usr/lib/python3.6/dist-packages/cv2.cpython-36m-aarch64-linux-gnu.so
```
