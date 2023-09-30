# Behaviour_Cloning_Carla

This project tells you how to do make your Carla actors behaviour clone your movements exactly the way you would react to certain conditions by making the model learn from your actions using a convolution neural network.

It is supervised learning based and we are providing the model with our own collected dataset, in which we are collecting the images from our 1920 x 1080 camera added on the ego's roof and recording the vehicle throttle, steering angle and vehicle braking.

The dataset is of 90GB after max compression so we are not going to add that in the repo. but we are providing you the code using which you can collect your own data using the Carla Simulator.  


# Collection of dataset

The files datacollection1.ipynb and datacollection2.ipynb can be used to collect your own data.

Just remember to change your location where you want the data to be collected . Keep in mind to run the last cell only when you have ran it for a large time because the cell will destroy all the actors and save the data in your dedicated location in .csv format.

We have collected data for 35000 images with their values. 

# Training the Model for Steering angle,vehicle throttle input and vehicle braking input cloning

We first visualize the dataset and then we divide the dataset in a set of bins and samples.Then we find the average of the number of samples per bin. As seen we need to drop some of the data as the model would underfit if we were going to train the model on the original dataset.


After dropping the data we are going for random augmentation of the dataset where we are going to change the brightness and also flip the images randomly.


In the end we are going to split the data into a ratio of 80:20 and then train our CNN model for all the different parameters.In the end we are going to save the model and model weights. 


* Braking.ipynb 


* steering.ipynb


* throttletrain.ipynb

# Using the trained models to run your actors autonomously cloning your behaviour in Carla

We have added the code for driving the car autonomously. If you enter any thing from the keyboard when it's driving autonomously the car's autonomous mode will stop.


* drive.ipynb 











