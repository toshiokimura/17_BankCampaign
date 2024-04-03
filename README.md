# Bank Campaign

## Business Objective

**The business objective of the task is to execute the direct marketing campaigns efficiently, considering ROI based on the result of the analysis of the previous campaign data.** The analysis here is essentially to predict if a new client will subscribe to a term deposit (Yes or No) through a campaign using phone calls or e-mail. For prediction, we will make classification models, which include a logistic regression model with multiple inputs (1/1+exp(-β0-β1*x1-β2*x2 ....) using OneHotEncoder as needed for categorical features and other classification techniques. Since there are relatively many features, we may want to use the L1 or L2 penalty to optimize the model calculation cost. It is ideal for a model to output a probability, so the number of target customers can be adjusted by changing the threshold depending on the budget of this project. This time, given that the campaign media cost is relatively high, like phone calls, our priority is to maximize "accuracy" rather than minimize false negatives at the cost of accepting false positives, which is suitable for low-cost campaigns like e-mail.

## Understanding the Data
**The dataset collected is related to 17 campaigns** that occurred between May 2008 and November 2010, corresponding to a total of 79354 contacts based on the paper. The actual data used is slightly different actually, and it has a total of 41188 contacts. The dataset includes various client characteristic features such as age, job, marital, education, default, balance, housing, loan, contact, day of week as well as a term deposit subscription status.


## Model Comparisons

The first 7 models below use just the bank information features (columns 1 - 7: age, job, marital, education, default, housing, and loan). The remaining 6 models use all the features.

![image](https://github.com/toshiokimura/17_BankCampaign/assets/44044445/f452abc4-b843-4145-94a7-6736b3fb4538)

* Overall test accuracy results are in the 87% - 91% range. 

* Using all features vs. 7 features gives better results with acceptable increase of Train time.

* SVS takes a very long time at both the Train and Score stages.

* DecisionTreeClassifier performs well at Train but not at Test, meaning overfitting.

* KNeighborsClassifier at k=19 shows the best accuracy with ~1% better than the default (k=5).

* "LogisticRegression all features L1 cost" performs the best (0.914732) among all the models I tested, but it is not that dramatically better than others.

* The reason behind this would be the data itself are not clearly separated between y = yes and y = no in the features space, so even if we tweak the model, there is a saturation of test accuracy.


## Important Features

Based on the fitting result of LogisticRegression using all features at L1 cost, there are some features highlighted as key to successful campaigns.

![image](https://github.com/toshiokimura/17_BankCampaign/assets/44044445/32aec4c1-35a8-4f13-b5a4-266ea58cbab8)

* There is a high chance in **March and August** and a low chance in **May**.

* **Longer duration of contact** does matter for a successful result. The company can control this, so I recommend that the client talk as long as possible over the phone.

* **"emp.var.rate"** has a negative impact to the successful result.

* **"cons.price.idx"** has a positive impact to the successful result.

* **"pdays"** has a negative impact on the successful result. "pday" is the number of days that passed by after the client was last contacted from a previous campaign. So, I will recommend that the client have successive campaigns.
