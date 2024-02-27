# deep-learning-challenge

## Alphabet Soup Charity Analysis Report

### Overview of the Analysis
-------------------------------
The purpose of this analysis was to create a tool to help Alphabet Soup determine whether potential applicants for funding would be successful in their ventures or not. This would be accomplished by creating a model that would analyze information on previous applicants, including whether they were considered successful, in order to see how well the model could predict the chances of success for future applicants.

### Results
-------------------------------
* Data Preprocessing
    * Target Variables: IS_SUCCESSFUL column (whether the money was used effectively)
    * Feature Variables: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME<AMT, SPECIAL_CONSIDERATIONS, ASK_AMT columns
    * Removed Variables: EIN and NAME columns
* Compiling, Training, and Evaluating the Model
    * I selected three layers, with 60, 30, and 1 neuron(s) respectively. An initial layer with 60 neurons and an activation function of relu. A second layer with 30 neurons again using relu. And a final output layer with 1 neuron that used a sigmoid function.
    * I was not able to acheive the target model performance with this model.
    * I took multiple steps to increase the model performance, including using keras tuner and hyperband to search for the best hyperparameters. I also used a random forest classifier model and learned which columns were the least important in that model. I then removed those columns from the training and testing datasets. Then I added more neuron layers and neurons to the model while adjusting the number of epochs.

### Summary
-------------------------------
The overall results of the deep learning model did not reach the target model performance. Although removing three columns, adding additional layers and neurons, and reducing the number of epochs to fifty, improved the dataset; it was only by about .3%. Further modification of the model would be needed to increase the accuracy. Perhaps, removing more columns or trying a different activation function might help the model reach target performance.

### Sources
-------------------------------
* Used https://re-thought.com/pandas-value_counts/ as resource for referencing items with a value count in a certain range with ".loc[lambda x : x<500]" and ".loc[lambda x : x>1]"
* Used https://stackoverflow.com/questions/35523635/extract-values-in-pandas-value-counts as a resource for creating a list out of the indexes of a value counts function with ".index.to_list()"
