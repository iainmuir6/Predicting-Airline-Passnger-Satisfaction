<p align="center">
  <img src='https://www.salesforce.org/wp-content/uploads/2021/02/uva-university-of-virginia-logo.png' width=300/>
</p>

# Predicting Airline Passnger Satisfaction

## Business Problem Statement

Recently, the largest U.S. airlines disclosed that the vast majority of their profits are generated by their frequent flyer (i.e. customer loyalty) programs. As such, the biggest priority for each airline is to attract users to their programs, even if it means operating the actual flights at a loss, as they currently do. With such fierce competition among frequent flyer programs, airlines need to figure out how to attract customers to their company over a rival. This is especially critical in the airline industry where customer loyalty and satisfaction is generally low.  

## Business Goal

The goal of our project is to figure out which factors effectively increase or decrease customer satisfaction on flights. By improving on these factors, airlines will be able to deliver more satisfying flight experiences to their customers, giving them a competitive edge over their rivals and attracting customers that are up for grabs to their programs. In addition, by improving the customer experience, airlines can improve their brands and the reputation of flying itself, making the experience seem less of a hassle and attracting more customers to flights in general. Thus, the findings of this project will also help airlines pull new customers into the market as well. Ultimately, the goal of the project is to help airlines attract more customers into their customer loyalty programs by figuring out how to improve their flight experience.  

## Data Profile

The data we used for investigation and analysis was the ‘Airline Passenger Satisfaction’ dataset published in 2020 on Kaggle. It was divided into separate training and testing sets, where the training set has 103,904 records and the testing set has 25,976 records. There are 24 columns in total, including 4 continuous variables, 5 categorical variables, 14 discrete rating variables, and the target variable which has two categories. There are 8,488 records that have missing or N/A values, which were either dropped from the dataset or replaced with median value depending on the column type. Our target attribute are in ones and zeros, where 1 represents satisfied customers and 0 represents neutral or dissatisfied customers. The target attribute is of roughly equal balance with 56.7% being neutral or dissatisfied and 43.3% being satisfied.

## Results

Our best-performing model on our training dataset was a 4-layer Neural Network model, which scored a 94.95% accuracy. However, the best performing model on our test dataset was an XGBoost model with hyperparameters tuned using a cross-validated grid search. This model scored a 67.79% accuracy and a ROC-AUC score of 80.444%. It had a recall score for the positive class of 49.64%, and recall score of 82.0% for the negative class. Based on this model, we found that the most important predictors of customer satisfaction for airlines are passenger class, inflight service, and the arrival delay of a plane in minutes. Airlines should use the findings from our analysis to know what areas of customer satisfaction to focus on.

### Initial Model Results

<p align="center">
  <img src="https://github.com/iainmuir6/Predicting-Airline-Passnger-Satisfaction/blob/main/input/pre_results.png" alt="mnbc" class="center" width="750">
</p>

### Post-Hyperparameter Tuning Model Results

<p align="center">
  <img src="https://github.com/iainmuir6/Predicting-Airline-Passnger-Satisfaction/blob/main/input/post_results.png" alt="mnbc" class="center" width="750">
</p>
