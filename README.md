# udacity_python_starbucks_capstone

The capstone project for Udacity's data scientist nanodegree program.

## Project Overview

The object of this capstone project is to answer the following business challenge using the Starbucks dataset:

* Can we use data to build a predictive model to determine whether a customer will complete a promotional offer based on the offer characteristics and customer demographic information?

I analyze three different machine learning (ML) predictive model solutions and compare their performance. These predictive models allow the business to personalize the characteristics of each promotional offer based on each customer’s demographic profile to maximize the probability that the customer completes a promotional offer.

## Installation

This project is written in Python 3 using Jupyter notebooks. The relevant Python packages include:

* numpy
* matplotlib
* scikit-learn
* pandas
* seaborn
* json

## File Descriptions

The key files for this project are:

* Starbucks_Capstone_notebook.ipynb : Code notebook used for data exploration, cleaning, and customer segmentation.
* Convert transcript.ipynb : Code notebook used for the preprocessing of the transcript dataset.
* trainModel_OfferCompleted.ipynb : Code notebook used for data preproccessing and training machine learning (ML) models using scikit-learn to predict completed offers.

## Data

The structure of the dataset provided Starbucks Capstone project notebook is structured as follows. Three files contain the data:
* `portfolio.json` - containing offer ids and metadata about each offer (duration, type, etc.)
* `profile.json` - demographic data for each customer
* `transcript.json` - records for transactions, offers received, offers viewed, and offers completed

The three types of offers presented in the `_type` column of `portfolio.json` are:
* Buy-one-get-one (BOGO): a user needs to spend a certain amount to get a reward equal to that threshold amount.
* Discount: a user gains a reward equal to a fraction of the amount spent. 
* Informational offer: there is no reward, but neither is there a required amount that the user is expected to spend.

Here is the schema and explanation of each variable in the files:

`portfolio.json` - Size: 10 offers by six fields
* *id* (string) - offer id
* *offer_type* (string) - type of offer, i.e., BOGO, discount, informational
* *difficulty* (int) - minimum required spend to complete an offer
* *reward* (int) - reward given for completing an offer
* *duration* (int) - time for offer to be open, in days
* *channels* (list of strings)

`profile.json` - Size: 17,000 users by five fields
* *age* (int) - age of the customer
* *became_member_on* (int) - date when customer created an app account
* *gender* (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
* *id* (str) - customer-id
* *income* (float) - customer's income

`transcript.json` - Size: 306,534 offers by four fields
* *event* (str) - record description (i.e., transaction, offer received, offer viewed, etc.)
* *person* (str) - customer-id
* *time* (int) - time in hours since the start of the test. The data begins at time t=0
* *value* (dict of strings) - either an offer id or transaction amount depending on the record

## Conclusions

Overall, this project was surprisingly challenging due to the structure of the `transcript.json` dataset and the preprocessing required to generate useful ML model predictions. However, I learned a lot in this project and developed a solution to the challenge discussed in the project proposal:

* I developed predictive ML models to classify whether a user completes a promotional offer based on personalized customer and offer characteristics

The models and insights developed in this project allow the company to understand the primary drivers of an effective and profitable promotional offer. The predictive models will enable the company to personalize the characteristics of each promotion to maximize its odds of success for each customer. This project is an excellent example of how machine learning models benefit marketing campaigns and create business value.
