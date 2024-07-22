# Food-Dishes-Classification

![Type](https://img.shields.io/badge/Type-Personal_Project-yellow)
![Concepts](https://img.shields.io/badge/Concepts-Deep_Learning,_Computer_Vision-blue)
![Language](https://img.shields.io/badge/Language-Python-red)
![Libraries](https://img.shields.io/badge/Libraries-Keras,_Tensorflow,_Scikit_Learn-green)

This repository contains work on Food Dishes Classification from Images, using a truncated version of Food-101 dataset, having only 20 categories, using Keras API of tensorflow in Python.

Dataset - [Food 101](https://www.kaggle.com/dansbecker/food-101/home)
This data was truncated to use 20 categories for the classification. The number of images used in training and testing set, and the labels used can be seen from the following graph -

<img src="/Visualizations/Dataset Distribution.PNG"/>

Team Members - Adarsha Mani, Lavina Chotrani

## Model -

This model is built in such a way that initial layers are that of the VGG-16 Model, pre-trained on imagenet weights. The initial layers are frozen for training, allowing us to fine-tune the later layers for effective feature recognition. The recognized features are then fed to a dense network for classification.

<img src="/Visualizations/model.png" align="center" width="40%"/>

## Training -

The results of training accuracies vs. epochs are shown below. Complete details of architecture and results can be viewed from the [Visualizations](https://github.com/neelabhsinha/Food-Dishes-Classification-using-Deep-Learning/tree/master/Visualizations) folder. 

<img src="/Visualizations/Training Accuracy.PNG" align="center" width="40%"/>

## Results & Conclusions - 

S. No. | Metric | Value |
-------|------|----------|
1 | Accuracy | 52.2% |
2 | Top 5 Accuracy | 82.03% |

- VGG16 model identifies features effectively because of more depth in the architecture, which allows it to identifiy both lower level and higher level features 
- Transfer learning helps us to make the training faster as the initial layers are used to identify local features only, which are same for almost all models. So, freezing the initial layers allows us to speed-up the training remarkably
- Features like dropout, regularization, etc. allows us to make the model more robust

## Steps to execute the code in this reposirory:

1. Install Anaconda Distribution and all relevant libraries

2. Prepare the dataset

3. Open up the terminal and type -

``` cmd
$git clone https://github.com/neelabhsinha/Food-Dishes-Classification-using-Deep-Learning.git
$cd Food-Dishes-Classification-using-Deep-Learning
$jupyter notebook
```
