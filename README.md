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
   
 We were asked to find the area under ROC curve between the predicted probability and the observed target.
 
 The dataset consists about 3,45,000 rows and 41 features.
 
 We have seperated the numerical and the categorical variables, tried to find the correlation between the numerical features using the heatmap from the seaborn package.
 
 Feature engineering is done on the categorical variables, with the date of birth
 
 
