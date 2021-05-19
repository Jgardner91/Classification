# Classification

Classification Write Up

Abstract

The Goal of this project was to use a few different classification models to demonstrate how using historical loan data can be helpful in making loan decisions in the present and future. The goal is not to put forth a model that classifies every potential default loan correctly but to demonstrate how 3 metrics in particular affect the cash flow of a lending office.

Design

The project idea was motivated by trying to understand how loan decisions can help or hurt a bank/lending organizations bottom line and what effect that has on the consumers. Classifying loans that could potentially default, as such, can enhance a loan officers ability to correctly identify an applicants 'worthiness' of a loan.

Data

The dataset contains over 850,000 unique loans, data for all loans issued through the years 2007 - 2015, including the current loan status (Current,Late, Fully Paid, etc.) and latest payment information. The Data set is highly imbalanced as the ratio of positive class(Default) to negative Class is 5.5%(0):94.5%(1). Some relevant features include , loan amount, interest rate, annual income, debt to income ratio, loan grade, loan sub grade, months since last credit inquiry and 65 other numerical and catergorical features.

Algorithms

Featrue Engineering
Converted loan grade,homeownership type, and loan term, to binary dummy variables.
Explored class imbalance by plotting a barplot
Explored feature 'seperability' with kde plots and pair plots
Models
K nearest neighbors(K=67), logistic regression, and tree classifier were used before deciding on logistic regression as my final model

Model Evaluation and Metrics

Seperated data into train/val/test split. Setting aside 20% of my data for final testing and using val to compare my models. The metric of comparison was F Beta (beta = .7). Class imbalance needed to be adressed so before scoring on fbeta I used class weights to penalize incorrect predictions of the positive class. Using a 10:1 ratio.

Results

FBeta Score Test(LogReg): .55

Tools

1.Numpy and Pandas for data manipulation 

2.Seaborn , google sheets , and keynote for visuals 

3.Sql and google sheets for querring

