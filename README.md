# Loan Data from Prosper Exploration:
## by Rania Souri


## Dataset

The dataset contains 113937 loans with 81 variables on each loan, for this exploration, we choose to focus on these variables:

**LoanKey:** Unique Key for each loan. This is the same key that is used in the API.
**Term:**The length of the loan expressed in months.
**LoanStatus**:The current status of the loan: Cancelled, Chargedoff, Completed, Current, Defaulted, FinalPaymentInProgress, PastDue. The PastDue status will be accompanied by a delinquency bucket.
**BorrowerAPR**:The Borrower's Annual Percentage Rate (APR) for the loan.
**BorrowerRate**:The Borrower's interest rate for this loan.
**ListingCategory**:The category of the listing that the borrower selected when posting their listing: 0 - Not Available,1 - Debt Consolidation, 2 - Home Improvement, 3 - Business, 4 - Personal Loan, 5 - Student Use, 6 - Auto, 7- Other, 8 - Baby&Adoption, 9 - Boat, 10 - Cosmetic Procedure, 11 - Engagement Ring, 12 - Green Loans, 13 - Household Expenses, 14 - Large Purchases, 15 - Medical/Dental, 16 - Motorcycle, 17 - RV, 18 - Taxes, 19 - Vacation, 20 - Wedding Loans
**Occupation**:The Occupation selected by the Borrower at the time they created the listing.
**Employment Status**:The employment status of the borrower at the time they posted the listing.
**LoanOriginalAmount**:The origination amount of the loan.
**MonthlyLoanPayment**:The scheduled monthly loan payment.
**StatedMonthlyIncome**: The monthly income the borrower stated at the time the listing was created.
**CreditScoreRangeLower**:The lower value representing the range of the borrower's credit score as provided by a consumer credit rating agency.
**CreditScoreRangeUpper**:The upper value representing the range of the borrower's credit score as provided by a consumer credit rating agency.


The dataset can be found [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv) and this [data dictionary](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0) explains the variables in the data set.


## Summary of Findings

> In the exploration, I found that in one hand, Sated Monthly Income is negatively 
correlated with the Borrower APR and Borrower Rate,and in the other hand, the Monthly income is positively coorelated with 
the Loan Original Amount and the loan monthly payment.Which mean that when the incomes increases, 
the loan Original Amount increase and so that the loan monthly payment increase, and by that the Borrower APR decrease.
Note also, that The Borrower APR and Borrower Rate are highly correlated.

Outside of the main variables of interest, I verified the relationship between The Borrower ARP, Borrower Rate and the Upper or Lower Credit Score Range, and I found that they are negalively correlated, thus, the better your score, the lower your APR and Rate.
For the dataset given, there was an interesting interaction in the categorical loan features. If the term of the loan is large the Borrower Rate increase,and even though The borrower Rate and APR are correlated, that it's not the case for the Borrower APR which decrease for the term 36 and that's can be explained because most of the loan for this term has been completed, and obviously a good rating is attributed.Another thing to note is that the Borrower APR variation interval differs from one category to another. Therefore, the type of loan affect also the interval of the Borrower APR.


## Key Insights for Presentation

> For the presentation, I just focus on features that could affect the borrower APR, which are Original Loan Amount, Upper/Lower Credit Score Range, The term and the Listing Category. I started by showing the distribution of borrower APR and loan amount variable.Then, I plotted the correlation between the numerical variables, to explain that the features I focused on in the visualization part are based on the correlation coefficient.After That, I showed the relationship between APR and The origial Loan Amount, as well asthe relation between  Borrower APR and the  Upper/Lower Credit Score Range. I also plotted the relation between the categorical variable "Term" and the Borrower APR and Borrower Rate, and I investigated on the Listing Category effect on relationship of APR and Loan Amount.