# Problem Statement:
The goal of this Assignment is to learn how to use CNNs: train from scratch, finetune a pretrained model, use a pre-trained model as it is.
The report of the project can be found at [this wandb link.](https://wandb.ai/tejoram/CS6910_Assignment2-Part-A/reports/Tejoram-Report-for-Assignment-2--VmlldzoxODE4MDEx)

# Prerequisites:
```
Python 3.7.10
Numpy 1.19.5
```

## Dataset:
We have used iNaturalist dataset [link.](https://storage.googleapis.com/wandb_datasets/nature_12K.zip).

## Installing:
+ Clone/download this repository.
+ For running in google colab, install wandb using following command - ```!pip install wandb```.
+ For running locally, install wandb using following command.
```
pip install wandb
pip install numpy
pip install tensorflow
```

## Part-A:
There are ten classes in the iNaturalist data set and here is a dictionary relating corresponding class names.
label={'Amphibia','Animalia','Arachnida','Aves','Fungi','Insecta','Mammalia','Mollusca','Plantae','Reptilia'}
 
#### Solution Approach:
+ The code for training and testing are in `Part-A.ipynb`.
+ `buildModel` function creates the CNN required for training.
+ `filter_size_needed` is the filter size in layer 1. `filter_scale`is the value that scales filter size on certain amount on each layer.
+ `num_filters` is the number of filters on each layer
+ There are seperate train and test functions and their wandb sweeps. 

The best model was saved and can be downloaded from [this gdrive link.](https://drive.google.com/file/d/15hSvIsqYwkZE1llSabJs0sscBEOjNCfj/view?usp=sharing)

## Part-B:
#### Solution Approach:
+ `buildModel` freezes the base model and adds 2 CNN layers on top chopped base model.
+ `train` function takes care on finetunning.

## Part-C:
#### Solution Approach:
+ This part focusses on taking pretrained network `YOLO` and using it as it is to ADAS object detection.
+ The youtube video of the working model can be found at [this link.](https://youtu.be/JPtj53raETc)
