## Environment

The given script is for google colab and will have to be changed to run on a local machine.

All the required packages are present in google colab.

## Setup

Make sure the file paths of the test and the train dataset are in accordance with the drive which is mounted.

The train and test datasets are present and, the output files will be saved in the following directory: 

`
file_dir = '/content/drive/My Drive/nlp_dataset/'
`

These can be changed in the code according to the user setup.

## Running the script
Once the file paths are set run all the cells with ctrl+F9 to get the evaluation results.

Each model will first train and then test the respective model and generate the output with the performance metrics and the output file.

There are 4 different models trained and tested.
1. TF-IDF

2. Glove w2v

3. Universal Sentence Encoder with logistic regression

4. Universal Sentence Encoder with neural network

For the neural network implementation of USE, it is possible to see the training loss and accuracy curves by setting the plot_training argument = True

## How the code executes

For every word embedding technique the respective embedding function is called with the training data as one of the arguments. This function returns the classification model trained on the training sentences. The model is then passed on to the evaluate function which accepts the test data and the classification model as two of its arguments and the output data frame with the sentences, gold label and the predicted label. The data is then stored in an output file.
