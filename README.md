# deep-learning_5class_classification

Problem statement
Ship or vessel detection has a wide range of applications, in the areas of maritime safety, fisheries management, marine pollution, defence and maritime security, protection from piracy, illegal migration, etc.
Keeping this in mind, a Governmental Maritime and Coastguard Agency is planning to deploy a computer vision based automated system to identify ship type only from the images taken by the survey boats. You have been hired as a consultant to build an efficient model for this project.
Dataset Description:
There are 6252 images in train folder. The categories of ships and their corresponding codes in the dataset are as follows -
'Cargo' -> 1
'Military' -> 2
'Carrier' -> 3
'Cruise' -> 4
'Tankers' -> 5

•	The train.zip which have the following structure.
Variable	Definition
image	Name of the image in the dataset (ID column)
category	Ship category code (target column)
•	train.zip contains the images corresponding to both train and test set along with the true labels for train set images in train.csv

Approach:
        The problem given was to identify different types of ships from the pictures. The training set contained around 6252 images across all the ships categories. As the amount of images for training is very less. Hence we will highly depend upon different transformation techniques as well as weights of pre-trained models. Data transformation techniques refer to tweaking of same image using various approaches such as horizontal flipping, random rotation, zooming, lighting, warping, padding etc. to create different versions of same image such that while training at each epoch, our model gets different images as if we have much more images to give the model to learn. After transformation, next step was to fix a particular image size to the whole data set.

Now, we are ready to create CNN model with pre-trained weight from inceptionv3 architectures. 

After the model is created, we are now ready for training. First step is to find the correct learning rate, so that we can quickly train the model. Then, I trained the model for 10 epochs with a learning rate of 0.0001 and got a accuracy for trained model of 95%. On the test, the classification report given a good prediction which classifies different categories of ships with overall 90%.

Model performance was good, we can increase the performance by tweaking learning rate and using different pre-trained  vgg16, Resnet/ densenet architectures.

