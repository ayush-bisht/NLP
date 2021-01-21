README
Each model will first train and then test the respective model and generate the output with the performance metrics and the output file.
Running one model at a time:
1. TF-IDF: Uncomment code from line 226-234
2. Glove w2v: Uncomment code from 236-246
3. Universal Sentence Encoder with logistic regression: Uncomment code from 248-258
4. Universal Sentence Encoder with neural network: Uncomment code from 260-270
For the neural network implementation of USE, it is possible to see the training loss and accuracy curves by setting the plot_training argument = True
IMPORTANT NOTE: the file path names have been defined according to a windows operating system. If testing in a linux environment all the file paths will have to be changed e.g.
File_path = “\\testing_output_tfidf.csv” will have to be changed to “/testing_output_tfidf.csv”.
File paths at line: 221-224, 238, 250, 262
Compilation: Just run the python code after commenting/uncommenting the appropriate code lines. No additional arguments are required. Need to make sure that all the associated files are in the folders as submitted.
To run the python file simply run the command “python3 sentiment_analysis.py” from the command prompt or run the file through an IDE.
HOW CODE EXECUTES:
For every word embedding technique the respective embedding function is called with the training data as one of the arguments. This function returns the classification model trained on the training sentences. The model is then passed on to the evaluate function which accepts the test data and the classification model as two of its arguments and the output data frame with the sentences, gold label and the predicted label. The data is then stored in an output file.
NOTE: The output files are included in the submission. They will be overwritten when the model is retrained and tested on.
NOTE: Every model is commented in the original submitted python file