# Starbucks Capstone Project | Udacity 

## Overview

Starbucks, one of the world’s most popular coffee shops, frequently provides offers to its customers through its rewards app to drive more sales. These offers can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). This project is focused on tailoring the promotional offers for customers based on their responses to the previous offers and predict the response of a customer to an offer. Firstly, to best analyze the data thoroughly, Exploratory Data Analysis(EDA) is performed to find the data representations & characteristics. Secondly, machine learning models are built  predict the customer’s response to an offer so that Starbucks can properly target who they send their offers to.


## Datasets and Inputs

For this project, the data sets are provided by Starbucks and Udacity in the form of three JSON files. These contains simulated data that mimics customer behavior on the Starbucks rewards mobile app.
-   portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
-   profile.json - demographic data for each customer
-   transcript.json - records for transactions, offers received, offers viewed, and offers completed

Here is the schema and explanation of each variable in the files:

**portfolio.json**

-   id (string) - offer id
-   offer_type (string) - type of offer ie BOGO, discount, informational
-   difficulty (int) - minimum required spend to complete an offer
-   reward (int) - reward given for completing an offer
-   duration (int) - time for offer to be open, in days
-   channels (list of strings)

**profile.json**

-   age (int) - age of the customer
-   became_member_on (int) - date when customer created an app account
-   gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
-   id (str) - customer id
-   income (float) - customer's income

**transcript.json**

-   event (str) - record description (ie transaction, offer received, offer viewed, etc.)
-   person (str) - customer id
-   time (int) - time in hours since start of test. The data begins at time t=0
-   value - (dict of strings) - either an offer id or transaction amount depending on the record

**Installations**
This project was written in Python, using Jupyter Notebook on Anaconda. The relevant Python packages for this project are as follows:

pandas
numpy
math
json
matplotlib
seaborn
sklearn.model_selection (train_test_split module)
sklearn.preprocessing (StandardScaler )
tensorflow
keras

**Conclusions**
Overall, this project was surprisingly challenging due to the structure of the transcript.json dataset and the preprocessing required to generate useful ML model predictions. However, I learned a lot in this project and developed solutions to the challenges discussed in the project proposal:

Developed predictive ML models to classify whether views and completes a promotional offer based on personalized customer and offer characteristics
Developed predictive ML models to determine how much a customer spends by completing an offer after subtracting out the reward cost. The ML predictive model outperforms the benchmark model in each of our three studies, and the benchmark models also perform pretty well.
Determined the features that are most significant to whether or not a customer views and completes a promotional offer
Defined key customer segment groups based on customer demographics
The models and insights developed in this project allow the company to understand the primary drivers of an effective and profitable promotional offer. The predictive models will enable the company to personalize the characteristics of each promotion to maximize its odds of success for each customer. This project is an excellent example of how machine learning models benefit marketing campaigns and create business value. Lastly, this project shows why a more efficient and straightforward machine learning model is often preferable to a larger and more complex deep learning model.

**Blogpost:** https://medium.com/@carmen.ilie/starbucks-capstone-project-f9c0082f4669

**Files**
The following files attached to this GitHub's repository include the following:

Starbucks_Capstone_notebook.ipynb: This is the Jupyter Notebook in which I performed all my work.
data: This contains the three JSON files provided by Starbucks / Udacity as noted above.
portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
profile.json - demographic data for each customer
transcript.json - records for transactions, offers received, offers viewed, and offers completed

**Acknowledgements**
Special thanks to Starbucks and Udacity for providing the data utilized in this project!
