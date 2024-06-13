# Buying Elections - Joel Raymond Day
### https://www.linkedin.com/in/joelrday/



# What is this all about?
This project establishes the positive correlation between financial contributions from individuals and vote share. The best election forecasting models in recent decades are trained on a combination of polling data and a hand-selected bundle of supplementary features. While traditional polling processes are being replaced by methods that utilize social media information, the supplementary bundle of features remains necessary for optimal performance – this project provides that bundle. Results have demonstrated that a model, excluding polling data and knowledge of the candidates’ state, can predict which 2020 candidates will obtain 50% vote share with an F1 score of 81%.

# Model Features
Along with the age, incumbency, and party of the candidate, the following features will be used:

### Contributions from Individuals and Multi-Candidate Committee Participation (FEC)
Strategic campaigning and the use of campaign funds can swing undecided voters and increase voter participation. A large budget enables more outreach and exposure both in person and online. Exposure theory proves that repeated exposure to a candidate will improve the impression of them (Oppenheimer et al., 1986). Only the contributions from individuals are used in the totals because only they can vote, and multi-candidate committees participation partially captures the support of PAC contributions. Contribution totals are calculated using data up to one month before the election. 

### Voter Education Inequality by State
Social demographics are also additive to election models (Myilvahanan et al., 2023). This project will focus on state education levels. For each state, the ratio of people who have a college degree to those who do not have a high school degree is calculated. 

### Economy Indicator - Unemployment
Both Kennedy et al. (2017) and Takashi (1981) warn about the poor performance of economic indicators, however, employment and inflation may be weak exceptions. Takashi found that employment was predictive, and Kennedy et al. found that inflation was predictive. I included unemployment because it varies more across the sample elections.  

# Navigatating the GitHub
Python code for this project is contained in two scripts, one for data acquisition and another for the visuals, pre-processing, and modeling. 

### Script 1
'(1)_Senate_reults.ipynb' downloads the data using webscraping and three different API's. It dpends on the following: '1_candidate_ages.xlsx', '1_state_mapping.xlsx', and the 1_months folder which contains the contribuion data. The output of the first scipt is the '2_senate_results.xlsx' file that holds all of the raw data. Take a peak! It also doubles as the input of the second python script. 

### Script 2
'(2)_EDA_Preprocessing_&_Modeling' as the name suggests trains the models. It depends on the The 2_display_states folder for the U.S. map visuals, but these are optional. The models are downloaded as .pkl files and the visuals as .png files. 
