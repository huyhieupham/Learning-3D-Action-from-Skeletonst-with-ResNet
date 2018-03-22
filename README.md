# Learning-and-Recognizing-Human-Action-from-Skeleton-Movement-with-Deep-Residual-Neural-Networks
This repository is an implementation of "[Learning and Recognizing Human Action from Skeleton Movement with Deep Residual Neural Networks (ICPRS-17)](https://arxiv.org/pdf/1803.07780.pdf)" by Huy-Hieu Pham, Louahdi Khoudour, Alain Crouzil, Pablo Zegers, and Sergio A. Velastin. We propose the use of Deep Residual Neural Networks (ResNets) to learn and recognize human action from skeleton data provided by Kinect sensor. The body joint coordinates are transformed into 3D-arrays and saved in RGB images space. Five different deep learning models based on ResNet have been designed to extract image features and classify them into classes. 


**Model**


We propose a data transformation module which allows us to encode skeleton sequences into 3D-arrays and store them in color images. The skeleton data is captured in frames, each frame contains the 3D coordinates of skeletal joints. We transform all the 3D coordinates of each frame into a new space by normalizing these coordinates by the transformation function:
<p align="center">
![image-1](https://github.com/huyhieupham/Learning-and-Recognizing-Human-Action-from-Skeleton-Movement-with-Deep-Residual-Neural-Networks/blob/master/figure/data-transformation.png)
</p>

