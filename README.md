# Melanoma-CNN-Prediction



## Problem Statement
To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution which can evaluate images and alert the dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

<!-- You can include any other section that is pertinent to your problem -->

## General Information
The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant. 

The data set contains the following diseases:

1. Actinic keratosis
2. Basal cell carcinoma
3. Dermatofibroma
4. Melanoma
5. Nevus
6. Pigmented benign keratosis
7. Seborrheic keratosis
8. Squamous cell carcinoma
9. Vascular lesion

## NOTE: 

* You don't have to use any pre-trained model using Transfer learning. All the model building processes should be based on a custom model.
* Some of the elements introduced in the assignment are new, but proper steps have been taken to ensure smooth learning. You must learn from the base code provided and implement the same for your problem statement.
* The model training may take time to train as you will be working with large epochs. It is advised to use GPU runtime in Google Colab.

## Project Pipeline

* Data Reading/Data Understanding → Defining the path for train and test images
* Dataset Creation→ Create train & validation dataset from the train directory with a batch size of 32. Also, make sure you resize your images to 180*180.
* Dataset visualisation → Create a code to visualize one instance of all the nine classes present in the dataset
* Model Building & training : 
  * Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1).
  * Choose an appropriate optimiser and loss function for model training
  * Train the model for ~20 epochs
  * Write your findings after the model fit, see if there is evidence of model overfit or underfit
* Choose an appropriate data augmentation strategy to resolve underfitting/overfitting 
* Model Building & training on the augmented data :
  * Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1).
  * Choose an appropriate optimiser and loss function for model training
  * Train the model for ~20 epochs
  * Write your findings after the model fit, see if the earlier issue is resolved or not? 
**Class distribution:** Examine the current class distribution in the training dataset
  * Which class has the least number of samples?
  * Which classes dominate the data in terms of the proportionate number of samples? 
**Handling class imbalances:** Rectify class imbalances present in the training dataset with Augmentor library. 
* Model Building & training on the rectified class imbalance data:
  * Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1).
  * Choose an appropriate optimiser and loss function for model training
  * Train the model for ~30 epochs
  * Write your findings after the model fit, see if the issues are resolved or not?

## Conclusions
The below are the observations for the given data set.

> Model 1: Initially we tried without any data augmentation , dropouts and the model is clearly Overfitting.

> Model 2: After adding Augumentation and Dropouts model overfitting issue is solved but model accuracy is reduced. To overcome this data augumentation and batch Normalization and l2 regularization is added.

> Model 3: After Data Augumentor, Normalization and l2 regularization and extra layer model accuracy is improved and model underfitting issue also solved.

## Contact
Created by Ashish Kumar Singh[@ashish0688] - feel free to contact me!
