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
- The column IS_SUCCESSFUL contains binary data refering to weither or not the charity donation was used effectively. This variable is then considered as the target for our deep learning neural network.
- The following columns APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT are the features for our model.
- Encoding of the categorical variables, spliting into training and testing datasets and standardization have been applied to the features.
 
 
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



