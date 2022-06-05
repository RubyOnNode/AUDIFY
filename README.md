# AUDIFY
Problem Statement
Churning in the mobile application industry is one of the major challenges. We say a customer is
churned when he or she has stopped using the services or buying the products of a firm, in our case
a customer is churned when the user uninstalls the Audify application.
We need to do the analysis of the data that was collected from Firebase - Google Analytics. Find out
the behavior of the users who are uninstalling the app. What factors or features are affecting the
churning behavior of the users and how likely ( probability ) users are going to uninstall the app who
have not yet uninstalled.

Brief overview of solution approach
● We will be using pyspark with hadoop for loading the data as we are dealing with big data. As
we have multiple entries of a single user id, we will group them by user id and sum up all the
features ( underlying assumptions, please find them at the bottom of the report )
● Splitting of data in terms of old users and new users and building separate models for both
for better decision making and analysis.
● Feature engineering, We have 56 total event columns, all these events will be clubbed
together which shows similarity
● A global test set for ( users who have not yet churned ) of 1 lakh users for accessing the
model when run in real time.
● Train Test split of the data points for training and testing of the models that we are going to
impliment.
● SMOTE with undersampling for unbalanced class problem
● Grid search for hyperparameter tuning.
● Confusion matrix and ROC curves for evaluating the accuracy of models ( Logistic
Regression, KNN classifier and Xgboost )
