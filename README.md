Loan Approval for Small Business and Credit Risk Management  using Regression Analysis on loan dataset
Problem Definition:
The loan dataset is downloaded from Kaggle and the task is to analyze the data and build a regression model to predict the propensity of small business borrowers to pay back their loans if approved.
Methodology
	•	Background
	•	Introduction
	•	Challenges experienced and how these were resolved
	•	Implementation
	•	Results

Description of data
	•	Name of the data: loan.csv (originally named SBAnational.csv).

              
 How to Run the Program using the loan Dataset.
For this Dataset, below is the steps taken to run the program in R.
> library(ggplot2)
> library(dplyr)
>library(broom)
> library(ggpubr)
>loan<-read.csv("//Users//muyi//Desktop//loan.csv")
> loan
> str(loan)
> summary(loan)
> head(loan)
> names(loan)
> cor(loan$NoEmp, loan$int.rate)
> cor(loan$int.rate, loan$Term)
> cor(loan$NoEmp, loan$Term)
> hist(loan$NoEmp)
> hist(loan$int.rate, col = "blue", xlab = "int_rate", main = "Histogram")
> hist(loan$NoEmp, col = "blue", xlab = "NoEmp", main = "Histogram")
> plot(int.rate ~ NoEmp, data=loan)
> plot(fico ~ Term, data=loan)
> plot(fico ~ int.rate, data=loan)
> fico.lm<-lm(fico ~ int.rate + NoEmp + Term, data = loan)
> summary(fico.lm)
> par(mfrow=c(2,2))
> plot(fico.lm)
