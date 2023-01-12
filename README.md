# predict-center-mouse-location-neural network
neural network model to predict the mouse location


### Project Description
The main idea of this project is to predict the dependent variable (coordinates of the middle
point of the box containing the mouse), based on a set of independent variables (coordinates
of 7 joints of the mouse and the coordinates of the 2-point containing box).This is done by
designing an automated model based on an artificial neural network.The training dataset is
generated from the given images by annotations a set of points for each mouse in the images.

### Conclusions

As we all know, deep learning relies on a large amount of data to train the model.Therefore, rotational transformation was used to address the lack of training data, although the data was increased from 67 to 737, but it is not sufficient to generalize a model based on neural networks. The data set was normalized using MinMaxScaler, after that it was divided into the 80% training set and the 30% test set.

Since the data set is small and in order to avoid overfitting problems of the MLP models (number of layers, number of nodes), k-fold cross validation with 10 times and three iterations was used in order to evaluate two multilayer models (MLP) for the multiple output regression task. The activation function was used.ReLU common in hidden layers.The first model contains two hidden layers, the first layer contains 18 nodes and the second layer contains 9 nodes, while the second model contains three hidden layers, the first contains 18 nodes, the second contains 9 and the third contains 4.Use the mean squared error (MSE) for the fit of these models because it is based on L2 loss and the Adams version of Stochastic Gradient Origin.
  
The first model is the best, because the mean is $0.000151$, and the standard deviation is $0.000048$ for the MSE which is much lower than the other model.

And after our proper selection of the model, it is trained on the available training data set and evaluated on the test data set, the model is trained with mse loss, epoch 300, adam optimizer.We conclude that the training phase was rather good. The model was evaluated using the test data set, where the model achieved a mean square error (MSE) of $9.742738257045858e-06$.





