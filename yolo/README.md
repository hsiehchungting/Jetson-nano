# download yolo github


```
git clone https://github.com/AlexeyAB/darknet
```
# download weights
you can download that you want get weights

```
wget https://pjreddie.com/media/files/yolov3.weights
wget https://pjreddie.com/media/files/yolov3-tiny.weights
```

# Enable the GPU

```
sudo vi Makefile
```
Set the values:
GPU=1
CUDNN=1
OPENCV=1

#Compile the Darknet
```
sudo make
```

#start your yolo file
```
cd darknet
```

use your webcam
```
./darknet detector test cfg/coco.data yolov3.cfg yolov3.weights -c 0

```

use yolo on your mp4
```
./darknet detector test cfg/coco.data yolov3.cfg yolov3.weights test.mp4 

```

reference
1.https://github.com/AlexeyAB/darknet

2.https://pysource.com/2019/08/29/yolo-v3-install-and-run-yolo-on-nvidia-jetson-nano-with-gpu/