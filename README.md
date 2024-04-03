# 17_BankCampaign
https://github.com/toshiokimura/17_BankCampaign/blob/main/17_prompt_III3.ipynb

**The dataset collected is related to 17 campaigns** that occurred between May 2008 and November 2010, corresponding to a total of 79354 contacts.
**The dataset** includes various client characteristic features such as age, job, marital, education, default, balance, housing, loan, contact, day of week as well as a term deposit subscription status. 



Model	Train Time	Score Time	Train Accuracy	Test Accuracy
0	LogisticRegression	0.509500	0.018991	0.887346	0.887346
1	KNeighborsClassifier	0.017254	5.485056	0.892234	0.878217
2	DecisionTreeClassifier	0.176354	0.030005	0.917775	0.866660
3	SVC RBF	11.303434	28.495463	0.887346	0.887346
4	SVC poly	48.241792	12.917504	0.887346	0.887346
5	SVC linear	52.276775	6.829769	0.887346	0.887346
6	SVC sigmoid	17.329399	10.135247	0.882296	0.882393
7	KNeighborsClassifier all features	0.025050	5.052671	0.930821	0.905215
8	KNeighborsClassifier all features grid (1, 22, 2)	39.400346	6.453232	0.930821	0.913373
9	DecisionTreeClassifier all features	0.592292	0.055007	1.000000	0.889094
10	LogisticRegression all features	6.636321	0.021000	0.910103	0.913761
11	LogisticRegression all features L1 cost	5.238281	0.010944	0.910265	0.914732
12	LogisticRegression all features L2 cost	0.580969	0.013006	0.909909	0.914635

![image](https://github.com/toshiokimura/17_BankCampaign/assets/44044445/b67202ba-521d-4fce-a545-3a4a7490c6f5)
