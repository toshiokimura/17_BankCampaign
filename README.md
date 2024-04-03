# Bank Campaign


## Business Objective

**The business objective of the task is to execute the direct marketing campaigns efficiently, considering ROI based on the result of the analysis of the previous campaign data.** The analysis here is essentially to predict if a new client will subscribe to a term deposit (Yes or No) through a campaign using phone calls or e-mail. For prediction, we will make classification models, which include a logistic regression model with multiple inputs (1/1+exp(-β0-β1*x1-β2*x2 ....) using OneHotEncoder as needed for categorical features and other classification techniques. Since there are relatively many features, we may want to use the L1 or L2 penalty to optimize the model calculation cost. It is ideal for a model to output a probability, so the number of target customers can be adjusted by changing the threshold depending on the budget of this project. This time, given that the campaign media cost is relatively high, like phone calls, our priority is to maximize "accuracy" rather than minimize false negatives at the cost of accepting false positives, which is suitable for low-cost campaigns like e-mail.

## Understanding the Data
**The dataset collected is related to 17 campaigns** that occurred between May 2008 and November 2010, corresponding to a total of 79354 contacts based on the paper. The actual data used is slightly different actually, and it has a total of 41188 contacts. The dataset includes various client characteristic features such as age, job, marital, education, default, balance, housing, loan, contact, day of week as well as a term deposit subscription status.



