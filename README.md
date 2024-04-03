# Bank Campaign


## Business Objective

**The business objective of the task is to execute the direct marketing campaigns efficiently, considering ROI based on the result of the analysis of the previous campaign data.** The analysis here is essentially to predict if a new client will subscribe to a term deposit (Yes or No) through a campaign using phone calls or e-mail. For prediction, we will make classification models, which include a logistic regression model with multiple inputs (1/1+exp(-β0-β1*x1-β2*x2 ....) using OneHotEncoder as needed for categorical features and other classification techniques. Since there are relatively many features, we may want to use the L1 or L2 penalty to optimize the model calculation cost. It is ideal for a model to output a probability, so the number of target customers can be adjusted by changing the threshold depending on the budget of this project. This time, given that the campaign media cost is relatively high, like phone calls, our priority is to maximize "accuracy" rather than minimize false negatives at the cost of accepting false positives, which is suitable for low-cost campaigns like e-mail.

## Understanding the Data




