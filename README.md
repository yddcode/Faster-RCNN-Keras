Cloned from https://github.com/yhenon/keras-rcnn

Added Chinese and Naxi detection data set.

XML: https://github.com/yddcode/yolo-keras/tree/main/VOCdevkit/VOC2007

labelme 生成的json文件：

链接：https://pan.baidu.com/s/1M-h4H6UL1PGztUaWMyLlZQ 提取码：hre8

Added resnet101 support.

# keras-frcnn
Keras implementation of Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks

USAGE:
- train_frcnn.py can be used to train a model. To train on Pascal VOC data, simply do:
python train_frcnn.py /path/to/pascalvoc/data/
- the Pascal VOC data set (images and annotations for bounding boxes around the classified objects) can be obtained from: http://host.robots.ox.ac.uk/pascal/VOC/voc2012/VOCtrainval_11-May-2012.tar

- simple_parser.py provides an alternative way to input data, using a text file. Simply provide a text file, with each
line containing:

filepath,x1,y1,x2,y2,class_name

For example:

/data/imgs/img_001.jpg,837,346,981,456,naxi

/data/imgs/img_002.jpg,215,312,279,391,chinese

- test_frcnn.py can be used to perform inference, given pretrained weights. Specify a path to the folder containing
images:

python test_frcnn.py /path/to/imgs/

/results_imgs is predicted image.

NOTES:
config.py contains all settings for the train or test run. The default settings match those in the original Faster-RCNN
paper. The anchor box sizes are [128, 256, 512] and the ratios are [1:1, 1:2, 2:1].

Example output:

![ex1](https://github.com/yddcode/Faster-RCNN-Keras/blob/main/results_imgs/0.png)
![ex2](https://github.com/yddcode/Faster-RCNN-Keras/blob/main/results_imgs/1.png)
![ex3](https://github.com/yddcode/Faster-RCNN-Keras/blob/main/results_imgs/2.png)
![ex4](https://github.com/yddcode/Faster-RCNN-Keras/blob/main/results_imgs/3.png)

# Useful Links
A report of this code from zhihu: https://zhuanlan.zhihu.com/p/28585873
