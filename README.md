# Mod-3-project

## Brief background
Telemarketing is still the main promotion approach in commerical banking industry today. Emails from banks are usually neglected by clients or directly into 'Ads' tag or spam. Bank tellers are calling their clients to pursuade them to make term deposit, open money market accounts, loans, etc. Telemarketing promotion is very time-consuming. A bank staff can call a client for more 10 times spending total 3 hours without getting a positive result. A good telemarketing campaign can get good amount of positive response without inputting too much human resources.

Therefore, it is essential to understand which type of clients are more likely to response positively to the promotion. And, it is important to establish a model to predict the telemarketing campaign outcome based on the bank's purposes for the management level to understand the potential outcome.

Utilizing a Portuguese Bank telemarketing campaign dataset, this project established model to predict outcome of bank term-deposit telemarketing campain and analyzed clients' response to the term deposit promoting with various clients' attributes. 

## Goals of this project: 

(1) analyze how various features can influence the telemarketing campaign response, help bank tellers to improve telemarketing efficiency; 

(2) develop machine learning models that can help bank tellers to predict telemarketing campaign response from clients;

(3) based on the results of various models, make suggestions to bank managers or bank tellers regarding how to use models.

## Resources of data:
The resource of data is from Kaggle.com
https://www.kaggle.com/yufengsui/portuguese-bank-marketing-data-set

## This repository contains the following files:

*  mod3_project_1.ipynb, -- the main jupyter notebook containing 7 parts: 
1. Data collection and cleaning
2. Explanatory Data Analysis, descriptive statistics
3. Hypothesis test and analysis
4. Preprocessing & feature engineering
5. Various model fitting
6. Models evaluation
7. Business conclusion and discussion

*  Portuguese Bank.csv, -- the dataset that contains all independent variables and taget variales with more than 40,000 observations 

*  bank data raw.csv, -- original raw data which contains all independent variables and taget variales but in lines of strings

*  precision.sav -- the prediction model that gives best precision score

*  sensitivity.sav -- the prediction model that gives best sensitivity score

## Some conclusions: 

### There are variuous factors that can influence the clients' response to banks' telemarketing. From the analysis in this project, we can conclude that:

* Clients with different ages and occupations do have different response rate to telemarketing, middle age people has the least interests. This is because early age people (students, lack of investment experiences) and old age people (retired people, more conserative) don't have many other choices or willingness to do other investment. The EDA of different occupations responses and different ages responses are very consistent on this point. So bank tellers shall focus more on these clients so that they can have higher success rate.
* Education levels matters. Low education level people (people only has primary education experience) are not likely to have positive response to the telemarketing campaign. Among the 3 different education levels, the post-secondary education level (highest) has significance response rate 14%, higher than the middle level(high school education) 10%, and further higher than 8% (lowest level, people only with the primary education). So bank tellers shall focus more on clients with higher education. Check the following plot:
![image](https://user-images.githubusercontent.com/64159084/91112631-a26ccc00-e651-11ea-9da5-7846e454877a.png)

* There are certain periods of time during a year people start saving. People usually spend more on holiday seasons (like Christmas) and are paying back credit cards after that. You can see March is a peak of people's response to term deposit. Another peak is close to the end of a year, after summer time. Bank tellers shall start telemarketing campaigns in this periods in order to have good outcome.


### Some tips to improve bank tellers' telemarketing strategies:

* Don't call people too many times, as shown in Explanatory Data Analysis, when the contact time is beyond 10, the positive response rate decrease, beyond 15 times is the worst. If a client is willing to make term deposit, he/she will do it when bank teller calls him/her certain times. But too many contacts make people feel annoying. Here is the graph showing relationship of response rate and contact times :
![image](https://user-images.githubusercontent.com/64159084/91112827-1b6c2380-e652-11ea-857c-7d9acfbd4a2c.png)

* Bank balance is not super important, one may assume that people with high balance in bank accounts are more likely to make term deposit, just because that this person have money to do it. But our analysis of features importances in section 5.3 and 5.5 shows the balance amount is not that important. Balance has some contribution to the final result, but not among the top 5. One thing to remember is that many people bank with more than 1 banking institution. So, low balance in this bank does not mean the person cannot make term deposit. High balance does not mean this person is likely to make term deposit, maybe other banks are offering this person better promotion.

### The way to use the models in the notebook:

* If the bank has abundant staff and not too busy in this season, it can use the model in section 5.5 with high sensitivity in order not to miss the false negatives. This way although the precision is not good enough, but the bank gets as many as people truely will make term deposit.
* If the bank has limited human resources, it can use the model in section 5.3 with high precision, which filters out only limited amount of candidates to be contacted. By doing this, they can get very high success rate. But, this way, bank will loss many false negatives.
* In our idea, bank who is serious about the telemarketing campaign shall use model in section 5.5 with high sensitivity to get as many clients as possible, because it is not just for term deposit in this campaign, it can also increase 'clients stickiness'. Term deposit is not only to get more deposit, but can also have the clients to stick with this bank for a long time, which can also bring other opportunities to the bank

## Project presentation link:

https://docs.google.com/presentation/d/1d5TTpYs8dPQW01Yw9gQuYmBFweYwcr8R8DP32NsO-z8/edit#slide=id.p
