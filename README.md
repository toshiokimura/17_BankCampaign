# 17_BankCampaign
https://github.com/toshiokimura/17_BankCampaign/blob/main/17_prompt_III3.ipynb

**The dataset collected is related to 17 campaigns** that occurred between May 2008 and November 2010, corresponding to a total of 79354 contacts.
**The dataset** includes various client characteristic features such as age, job, marital, education, default, balance, housing, loan, contact, day of week as well as a term deposit subscription status. 





![image](https://github.com/toshiokimura/17_BankCampaign/assets/44044445/b67202ba-521d-4fce-a545-3a4a7490c6f5)


Overall test accuracy results are in the 87% - 91% range. 

DecisionTreeClassifier performs well at Train, but not well at Test.

Using all features vs. 7 features gives better results.

"LogisticRegression all features L1 cost" performs the best (0.914732) among all the models I tested, but it is not that dramatically better than others.

The reason behind this would be the data itself are not clearly separated between y = yes and y = no in the features space, so even if we tweak the model, there is a saturation of test accuracy.
