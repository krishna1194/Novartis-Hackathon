# Novartis Data Science Challenge-Hackathon

### Problem Statement
This is a data science competition to identify by detecting an attack is actually going to take place on their system or not. It's a classification use case.

### My approach to the given problem:
In this problem, I clearly understood that more than Accuracy we have to select a model that provides less False Negative (FN) because not detecting an Attack that is actually going to take place is much costlier than falsely detecting that an attack will take place where the attack is not going to take place.

Preprocessing steps:

    1. Impute the Missing Data
    2. Create Day, Month and Year as individual features
    3. Checking Multicollinearity and handling it
    4. Removing the unwanted features
    5. Standardizing the data

Post this I split the data into Train and Valid dataset(70-30 Split). I've used seven different models on the Train dataset to determine the best model to use on the Test dataset. I perform Cross-Validation on different models and calculate accuracy and standard deviation to understand how the model has performed. I even check the confusion matrix to check how good a model has performed and then check the value of False Negative. After checking I select the model that I'll be using on Test dataset to predict the MULTIPLE_OFFENSE.

For this Dataset GradientBoostingClassifier has performed very well with only One False Negative and the recall score is also best for this method.

At last, I performed preprocessing on the test dataset (as mentioned above) and used GradientBoostingClassifier to predict the Response(MULTIPLE_OFFENSE)
