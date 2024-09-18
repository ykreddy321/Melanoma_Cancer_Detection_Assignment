# Project Name

To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

# Table of Contents

## General Information 
The dataset consists of 2239 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

	The data set contains the following diseases:

	Actinic keratosis
	Basal cell carcinoma
	Dermatofibroma
	Melanoma
	Nevus
	Pigmented benign keratosis
	Seborrheic keratosis
	Squamous cell carcinoma
	Vascular lesion
	
To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

Data loaded in Google drive location: https://drive.google.com/drive/folders/1sNLX2TO5b0_K0ACI8YU2C9VwgnSz34qP

## Data Analysis:

 Bar Plot (Each class vs No. of images)
  - 'seborrheic keratosis' class has the least number of samples.
  - 'pigmented benign keratosis' class dominates with the highest propotionate of samples.
  
## CNN Architecture Design:

	To identify the melanoma skin cancer using skin lesions images. To achieve the higher accuracy and results on the classification task, We have built different variation of custom CNN model to get the highest acuracy.
	
		
	1. Rescaling Layer - To rescale an input in the [0, 255] range to be in the [0, 1] range.
	2. Convolutional Layer - Convolutional layers apply a convolution operation to the input, passing the result to the next layer. A
 	convolution converts all the pixels in its receptive field into a single value.
	3. Pooling Layer - Pooling layers are used to reduce the dimensions of the feature maps. Thus, it reduces the number of parameters to learn and the amount of computation performed in the network. The pooling layer summarises the features present in a region of the feature map generated by a convolution layer.
	4. Dropout Layer - The Dropout layer randomly sets input units to 0 with a frequency of rate at each step during training time, which helps prevent overfitting.
	5. Flatten Layer - Flattening is converting the data into a 1-dimensional array for inputting it to the next layer. We flatten the output of the convolutional layers to create a single long feature vector. And it is connected to the final classification model, which is called a fully-connected layer.
	6. Dense Layer - The dense layer is a neural network layer that is connected deeply, which means each neuron in the dense layer receives input from all neurons of its previous layer.
	7. Activation Function(ReLU) - The rectified linear activation function or ReLU for short is a piecewise linear function that will output the input directly if it is positive, otherwise, it will output zero.The rectified linear activation function overcomes the vanishing gradient problem, allowing models to learn faster and perform better.
	8. Activation Function(Softmax) - The softmax function is used as the activation function in the output layer of neural network models that predict a multinomial probability distribution. The main advantage of using Softmax is the output probabilities range. The range will 0 to 1, and the sum of all the probabilities will be equal to one.
	9. Added the augumentation images created from the actual images. This will add additional train data to the model and will increase the accuracy.

	
## Conclusions

	1.  Simple Sequential CNN Model: We got the very less validation accuracy and high loss function model.It is overfitting the model.
	2.  Second Model with dropouts and Data augumentation improved accuracy and decreasing loss function.
	3.  Third Model including Class Imbalance Logic improved accuracy. This rebalance using the Augementor Module balances the each classes by addig the    more sample images 500 for each classes. we can see the accuracy is 95% and 82% acuracy for train and validation set respectively. 
	4. We used above model for the prediction and due to memory issues we could not get time to run this step, but based on validation data the accuracy is 82% and loss function also reduced from 2.684 to 1.07

	Accuracy & Loss Analytics for different Model :

	Simple Sequential model:
	accuracy: 0.9074 - loss: 0.2540 - val_accuracy: 0.5123 - val_loss: 2.6854

	Drop Outs and Data Augumentation:
	accuracy: 0.5539 - loss: 1.2543 - val_accuracy: 0.5302 - val_loss: 1.3136

	Class Imbalance with Augumentor:
	Epoch 50/50 - accuracy: 0.9532 - loss: 0.1100 - val_accuracy: 0.8203 - val_loss: 1.0711

## Technologies Used
		Python (Version 3.11.7)
		Numpy  (Version 1.26.4)
		Pandas (Version 2.1.4)
		Matplotlib (Version  3.8.0)
		Seaborn (version 0.13.2)
		Tensorflow (version 2.17.0)
		Augmentor  (version 0.2.12)

## Acknowledgements
	 This project is created based on the trainings provided by UpGrad Team.

## Contact

Created by Kushalava Reddy Yanala [@ykreddy321] - feel free to contact me!