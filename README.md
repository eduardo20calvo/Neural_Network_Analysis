# Neural Network Analysis

The purpose of this analysis is to create a binary classifier model, using a deep neural network, that will predict whether an applicant will become successful using the features from a dataset of 34,000 organizations. The steps of this analysis includes preparing the data for use on a neural network model, compiling/evaluating a binary classification model using a neural network and optimizing the neural network model. The tools/libraries used include Pandas, Tensorflow and Scikit-learn. The main programming language used is Python.

## Prepare the Data to be used on a Neural Network Model

The CSV file was read and organized into the DataFrame to display all of its rows and columns. The "EIN" and "NAME" columnns were dropped as they are not relevant to the binary classification model. "OneHotEncoder" was used to encode the dataset's categorical variables as these datatypes can't be fit into the neural network model as object types. These encoded variables were then organized into a DataFrame. Then the original DataFrame's numerical variables were concatenated to the encoded DataFrame. 

X and Y variriables were defined with X attributing to all the features of each of the organizations in the dataset and Y attributing to the target column that determines whether each organization is succesful or not. The feature and target sets were split into training and testing datasets. Using scikit-learn's "Standard Scaler" the features data was scaled to prevent discrepencies when fitting the data into the neural network model.

## Compile and Evaluate a Binary Classification Model using a Neural Network

The deep neural network was created by assigning the number of input features, the number of layers, and the number of neurons on each layer using Tensorflow's Keras. For this example, about 116 features were used for the model. One output layer was defined. Two hidden layers were also defined with each having 15 and 10 nodes respectively, along with the "relu" activation function.

With all the characteristics of the model defined, the neural network model instance was called as Sequential(). The first hidden, second hidden, and output layer were added to the instance. Along with these additions, an activation function was added. The activation function used for this layer is "sigmoid". Last but not least, the Sequential model was compiled using the binary_crossentropy loss function, the adam optimizer, and the accuracy evaluation metric. The training data was then fitted into the model using 50 epochs.

The model loss and accuracy metrics were evaluated for this model. The results show that the model had a loss of 56% and an accuracy of 73%.

## Optimize the Neural Network Model

Two more models were defined for the attempt to optimize the original model. For the first optimized model, the number of neurons in each layer were increased. The first hidden layer contained 30 nodes and the second hidden layer contained 20 nodes. Keeping all other variables constant, the model produced a loss of 56% and an accuracy of 73%.

For the second optimized model, an extra hidden layer was added. The first hidden layer was brought back to 15 nodes and the second hidden layer to 10 nodes. The third hidden layer was given 5 nodes. Keeping all other variables constant, the model produced a loss of 55% and an accuracy of 73%. See below for a summary of the results:

![Screenshot 2022-12-17 140419](https://user-images.githubusercontent.com/104874384/208258428-4fa20f2e-a0ed-40f6-8670-bb989f1d2ed6.png)

Based on the results above, all models had similar loss metrics and the same accuracy. We can conclude that the change of characteristics did not effectively optimize the last two models to their potential. 
