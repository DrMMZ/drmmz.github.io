**[Tracking from Faces](https://github.com/DrMMZ)**

Jesus Christ it's Jason Bourne! Can we track him?

A tracker built from [object detection](https://github.com/DrMMZ/RetinaNet) and [few-shot learning](https://github.com/DrMMZ/ProtoNet), allows us to detect and recognize faces.
<p align="center">
<video src="https://user-images.githubusercontent.com/38026940/132160401-ee1f22ca-0b0f-4471-8b62-6144c76cf21c.mp4" controls="controls" style="max-width: 380px;"></video>
</p>
Scenes are taken from *The Bourne Ultimatum (2007 film)* and the cover page is from *The Bourne Identity (2002 film)*.

----

**[ProtoNet for Few-Shot Learning](https://github.com/DrMMZ/ProtoNet)**

By just learning few face images from a random person, the [algorithm](https://github.com/DrMMZ/ProtoNet) is able to identify and recognize that person effectively from a group of people. Below are samples tested on the [CelebA](https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html) dataset.
<p align="center">
  <img src="https://raw.githubusercontent.com/DrMMZ/drmmz.github.io/master/images/celeba/7.JPG" width='380' height='420'/>
  <img src="https://raw.githubusercontent.com/DrMMZ/drmmz.github.io/master/images/celeba/12.JPG" width='380' height='420'/>
</p> 
In each sample, there are 3 face images learned by the model (under the text "Learning") and a group of 15 people face images to find that person (under the text 'Recognizing') where the correct recognization is labeled by "match" in green color and the wrong recognization has "ground-truth" and "predict" in red color.
<p align="center">
  <img src="https://raw.githubusercontent.com/DrMMZ/drmmz.github.io/master/images/celeba/2.JPG" width='380' height='420'/>
  <img src="https://raw.githubusercontent.com/DrMMZ/drmmz.github.io/master/images/celeba/celeba_movie.gif" width='380' height='420'/>
</p> 

----

**[RetinaNet for Object Detection](https://github.com/DrMMZ/RetinaNet)**

[RetinaNet](https://arxiv.org/abs/1708.02002) is an efficient one-stage object detector trained with the focal loss. This [repository](https://github.com/DrMMZ/RetinaNet) is a TensorFlow2 implementation of RetinaNet and its applications, aiming for creating a tool in object detection task that can be easily extended to other datasets or used in building projects.

The following are example real-time detections using RetinaNet, randomly selected from un-trained images.

* My own dataset, *empty returns operations (ERO-CA)*, is a collection of images such that each contains empty beer, wine and liquor cans or bottles in densely packed scenes that can be returned for refunds in Canada. The goal is to count the number of returns fast and accurately, instead of manually checking by human (specially for some people like me who is bad on counting). The dataset (as of July 15 2021) consists of 47 labeled cellphone images in cans, variety of positions. If you are interested in contributing to this dataset or project, please [email](mailto:mmzhangist@gmail.com) me. 
<p align="center">
  <img src="https://raw.githubusercontent.com/DrMMZ/drmmz.github.io/master/images/ero_movie.gif" width='360' height='360'/>
</p> 

* The [SKU-110K](https://github.com/eg4000/SKU110K_CVPR19) dataset, focusing on detection in densely packed scenes. Indeed, our ERO-CA detection above used transfer learning from it.
<p align="center">
  <img src="https://raw.githubusercontent.com/DrMMZ/drmmz.github.io/master/images/sku_movie.gif" width='360' height='360'/>
</p>

* The [nuclei](https://www.kaggle.com/c/data-science-bowl-2018) dataset, identifying the cells’ nuclei. 
<p align="center">
  <img src="https://raw.githubusercontent.com/DrMMZ/drmmz.github.io/master/images/nuclei_movie.gif" width='360' height='360'/>
</p> 

----

**[Ensemble Model: ResNet + FPN](https://github.com/DrMMZ/ResFPN)**

This is an implementation of [*ResFPN*](https://github.com/DrMMZ/ResFPN) on Python 3 and TensorFlow 2. The model classifies images by ensembling predictions from [Residual Network](https://arxiv.org/abs/1512.03385) (ResNet) and [Feature Pyramid Network](https://arxiv.org/abs/1612.03144) (FPN), and can be trained by minimizing [focal loss](https://arxiv.org/abs/1708.02002). 

Below are example classifications using ResFPN on the [tf_flowers](https://www.tensorflow.org/datasets/catalog/tf_flowers) dataset randomly selected from un-trained images.

<p align="center">
  <img src="https://raw.githubusercontent.com/DrMMZ/drmmz.github.io/master/images/flower_movie.gif" width='480' height='360'/>
</p>
