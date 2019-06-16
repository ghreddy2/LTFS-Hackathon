# LTFS-Hackathon

### Problem Statement
  Afinancial institution wants to predict the probability of a customer(loan borrower) defaulting on a vehicle loan in the first EMI(Equated Monthly Installments) on the due date.
  
### Analytical Statement
  With the available data we will ensure that the clients capable of repayment are not rejected and finding the important features to minimize the default rates.
  
### Data description
  The given data can be considered as three parts:
   - Loanee Information (Demographic data like age, income, Identity proof etc.)
   - Loan Information (Disbursal details, amount, EMI, loan to value ratio etc.)
   - Bureau data & history (Bureau score, number of active accounts, the status of other loans, credit history etc.)
   
 ### Expected output  
 We were asked to find the area under ROC curve between the predicted probability and the observed target.

#### Code
I imported the data using the pandas package to load our excel file.pandas helps us by allowing the data manipulation functions with the numpy record arrays.

 The dataset consists about 3,45,000 rows and 41 features.
 
 We have seperated the numerical and the categorical variables, tried to find the correlation between the numerical features using the heatmap from the seaborn package.
 
 Feature engineering is done on the categorical variables, the date of birth and date of disbursal are made use with the help of datetime package.
 
 When checked for the missing values, we observed missing values in the employment type which are replaced with mode imputation.
 
Some insights observed in the data analysis part are:
  - Self-employed customers are more likely to take the loan when compared with salaried customers. They are also the customers who are in maximum number of defaulters.
  - The customers when compared on the Aadhar flag and the loan default, the defaulters are lesser than the non-defaulters.
  - The defaulters in the train data are utmost 30% when compared to the non-defaulters.
  
### Model building
The data is split in a manner such that 70% is for train and the 30% is for test.

When we tried to fit the Decision-Tree classifier on the initial numerical data, we got an accuracy of 67% but cohen-kappa score is not good.

When probabilities are caluclated for the test-train split in the train data, we have achieved 53% of the area under the curve.

When a RandomForestClassifier is fit on the data with the help of AdaboostClassifier, BaggingClassifier, GradientBoostClassifier and the RandomForestClasifier, by dropping some of the low performance attributes, a bagging classifier gave an accuracy of 79% but still no change in the Cohen'sKappascore.

When an AUC curve is drawn on the probabilities, achieved 64%.

Applying an XGBoost classifier gave us the AUC of 66%.

An ADABoost classifier model(which gave an AUCof 66%) is fit on the test data after manipulations done in the same manner of the train data.
 
 
