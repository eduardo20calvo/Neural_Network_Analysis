# Neural Network Analysis

The purpose of this analysis is to create a binary classifier model, using a deep neural network, that will predict whether an applicant will become successful using the features from a dataset of 34,000 organizations. The steps of this analysis includes preparing the data for use on a neural network model, compiling/evaluating a binary classification model using a neural network and optimizing the neural network model. The tools/libraries used include Pandas, Tensorflow and Scikit-learn. The main programming language used is Python.

## Prepare the Data to be used on a Neural Network Model

The CSV file was read and organized into the DataFrame to display all of its rows and columns. The "EIN" and "NAME" columnns were dropped as they are not relevant to the binary classification model. "OneHotEncoder" was used to encode the dataset's categorical variables as these datatypes can't be fit into the neural network model as object types. These encoded variables were then organized into a DataFrame. Then the original DataFrame's numerical variables were concatenated to the encoded DataFrame. 

X and Y variriables were defined with X attributing to all the features of each of the organizations in the dataset and Y attributing to the target column that determines whether each organization is succesful or not. The feature and target sets were split into training and testing datasets. Using scikit-learn's "Standard Scaler" the features data was scaled to prevent discrepencies when fitting the data into the neural network model.

## Compile and Evaluate a Binary Classification Model using a Neural Network

The deep neural network was created by assigning the number of input features, the number of layers, and the number of neurons on each layer using Tensorflow's Keras.
