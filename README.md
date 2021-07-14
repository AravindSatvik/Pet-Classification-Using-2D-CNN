# Pet-Classification-Using-2D-CNN
The main idea of this project is to classify whether the image is a dog or a cat. The dataset is collected from [kaggle](https://www.kaggle.com/c/dogs-vs-cats/data). The dataset contains a total of 25,000 images out of which 20,000 images were used for training the model and 5,000 images were used for validation. 

* First, the dataframe is split to training and validation dataframes. Then some transformations are applied on the images of training set. The reason why we want to apply some transformations on the training set is to avoid overfitting. If we dont apply these transformations on the training set, we will get a huge difference between the training set accuracy and test set accuracy. This process is called IMAGE AUGMENTATION. We do these transformations so that the model does not over learn or over train on the existing images.
(Note: Do not apply any transformations on the validation dataset)
* Then the model is trained using two-dimensional convolutional neural networks. Tensorflow and Keras libraries were used to train the model. 17 layers were used to build the CNN model.
* The model is trained for 10 epochs and finally, we have obtained a validation accuracy of 90.37% at the end of 10th epoch.
* The model weights are then stored in .h5 file.
* For predicting single images, first the image is converted to array format which contains pixel values. Then the image is resized to 128*128 size and feature scaling is applied for all the pixels. predict_classes method is used to predict the class of image. If 0 is obtained, then it is a cat and if 1 is obtained, then it is a dog.
