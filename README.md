# Machine-Learning-Challenge
Analysis

Model-1 SVM

The first step after reading the data to a dataframe is to decide if all information was imperative to keep for the model. 
I removed fields with a zero or null value assuming it would increase the accuracy of the model, but that decreased the accuracy dramatically.
Next I assigned X and y values for the model to perform split data to get train and test data for the model.
Next step is to scale and normalize the data to create more accurate model that has less gap between data points so they all have acurate weights for the model. Initially, using MinMaxScaler to scale the data with SVM model, the training and testing scores were around 0.85. Chaning to StandardScaler to scale the data resulted better numbers for the scores, Training Data Score: 0.8916650772458516 ,Testing Data Score: 0.8947368421052632.
Finally I used GridSearchCV to tune the model's parameters and changing the grid parameters C and gamma displayed no score improvement.

Model-2 Logistic Regression

For this model, data cleaning and preprocessing steps were the same as SVM model.
Using StandardScaler resulted better scores that MinMaxScaler, so used StandardScaler to scale and normalize the data.
The scores for training and testing data was :Training Data Score: 0.887659736791913, Testing Data Score: 0.8895881006864989.
Using GridSearchCV to tune the model's parameters, and changing C values, and increasing the number of iterations max_iter didn't improve.
The two models SVM and LogisticRegression have little to any significant difference between them for this data, even hyperparameter tuning failed to differentiate any significance between the models.
