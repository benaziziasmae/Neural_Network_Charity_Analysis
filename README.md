# Neural_Network_Charity_Analysis

## Overview of the project

The purpose of this project is to use deep-learning neural networks with the TensorFlow platform in Python, to analyze and classify the success of charitable donations.
We use the following methods for the analysis:

- Preprocessing the data for the neural network model,
- Compile, train and evaluate the model,
- Optimize the model.

Within this dataset are a number of columns that capture metadata about each organization, such as the following:

- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special consideration for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

## Resources
- Data source : [charity_data](/Resources/charity_data.csv)
- Software :Python , Anaconda Navigator, Conda, Jupyter Notebook.

## Summary and Results 

 ### Deliverable 1: Preprocessing Data for a Neural Network Model
  
- First action we did is to drop the columns EIN and NAME as they are identification information .
- The columns with more than 10 unique values have been grouped together 
- The categorical variables have been encoded using one-hot encoding 
- The preprocessed data is split into features and target arrays 
- The preprocessed data is split into training and testing datasets 
- The numerical values have been standardized using the StandardScaler() module 
 
![Capture1](/Resources/Capture1.PNG)

 ### Deliverable 2: Compiling, Training, and Evaluating the Model
 
The neural network model using Tensorflow Keras contains working code that performs the following steps:
- The number of layers, the number of neurons per layer, and activation function are defined
- An output layer with an activation function is created
- There is an output for the structure of the model
- There is an output of the model’s loss and accuracy
- The model's weights are saved every 5 epochs

### Deliverable 3: Optimizing the Model

The model is optimized, and the predictive accuracy is increased to over 75%, or there is working code that makes three attempts to increase model performance using the following steps:
- Noisy variables are removed from features 
- Additional neurons are added to hidden layers 
- Additional hidden layers are added 
- The activation function of hidden layers or output layers is changed for optimization
- The model's weights are saved every 5 epochs 

## Summary 

*Data Preprocessing*

- The column IS_SUCCESSFUL contains binary data refering to weither or not the charity donation was used effectively. This variable is then considered as the target for our deep learning neural network.
- The following columns are the features for our model:
-  APPLICATION_TYPE, 
-  AFFILIATION, CLASSIFICATION, 
-  USE_CASE, 
-  ORGANIZATION, STATUS, 
-  INCOME_AMT, 
-  SPECIAL_CONSIDERATIONS, 
-  ASK_AMT.

- Encoding of the categorical variables, spliting into training and testing datasets and standardization have been applied to the features.


*Compiling, Training, and Evaluating the Model*

This deep-learning neural network model is made of two hidden layers:
- with hidden_nodes_layer1 =80
- hidden_nodes_layer2 30 neurons
- The input data has 43 features and 25,724 samples. 
- The output layer is made of a unique neuron as it is a binary classification. To speed up the training process, we are using the activation function ReLU for the hidden layers. As our output is a binary classification, Sigmoid is used on the output layer.


- For the compilation, the optimizer is adam and the loss function is binary_crossentropy. The model accuracy is under 75%. In other words This model acheived 63.8% accuracy with several attempts to incraese the accuracy including:
- Increasing the number of hidden nodes in layer 1 (3 X number of input features)
- Increasing the number of hidden layers to include a 3rd
- Changing the activation functions: tried linear, tanh, sigmoid for a combination of hidden layers and output layer.

## Conclusion 

This is not a satisfying performance to help predict the outcome of the charity donations as the deep learning neural network model did not reach the target of 75% accuracy.
To increase the performance of the model, we applied bucketing to the feature ASK_AMT and organized the different values by intervals. We increased the number of neurons on one of the hidden layers, then we used a model with three hidden layers. We also tried a different activation function (tanh) but none of these steps helped improve the model's performance.

Since we are in a binary classification situation, we could use a supervised machine learning model such as the Random Forest Classifier to combine a multitude of decision trees to generate a classified output and evaluate its performance against our deep learning model.
