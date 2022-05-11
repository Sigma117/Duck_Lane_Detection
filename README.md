# Duck_Lane_Detection
Development and experimentation of a neural network for the autonomous recognition of the roadway, with application to mobile robotics.


This work was created starting from data recorded in the environment of Duckietown, a simulated city in which there are small mobile robots called duckiebots, which imitate a car that circulates on the streets of this city. The CNN used in this work it is taken by (Zou, Qin, et al. "Robust Lane detection from continuous driving scenes using deep neural networks." IEEE transactions on vehicular technology 69.1. [github Link](https://github.com/Sigma117/Robust-Lane-Detection))

The aim of this work is to develop a system that is able to recognize the roadway lines of a street using a CNN, starting from videos recorded by the duckiebot while traveling around the Duckietown. 

# Some results
![IMAGE 2022-05-11 10:29:52](https://user-images.githubusercontent.com/71655239/167804918-ed84ef20-5f49-4d8f-b17c-ea0e3554912b.jpg) ![IMAGE 2022-05-11 10:30:03](https://user-images.githubusercontent.com/71655239/167804960-b2f1212d-43e4-43d2-a08e-83ad54c7c529.jpg) ![IMAGE 2022-05-11 10:30:26](https://user-images.githubusercontent.com/71655239/167805059-af89fd25-cfe1-484c-83c6-cb7282ee0689.jpg)


![IMAGE 2022-05-11 10:29:57](https://user-images.githubusercontent.com/71655239/167804934-f9d6e8b9-c861-4220-ad93-3941c6d9824f.jpg) ![IMAGE 2022-05-11 10:30:09](https://user-images.githubusercontent.com/71655239/167804985-70d3dcba-5dcd-46fa-a0c6-1e8893efb320.jpg) ![IMAGE 2022-05-11 10:30:29](https://user-images.githubusercontent.com/71655239/167805069-1588e18a-1e4f-41ab-927c-1181181548ef.jpg)

# Description (dataset)

The dataset used in this work contains 7820 images extracted from 391 videos taken by the Duckietown servers ([Duckitown Videos link](http://ipfs.duckietown.org:8080/ipfs/QmUbtwQ3QZKmmz5qTjKM3z8LJjsrKBWLUnnzoE5L4M7y7J/logs/gallery.html)). Among those images, 782 have been labeled. 
The size of the images in this dataset is 256 x 128 RGB, while for the labeled images is 256 x 128 Gray Scale.

the whole data set was created starting from the videos taken from the site 

Data Costruction
- 256 x 128 RGB (images)
- 256 x 128 Gray scale (labels)
- Each 13th and 20th frame in a sequence are labeled
- Each folder consists of 20 images which are a sequence of a 4 second video

## Using

If you want to use the same CNN please look at the paper [github Link](https://github.com/Sigma117/Robust-Lane-Detection) everything is described

### Requirement
- PyTorch 0.4.0
- Python 3.6
- CUDA 8.0

## Pretrained model


In this work i show only preterened model, if you want train your ouw model you can download my dataset and take the CNN from the link in the Using section.

To make the pre-trained model work, you need to do this steps.
- Download all Duck folder [Duck](https://github.com/Sigma117/Duck_Lane_Detection/tree/main/Duck)
- Download the Test set
- Open Config.py file and change all path in your path
- Lanch file Test.py

If you want try different images you just need to add them on the test set and change the Test_index.txt (in this case you can use one of my random labels, you cont need to create as you own labels)

## Download

You can download this dataset from the link:
- [Train_Duck](https://drive.google.com/drive/folders/1izZTAy_6rkxxlPdOxZ9V6tvzsYUJbYBU?usp=sharing)
- [Labels](https://drive.google.com/drive/folders/1jNy0ZBTjs7w74amte1DpFpBuoLzrU_FF?usp=sharing)
- [Test_set](https://drive.google.com/drive/folders/11A-0cB7XQtpLR-CAJVxTIYlRb9RuAbSY?usp=sharing)
- [Pretreined CNN](https://drive.google.com/file/d/1-zITlwEgOUXbFkGLD1BTfzA9tWzYM9Ac/view?usp=sharing)
