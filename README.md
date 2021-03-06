# Datasets-auto-generator-based-on-Blender
This code generates image datasets with annotations and labels for training your neural network by one click.

# Platform
Using **Blender 2.91** on **Pop!\_OS 20.04 LTS**

# Getting Started
1) Prepare your 3D models (\*.blend files) and backgrounds (\*.hdr files).
2) Paste the code into **Blender Scripting Window** and change to absolute paths of your models folder and backgrounds folder, unless you know where your *blender script* placed.
3) Chage some variables like *image numbers* etc. 
4) **Note that this code also generates KITTI format dataset for my other project, and it's not 100% correct for other general using. But the COCO dataset does.**

# Result
Detection using [YOLOv5](https://github.com/ultralytics/yolov5) trained by generated dataset
![image](https://github.com/Siidej/Datasets-auto-generator-based-on-Blender/blob/main/imgForIntro/test.png) 
![image](https://github.com/Siidej/Datasets-auto-generator-based-on-Blender/blob/main/imgForIntro/res.png)

# For real object detection
According to this [paper](https://arxiv.org/abs/1811.12231), pay attention to the texture of model to render.
## real object detection using YOLOv5 trained by fake dataset  
![image](https://github.com/Siidej/Datasets-auto-generator-based-on-Blender/blob/main/imgForIntro/fake.png) 
![image](https://github.com/Siidej/Datasets-auto-generator-based-on-Blender/blob/main/imgForIntro/detection.png)  
Note: For saving time, used Evee (Blender real-time render engine) to render the training set (1500 images) and Cycles to render the validation set (500 images). So, theoretically, using Cycles for both will have a better performance. 
