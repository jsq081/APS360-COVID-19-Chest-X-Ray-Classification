# COVID-19-Chest-X-Ray-Classification

-classify the feature among COVID-19, viral pneumonia and normal chest radiography
-achieved the final test accuracy with 98% with Reference Model

## Contributors 
- Yunyi (Cynthia) Chen
- Yuanzhe (Felix) Deng 
- Siqi (Vicki) Jin 
- Ming (Bes) Liao 


## Data Processing 
- We obtained our data from Kaggle.com, a data modelling and data analysis competition platform that provides the readily available datasets for our project. The   dataset we selected contains labelled chest X-ray radiographs prepared by a research team in collaboration with doctors, where the images are collected from different publicly accessible datasets, published papers, and online resources (https://www.kaggle.com/preetviradiya/covid19-radiography-dataset). 

- The dataset contains 3,616 CXR images of pneumonia caused by COVID-19, 6,012 CXR images of lung opacity, 10,102 CXR images of normal lung, and 1,345 CXR images of ordinary viral pneumonia. However, we decided to exclude the lung opacity class because similar research did not consider the class as a lung-related disease with similar characteristics to COVID-19 infection. 
- To avoid misleading accuracies and errors caused by the unbalanced dataset, we duplicated the images in the viral pneumonia set three times and randomly selected 3616 images from the normal dataset. 
- It is worth noting that we have not applied any data augmentation method to increase the number of images in the viral pneumonia class, because we anticipate that any slight changes in a medical image could lead to significant differences during analysis in clinical settings. Thus, we have three balanced classes of reasonably large numbers of imageswe also resized all images into 224 * 224 pixels to ease the training process on CNN and AlexNet models, except GoogLeNet, which only takes in images in size 299 * 299 pixels. In addition, we randomly separated the dataset into training, validation, and testing sets according to the ratio of 60%, 20%, and 20%. Finally, we converted all three sets of data into their corresponding data loaders for training. 




