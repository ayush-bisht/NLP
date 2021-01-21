## Environment

The given script is for google colab and will have to be changed to run on a local machine.

All the required packages are present in google colab expect pywsd and vaderSentiment

They can be installed as follows:
```
!pip install vaderSentiment
```
```
!pip install -U pywsd
```

## Addition downloads required

nltk using:
```
nltk.download('wordnet')
nltk.download('averaged_perceptron_tagger')
nltk.download('punkt')
```

universal sentence encoder using: 

```
hub.load("https://tfhub.dev/google/universal-sentence-encoder-large/5")
```

## Note

1. Make sure the file paths of the test and the train dataset are in accordance with the drive which is mounted.

Currently the file paths are: 

`
file_path = '/content/drive/My Drive/nlp_dataset/p2_train.csv'
`

`
file_path_test = '/content/drive/My Drive/nlp_dataset/p2_test.csv'
`

The datasets are present in a folder 'nlp_dataset' in the mounted drive

This will have to be changed in accordance with the testing environment.
This can be changed in 'load_data()' function.

## Running the script
Once the file paths are set run all the cells with ctrl+F9 to get the evaluation results.


The function create_train_test_set takes a 'features' argument.
It can have 2 values 'baseline' and 'additional'. 
The baseline features uses POS tags and sentence embeddings.
The additional features uses POS tags, word senses, sentence embeddings and sentiment analysis.


The train and test model functions allows user to set the classifier used for training and testing.
It can have two values 'SVC' and 'NN'. 'SVC' is used for the given dataset as it provides the best result.
NN classifier results can be observed by changing the argument. 
Remember to set the same classifier for train and test functions.


The train function also allows the user to plot the training curves if the classifier is set as 'NN'.
Just set 'plot_training' = True.  
