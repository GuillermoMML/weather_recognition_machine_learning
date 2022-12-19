# Weather Recognition Machine Learning ⛅

## Introduction
In this project, we will study several aspects of machine learning. This neural network can recognize different types of weather conditions, such as **dew, fog, smog, rain, etc...** 

Our motivation to have selected this dataset is that many devices and vehicles are capable of recognizing their environment, depending on their environment they behave in one way or another, so knowing the weather conditions can be very useful in specific cases.

## Datasets 📁
All images used for the **training set** and for the **validation set**, have been extracted from this dataset: https://www.kaggle.com/datasets/jehanbhathena/weather-dataset <br>
We modified the dataset mentioned above to have extact **120 images** for each class

## Data Augmentation
We implemented a function, which uses previous trained images from the used dataset, in order to obtain new rotated, zoomed or flipped images.
In order to do this, we imported ```ImageDataGenerator, img_to_array, load_img``` from ```tensorflow.keras.preprocessing.image```

## Efficiency Table Without Data Augmentation
Number Of Layers|Number Of Neurons Per Layer|Activation Function|DropOut|Accuracy|
|:---|:---|:---|:---|:---|
|5| 16, 32, 64, 128, 7| relu, softmax|0.25, 0.25, 0.5|0.5143|
|7| 32, 64, 128, 256, 20, 256, 7| relu, softmax|0.20, 0.25, 0.30, 0.35, 0.5|0.5000|
|7| 32, 64, 128, 256, 20, 256, 7| relu, softmax|0.20, 0.25, 0.30, 0.35, 0.5|0.5571|

## Efficiency Table With Data Augmentation
Number Of Layers|Number Of Neurons Per Layer|Activation Function|DropOut|Accuracy|
|:---|:---|:---|:---|:---|
|6| 64, 64, 64, 64, 256, 7| relu, softmax|0.10, 0.10, 0.10, 0.10|0.7861|
|6| 64, 128, 128, 128, 256, 7| relu, softmax|0.25, 0.25, 0.25, 0.30|0.8208|
|6| 64, 64, 64, 64, 256, 7| relu, softmax|0.25, 0.25, 0.25, 0.30|0.8266|
|6| 128, 64, 128, 64, 256, 7| relu, softmax|0.25, 0.25, 0.50, 0.50|0.8862|
|5| 128, 128, 128, 256, 7| relu, softmax|0.50, 0.50, 0.50, 0.50|0.9712|

## Conclusion
We can clearly observe, that the **accuracy** is much higher when we implement the **Data Augmentation** class. 
<br>
Without Data Augmentation, we reached an accuracy of roughly **55%-60%**, and while using Data Augmentation, we reached after several tests, **98%-99%** accuracy
Observing the Graph we can also add that our **lost_value** decreases significantly, while your training and validation tests reach a high/stable level.


Model Accuracy | Confusion Matrix
:-------------------------:|:-------------------------:
<img src="https://cdn.discordapp.com/attachments/895966492410118194/1054012044178882560/image.png" width="600" height="300" />  |  <img src="https://cdn.discordapp.com/attachments/895966492410118194/1054012081889873960/image.png" width="600" height="300" />

## Distributors ✍️
* **Louka Vanhoucke** [@LuksFlukss](https://github.com/LuksFlukss)
* **Guillermo Marión Lopez** [@GuillermoMML](https://github.com/GuillermoMML)

* Main Code => [@CayetanoGuerra](https://cayetanoguerra.github.io/ia/)
