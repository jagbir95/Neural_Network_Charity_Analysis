# Neural_Network_Charity_Analysis
# Overview of the analysis:
The main purpose of this analysis is to create a binary classifier with the help of machine learning and neural networks for Alphabet Soup foundation to help them predict whether applicants will be successful if funded by them. We have all the data of different organizations that have received funding from Alphabet over the years.
# Results:
### Data preprocessing:
- The column `IS_SUCCESSFUL` is considered to be target variable. it contains binary information whether a charity is successful or failed.
- The column which have been considered as features variable are following: `APPLICATION_TYPE` ,`AFFILIATION`,`CLASSIFICATION`,`USE_CASE`,`ORGANIZATION`,`STATUS`,`INCOME_AMT`,`SPECIAL_CONSIDERATIONS`,`ASK_AMT`.
- Binning is applied on `APPLICATION_TYPE` and `CLASSIFICATION` columns and categorical columns are encoded for train, test and split the features.
- The column names `EIN` and `NAME` have been removed from the data.
### Compiling, Training, and Evaluating the Model
- For this deep-learning model two hidden layers have been used first one with 80 neurons and second with 30 neurons.
- The activation function used in hidden layers is `relu` for higher acuracy of the model. whereas otput layer has a single neuron with `sigmoid` activation function. For the compilation the loss function is `binary_crossentropy` and optimizer is `adam` with metrics `accuracy`.
- After evaluating the model the accuracy is 72 % which is lower than expected acuracy of over 75 percent.
- To increase the model performance additonal columns `STATUS` and `SPECIAL_CONSIDERATIONS` dropped from the features and a third layer is added to the model with 20 neurons and the activation function also changed to `tanh`.Despite all these changes the model performance stayed under 75 percent.
# Summary:
- In conclusion, this deep learning model is not performing well for the predictions because its accuracy stayed under 75%.
- Since this is labeled data we can use supervised machine learning model `Random Forest Classifier` and compare the results with deep learning model.