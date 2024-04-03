# 17_BankCampaign
https://github.com/toshiokimura/17_BankCampaign/blob/main/17_prompt_III3.ipynb

## Business Objective

**The business objective of the task is to execute the direct marketing campaigns efficiently, considering ROI based on the result of the analysis of the previous campaign data.** The analysis here is essentially to predict if a new client will subscribe to a term deposit (Yes or No) through a campaign using phone calls or e-mail. For prediction, we will make classification models, which include a logistic regression model with multiple inputs (1/1+exp(-β0-β1*x1-β2*x2 ....) using OneHotEncoder as needed for categorical features and other classification techniques. Since there are relatively many features, we may want to use the L1 or L2 penalty to optimize the model calculation cost. It is ideal for a model to output a probability, so the number of target customers can be adjusted by changing the threshold depending on the budget of this project. This time, given that the campaign media cost is relatively high, like phone calls, our priority is to maximize "accuracy" rather than minimize false negatives at the cost of accepting false positives, which is suitable for low-cost campaigns like e-mail.

## Understanding the Data

**The dataset collected is related to 17 campaigns** that occurred between May 2008 and November 2010, corresponding to a total of 79354 contacts based on the paper. The actual data used is slightly differnet actually and it has a tota of 41188 contacts. The dataset includes various client characteristic features such as age, job, marital, education, default, balance, housing, loan, contact, day of week as well as a term deposit subscription status. 


## Model Comparisons

![image](https://github.com/toshiokimura/17_BankCampaign/assets/44044445/b67202ba-521d-4fce-a545-3a4a7490c6f5)


Overall test accuracy results are in the 87% - 91% range. 

DecisionTreeClassifier performs well at Train, but not well at Test.

Using all features vs. 7 features gives better results.

"LogisticRegression all features L1 cost" performs the best (0.914732) among all the models I tested, but it is not that dramatically better than others.

The reason behind this would be the data itself are not clearly separated between y = yes and y = no in the features space, so even if we tweak the model, there is a saturation of test accuracy.


![image](https://github.com/toshiokimura/17_BankCampaign/assets/44044445/8b66763a-a239-4f1b-820a-54b2f74d8c36)


High chance in **March and August** and low chance in **May**.

**Longer duration of contact** does matter to the succesful result. This can be controlled by the compnay, so I will recommend the cliant to talk as long as possible over the phone.

**"emp.var.rate"** has a negative impact to the succesful result.

**"cons.price.idx"** has a positive impact to the succesful result.

**"pdays"** has a negative impact to the succesful result. "pday" is the number of days that passed by after the client was last contacted from a previous campaign. So I will recommend the cliant to have campaigns successievely.
