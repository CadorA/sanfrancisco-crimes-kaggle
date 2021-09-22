# San Francisco Crime Classification

This repository contains the notebook which I used to attend the related Kaggle competition. The train dataset contains few features ('Date', 'DayOfWeek', 'PdDistrict','Address', 'X', 'Y) and a significant number of examples (878000 registered charges). The test dataset contains roughly the same number of rows (850000).

In simple words, the objective is to predict the category of crime that occurred given the time and location.

## Structure
The notebook starts with a short description of the problem.

Afterwards, the Exploratory Data Analysis begins, looking at the given features, plotting useful figures and comparing the value counts for different combinations of features (such as Roadtype-Crime Category).

The models I used are presented below:
1. K-Nearest Neighbours (KNN) Classifier - Simple and good for initial insights.
2. Logistic Regression - Good for gaining some more insights regarding feature importance
3. Ensemble Methods
 - (Bagging) Random Forest Classifier (RFC) - Good option, higher complexity than previous models.
 - (Boosting) LightGBM - Faster to train than RFC, higher accuracy, but more parameters to tune.

For the tuning of the previous models, I used both RandomSearchCV and GridSearchCV (from sklearn).

## Results
This project was more of a playground than a competition. I tried exploring all the above strategies and to compare their benefits and their drawbacks. The dataset was hardly a good starting point because it was sizable enough to create a long training time (on my CPU, trianing 20 RFC with a 5-fold CrossValidation was taking more than 400 minutes). My strategy was far from optimal, I wanted to get some hands-on experience with the algorithms and at the very end I realized the structural mistakes I made at the beggining.

All in all, this was my first ever Kaggle competition. I think I learned some valuable lessons and the next challenges will be on a smaller dataset with better results.

**A detailed article that contains the insights and the explanations of the strategy used can be found on my Medium page: [Link Medium Page - To be updated]**