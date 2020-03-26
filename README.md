# Detecting penumonia from X-ray images using Deep Learning

## Introduction
Pneumonia is an infection of the lungs with a range of possible causes. It can be a serious and life-threatening disease. It normally starts with a bacterial, viral, or fungal infection.

![Pneumonia](https://i.imgur.com/jZqpV51.png)

## Dataset 
This dataset is avilable on Kaggle. The motivation for me here was to implement Transfer Learning. 
Dataset source: https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia

The dataset is organized into 3 folders (train, test, val) and contains subfolders for each image category (Pneumonia/Normal). There are 5,863 X-Ray images (JPEG) and 2 categories (Pneumonia/Normal).

- The kaggle's data have split into 3 folders : train, val and test.
- The train folder have 5216 samples (NORMAL:1341，PNEUMONIA:3875).
- The val folder have 16 samples (NORMAL:8，PNEUMONIA:8).
- The test folder have 624 samples (NORMAL:234，PNEUMONIA:390).

*The valiadation set is only 16 samples which is not enough to fine-tune our model's hyperparameters*

## Model  
- We are using the **VGG16** model from the Keras.Applications library as the base model.
- We trained the whole network for 20 epochs
- Optimizer : RMSPROP 
- Data Augmentation : The goal is to get rid of the class imbalance issues. Oversampling with data augmentation 
- Dropout

final accuracy : 81.25%
