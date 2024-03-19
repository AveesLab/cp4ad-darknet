# [Week 5] Object Detection
## We try ...
### 1. Object Detection using Darknet (CPU, GPU)
**Installation**
step1. git clone
```
$ git clone https://github.com/AveesLab/cp4ad-darknet.git
$ cd cp4ad-darknet/
```
step2. download yolov4-tiny weights file
```
$ wget https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v4_pre/yolov4-tiny.weights
```
**Inference only using CPU**
```
$ vim Makefile
```
```
GPU = 0
CUDNN = 0
OPENCV = 1
```
```
$ make -j6
$ ./darknet detector demo cfg/coco.data cfg/yolov4-tiny.cfg yolov4-tiny.weights data/highway.mp4
```

**Inference using GPU**
```
$ vim Makefile
```
```
GPU = 1
CUDNN = 0
OPENCV = 1
```
```
$ make -j6
$ ./darknet detector demo cfg/coco.data cfg/yolov4-tiny.cfg yolov4-tiny.weights data/highway.mp4
```
### 2. MonoCamera Distance Estimation

```
$ code src/
```

```
$ make -j6
$ ./darknet detector demo cfg/coco.data cfg/yolov4-tiny.cfg yolov4-tiny.weights data/highway.mp4
```
