# Optimizing Truist Bank's Term Deposit Phone Marketing Campaign
![enter image description here](https://images.unsplash.com/photo-1607863680198-23d4b2565df0?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80)
## Business Understanding
A regional bank in Texas recently started offering term deposits as a way for their customers to invest their money. Term deposits are time-restricted investments that offer some fixed rate of return over a pre-defined measure of time, ranging anywhere from three months to several years. These kinds of investments are typically attractice to those who are more risk-averse, concerned about movement in the stock market, or want a fixed amount of money coming in every month. Customers at the bank can easily transfer funds from their current accounts to these term deposits, and while there are some limitations on withdrawing money from these term deposit accounts, they offer a higher interest rate than normal checking or savings accounts, so there is an attractive tradeoff for those with extra capital.

This regional bank recently underwent a sales/marketing campaign to encourage current customers to also sign up for term deposits. This was done by contacting customers over the phone to gauge their interest and discuss their options.

Our goal is to take the data from their sales campaign and predict whether or not a customer signed up for term deposits. From there, we can determine feature importance from our model and gauge how best to optimize future sales efforts for term deposits that are highly lucrative for the bank.

## Data
Our data included information on over 45,000 current customers who had accounts with Truist. Data included demographic information such as age, marital status and education level, account information including their current balance and any loans to their name, and finally marketing specific information about frequency of calls, length of conversations, and most importantly whether or not they subscribed to term deposits.

## Modeling
Three classification models were used: decision tree, random forest, and ADABoost. The idea is that a single decision tree can be tuned, and then a random forest can be an aggregate of trees, and then ADABoost can create trees that learn form the mistakes of previous ones. The goal was to predict whether or not a customer signed up for term deposits.

Our random forest model had the best accuracy at 90.2%. 

![enter image description here](https://github.com/acollins28/Phase-5/blob/main/Presentation%20Materials/outcome%20prediction%20confusion%20matrix.PNG?raw=true)

To prepare for the modeling process: some data had to be converted from objects to floats, often because the columns were binary in nature. Others had to be one hot encoded since they were more categorical.
A MinMax scalar was applied to the one hot encoded data to make every column be on the same unit scale while preserving the binary nature of other columns.

## Results
Our random forest determined the five most important features when predicting subscription outcome:

![enter image description here](https://github.com/acollins28/Phase-5/blob/main/Presentation%20Materials/what%20predicts%20subscription.PNG?raw=true)

From these top 5, four primary action items were determined to help improve the marketing campaign's success:
1. Write scripts and create conversation that allows phone calls to last at least 7 minutes.
2. Target customers with at least $1800 in their account
3. Target customers who are at least 38 years old
4. Follow up with non-subscribers more frequently

## Navigating the Repository
[Data](https://github.com/acollins28/Phase-5/tree/main/Data)<br>
[Presentation Materials](https://github.com/acollins28/Phase-<br>5/tree/main/Presentation%20Materials)<br>
[Notebook](https://github.com/acollins28/Phase-5/blob/main/Notebook.ipynb)<br>
[Presentation](https://github.com/acollins28/Phase-5/blob/main/Presentation.pptx)
