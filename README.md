# Waste Segregation for Improving Waste Management

## Objective
The aim of this endeavor is to develop a sophisticated waste segregation framework leveraging convolutional neural networks (CNNs) to effectively differentiate and classify waste into discrete categories. This initiative aspires to bolster recycling efficacy, mitigate ecological degradation, and foster environmentally sustainable waste management protocols.

## The key goals are:

* Precisely categorising waste materials into distinct classifications such as cardboard, glass, paper, and plastic. 
* Enhancing the efficiency of waste segregation to facilitate recycling processes and curtail landfill contributions. 
* Gaining deeper insights into the characteristics of various waste materials to refine sorting strategies and advance sustainability efforts.

## Data Description
* The dataset is organized into several folders, each corresponding to a specific category, such as Cardboard, Food_Waste, and Metal. • Each folder contains images of objects that fall within its respective classification.
* However, the items within these folders are not further distinguished into subcategories. For example, the Food_Waste folder may include images of items like coffee grounds, teabags, and fruit peels, but these are not explicitly labeled as coffee grounds or teabags.However, these items are not further subcategorised.

## Table of Contents
* [Data Understanding](#data-understanding)
* [Data Preparation](#data-preparation)
* [Model Building and Evaluation](#model-building)
* [Data Augmentation](#data-augmentation)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)


## Data Understanding
- The dataset comprises images grouped into seven distinct categories: Cardboard, Food_Waste, Glass, Metal, Paper, Plastic, and Other.
- Each category is encapsulated within a folder, containing images of objects specific to that classification.
- We load and unzip data
  
## Data Preparation
- Loading and pre-processing the images
- Training and Testing directories
- Visualise sample images for better understanding
- Encoding different classes
- Creating validation and final training sets
  
## Model Building and Evaluation
- Normal model building with 3 CNN layers
- Model Training
- Testing model on the test set
- Build models using transfer learning (with VGG16 and ResNet50V2). Then training and evaluation on the test set

## Data Augmentation
- Create a Data Augmentation Pipeline
- Train and Evaluate the model on the new augmented dataset
  
## Conclusions (Major)
- The normal convolution model does not give accuracy on test set better than 64%
- The transformation technique with base model as VGG16 provides much better test data accuracy of 76%
- We get even better test data accuracy of 84% with base model as ResNet50V2
- Also, loss in test data set; normal CNN model > base model as VGG16 > base model as ResNet50V2

    
## Acknowledgements

- This project is by UpGrad & IIIT-B


## Contact
Created by [Sumegh Singh Chouhan]
