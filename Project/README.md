## Environment


The given script is for google colab and will have to be changed to run on a local machine.

## Setup

For qa_testing:

Make sure the following file/dir paths are adjusted according to file locations.


file- augmented_dev.json (augmented dev set)

dir- bert-base-uncased and distilbert-base uncased (models and predictions are stored in these directories)

Currently the main directory where all files and sub-directories are stored is

`
file_dir = '/content/drive/My Drive/nlp_dataset/'
`

## Running the script

Just run the cells for all the colab files to get the associated results.

There are 3 different files:

1. qa_testing: This is the main file which is used to calculate the f1 and em score for both original dev set and augmented dev set using pre-trained bert and distil-bert models.

2. qa_type_analysis: This file is used to perform data analysis on the questions present in the SQAUD V2.0 train and dev set.

3. Data_Augmentation: This file is used to generate the augmented dev set.
