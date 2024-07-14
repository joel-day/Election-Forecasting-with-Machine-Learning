# Buying Elections
# Official Paper - https://github.com/joel-day/Election-Forecasting-with-Machine-Learning/blob/main/Buying%20Elections.pdf
# What is this all about?
This project establishes the positive correlation between financial contributions from individuals and vote share in U.S. federal senate elections. The best election forecasting models in recent decades are trained on a combination of polling data and a hand-selected bundle of supplementary features. While traditional polling processes are being replaced by methods that utilize data on social media, the supplementary bundle of features remains necessary for optimal performance – this project provides that bundle. 

![Sample Vote Share vs  log(Total Contributions Received from Individuals_ X Months Before Election in Federal Senate Elections 2016-2020](https://github.com/joel-day/Predicting-U.S.-Federal-Senate-Elections/assets/105340191/7ea79aee-af1c-4627-98c6-384c497ee959)


# Results
Among the 5 models (neural network, random forest, gradient boosting, support vector machine, and an ensemble model), the Random Forest model perfromed the best with an F1-socre of 81%.

![Precision, Recall,   F1-Score of 5 Model's Predictions for the 2020 Federal General Senate Elections (1)](https://github.com/joel-day/Election-Forecasting-with-Artifial-Intelligence/assets/105340191/9c63b057-a8a7-490c-a6f8-7c246f93492b)


# Model Features:
### Sum of Contributions from Individuals, Age, Incumbency, Party, Multi-Candidate Committee Participation (FEC), Unemployment, & Voter Education Inequality

A few notes. Strategic campaigning and the use of campaign funds can swing undecided voters and increase voter participation. A large budget enables more outreach and exposure both in person and online. Exposure theory proves that repeated exposure to a candidate will improve the impression of them (Oppenheimer et al., 1986). Only the contributions from individuals are used in the totals because only they can vote, and multi-candidate committees participation partially captures the support of PAC contributions. Contribution totals are calculated using data up to one month before the election.Social demographics are also additive to election models (Myilvahanan et al., 2023). This project will focus on state education levels. For each state, the ratio of people who have a college degree to those who do not have a high school degree is calculated. Regarding the unemployment varibale, both Kennedy et al. (2017) and Takashi (1981) warn about the poor performance of economic indicators, however, employment and inflation may be weak exceptions. Takashi found that employment was predictive, and Kennedy et al. found that inflation was predictive. I included unemployment because it varies more across the sample elections.

# Navigatating the GitHub
Python code for this project is contained in two scripts, one for data acquisition and another for the visuals, pre-processing, and modeling. 
### Script 1
'(1)_Senate_reults.ipynb' downloads the data using webscraping and three different API's. It dpends on the following: '1_candidate_ages.xlsx', '1_state_mapping.xlsx', and the 1_months folder which contains the contribuion data. The output of the first scipt is the '2_senate_results.xlsx' file that holds all of the raw data. Take a peak! It also doubles as the input of the second python script. 
### Script 2
'(2)_EDA_Preprocessing_&_Modeling' as the name suggests trains the models. It depends on the The 2_display_states folder for the U.S. map visuals, but these are optional. The models are downloaded as .pkl files and the visuals as .png files. The '1.5_Downloading_bulk_contribution_data.ipynb' splits the massive text file containing the contribtution data. You may not need it if you have enough processing power (i did not lol).
