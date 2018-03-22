# Learning-and-Recognizing-Human-Action-from-Skeleton-Movement-with-Deep-Residual-Neural-Networks
This repository is an implementation of "[Learning and Recognizing Human Action from Skeleton Movement with Deep Residual Neural Networks (ICPRS-17)](https://arxiv.org/pdf/1803.07780.pdf)" by Huy-Hieu Pham, Louahdi Khoudour, Alain Crouzil, Pablo Zegers, and Sergio A. Velastin. We propose the use of Deep Residual Neural Networks (ResNets) to learn and recognize human action from skeleton data provided by Kinect sensor. The body joint coordinates are transformed into 3D-arrays and saved in RGB images space. Five different deep learning models based on ResNet have been designed to extract image features and classify them into classes. 


**Model**


We propose a data transformation module which allows us to encode skeleton sequences into 3D-arrays and store them in color images. The skeleton data is captured in frames, each frame contains the 3D coordinates of skeletal joints. We transform all the 3D coordinates of each frame into a new space by normalizing these coordinates by the transformation function:
<p align="center"> 
<img src="https://github.com/huyhieupham/Learning-and-Recognizing-Human-Action-from-Skeleton-Movement-with-Deep-Residual-Neural-Networks/blob/master/figure/data-transformation.png">
</p>
<p align="center"> 
Figure 1: Normalizing the 3D joint coordinates into the range [1,255] 
</p>
By this way, each skeleton sequence is encoded into a single RGB image. The following picture describes this process. We then design different ResNet architetures for learning the spatial-temporal information from RGB-coded images for recognition tasks.
<p align="center"> 
<img src="https://github.com/huyhieupham/Learning-and-Recognizing-Human-Action-from-Skeleton-Movement-with-Deep-Residual-Neural-Networks/blob/master/figure/data-transformation-process.png">
</p>
<p align="center"> 
Figure 2: Illustration of the data transformation process. N denotes the number of frames in each sequence. K denotes the number of joints in each frame.
</p>
<p align="center"> 
<img src="https://github.com/huyhieupham/Learning-and-Recognizing-Human-Action-from-Skeleton-Movement-with-Deep-Residual-Neural-Networks/blob/master/figure/resnet.png">
</p>
<p align="center"> 
    Figure 3: A building block of ResNet.
  </p>
  
  **Training and results**


Before running the experiments, you need to download and compile [VLFeat](http://www.vlfeat.org/), and [MatConvNet](http://www.vlfeat.org/matconvnet/). Then, start to train ResNets on GPU by the following commande:


 ```experiments([20 32 44 56 110], 'gpus', [1]);```

  
  <p align="center"> 
<img src="https://github.com/huyhieupham/Learning-and-Recognizing-Human-Action-from-Skeleton-Movement-with-Deep-Residual-Neural-Networks/blob/master/figure/Training.png">
</p>
<p align="center"> 
   Learning curves on MSR Action3D/AS1 dataset. Dashed lines denote training errors (%), bold lines denote testing errors (%).
  </p>
  
  
  


