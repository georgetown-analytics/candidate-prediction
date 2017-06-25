# Predicting Congressional Elections
Georgetown Data Science Candidate Prediction Project

**Team Members:** Stephanie Li, Natasha Pangarkar, Camille Smith, Sarah Thambidurai, Qing Zhao

**Project Domain:** Political Science, Electoral Demographics, Donor Networks

**Project Overview**

*Problem/Hypothesis:*

Using demographic information and donor information, it is possible to predict the winner of congressional general elections.

We are looking at this problem from two perspectives given our data sources: first, can we predict which party will win each election? Second, can we predict when the incumbent will lose the election?

*Data Sources*

We found three readily available data sources:

1. [United States Government Census Data:](https://www.census.gov/mycd/) includes numerous demographic, sociological, and economic features on the population, broken down by congressional district.

2. [Federal Election Commission Data:](https://www.fec.gov/data/advanced/) all the campaign finance information regarding donations given to candidates and their respective Political Action Committees.

3. [CQ Press Library:](http://library.cqpress.com/elections/) dataset of all the election results, including the raw number and corresponding percentages of votes for each candidate, party affiliation, and incumbent status.

**Data Science Pipeline Overview**

This sections gives a brief overview of the steps we followed to develop the model. These steps (as well as assumptions and information on the datasets) are discussed more in the final paper, as well as the powerpoint presentation.

*Ingestion*

Two of the data sets (Census and FEC) were already in .csvs and ready to download in a neat and tidy format. The CQ Press Library data was in an html format with no easy export capability. This jupyter notebook walks through the process of scraping and cleaning a subset of that data (just Alabama's congressional elections information).

*Munging and Wrangling*

Our group created an AWS instance for a PostgreSQL database to store our information. The data required cleaning and standardizing in order to join the three disparate data sources together.

*Computation and Analysis*

We conducted initial data exploration to better understand the data we were working with, and which features would be most relevant to our model.

*Modeling and Application*

For the model, we determined that a linear SVC model would be most applicable to our study.

*Visualization*

As an initial cut at visualization, we looked at a subset of the FEC dataset. This jupyter notebook walks through initial network calculations and visualizations to understand the nature of donor networks, and how we many want to further incorporate network analysis into future models.

**Future Analysis and Applications**

This project illuminated several opportunities for future analysis and modeling. Some of them are listed below:
* Build a larger dataset so we can further explore the idea of features other than incumbency that play a role in determining a winner.
* Collect demographic information of candidates and include them as features (ie, sex, ethnicity, age, religion).
* Incorporate donor network calculations (centrality measures) as features into the model.
* Look at donor networks over time to see how/if incumbency has an effect on the network as a time series function.
