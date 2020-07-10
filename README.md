# Mod-3-project
by Zhi Chen and Daniel Mocombe

## Brief background
Telemarketing is still the main promotion approach in commerical banking industry today. Emails from banks are usually neglected by clients or directly into 'Ads' tag or spam. Bank tellers are calling their clients to pursuade them to make term deposit, open money market accounts, loans, etc. Telemarketing promotion is very time-consuming. A bank staff can call a client for more 10 times spending total 3 hours without getting a positive result. A good telemarketing campaign can get good amount of positive response without inputting too much human resources.

Therefore, it is essential to understand which type of clients are more likely to response positively to the promotion. And, it is important to establish a model to predict the telemarketing campaign outcome based on the bank's purposes.

Utilizing a Portuguese Bank telemarketing campaign dataset, this project analyzed clients' response to the term deposit promoting with various clients' attributes. 

## Goals of this project: 

(1) analyze how various features can influence the telemarketing campaign response, help bank tellers to improve telemarketing efficiency; 
(2) develop machine learning models (with various metrics) that can help bank or bank tellers to predict response of the clients;
(3) Based on the results of various models, make suggestions to bank or bank tellers regarding how to use models.

## Resources: There are 2 resources of data:
--(1) __Kaggle.com dataset__, prediction model will be build up based on this dataset; 
--(2) __Web scraping diamonds data from www.bluenile.com__ , data from www.bluenile.com will be compared to predictions. 

## This repository contains the following files:

*  mod2 project1.ipynb, -- the main jupyter notebook containing 6 parts: 1). 1. Data Collection and cleaning; 2). Explanatory Data Analysis, descriptive statistics; 3). Hypothesis Testing; 4). Model with MultipleLinear Regression and Lasso Regression, Comparing Models; 5). Feature Engineering, Establishing Final Model; 6). Business/Social Case & Conclusions. All EDA graphes are in this notebook; final model is in section 5; and each section has conclusion, and, final conclusions are made as summarized to seven points in last section. 

*  selenium webscraping.ipynb, -- I wrote web scraping code in this notebook to get data from online jewelry sales website. In this, various feature values can be input to scrape the data in the range I desire. 

*  diamonds.csv, -- the dataset downloaded from kaggle.com, I used this dataset to establish my prediction model. 

*  bluenile.csv, -- the data I scraped from www.bluenile.com, saved as .csv file. 

*  geckodriver.exe -- the file needed to run selenium scraping, to open firefox browser. 

*  diamondpredict.sav -- the final prediction model I saved using pickle, for future use.

## Some conclusions: 

* In the diamonds market, prices are like exponentially related to carat weight, as the carat weight get larger and larger, price increase faster and faster. One 2 carats diamond are much valuable than 2 one carat diamonds.

* In reality, top quality diamonds(higher clarity, higher colorless) mainly lay in smaller diamonds range, it is difficult to get larger carat weight high clarity (or high color level) diamonds. Bigger diamonds are more likely to have middle or low clarity or colorless levels

* Pure dimensions (x,y,z) are usually not cared in diamonds selection, since carat weight value can represent them. But the shape matters, so L/W and depth are important features that can affect diamonds prices.

* Overall speaking, middle color level and middle clarity level have the most percentage in all levels.

* There is statistically significant difference in carat weight of diamonds with different cut levels, there is statistical significant difference in prices of diamonds with different color levels.

* There is relationship between the distributions of diamond clairity levels category and the color levels category (they are not independent), this is determined by diamonds forming mechanism and processing.

* Prediction model developed based on Kaggle dataset fit perfectly with Kaggle dataset, but predict higher prices than online sales prices. Normally, online sales prices are lower, this makes sense. And, datasets from different resources many not reflect each other well. Data resources of learn and practices (non-profit) may not have the same trend as data from commercial resources. Before using dataset to make serious modeling and professional prediction, reliability of data resources and type of the data resources shall be considered.

## Project presentation link:

https://docs.google.com/presentation/d/1YXuIXfcZhcGVjATO_c1_hLBSJ684fRFyFeLu2MA_zYQ/edit?usp=sharing
