## Table of Contents
1. [Installation](#installation)
2. [Introducing a Dataset](#dataset-introduction)
3. [Project Motivation](#project-motivation)
4. [Data Preparation](#data-preparation)
5. [File Descriptions](#files)
6. [Results](#results)
7. [Author](#author)


### Installation <a name="installation"></a>
* Python versions 3.*.
* Python libraries:
    - Pandas
    - Numpy
    - Matplotlib
    - Seaborn
    - Scikit learn
 
### Introducing a Dataset <a name="dataset-introduction"></a>
This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.

Not all users receive the same offer, and that is the challenge to solve with this data set.

### Project Motivation <a name="project-motivation"></a>
It is the Starbuck's Capstone Challenge of the Data Scientist Nanodegree in Udacity. We get the dataset from the program that creates the data simulates how people make purchasing decisions and how those decisions are influenced by promotional offers. We want to make a recommendation engine that recommends Starbucks which offer should be sent to a particular customer.

We are interested to answer the following two questions:

1. hich offer should be sent to a particular customer to let the customer buy more?
2. Which demographic groups respond best to which offer type?


### Data Preparation <a name="data-preparation"></a>
There are three datasets provided and each dataset is cleaned and preprocessed for further analysis. The target features for analysis are offer_success, percent_success.

1. Portfolio - renaming id column name to offer_id, one-hot encoding of channels and offer_type columns
2. Profile - profile: renaming id column name to customer_id, replacing age value 118 to nan, creating readable date format in became_member_on column, dropping rows with no gender, income, age data, converting gender values to numeric 0s and 1s, adding start year and start month columns (for further analysis)
3. Transcript - renaming person column name to customer_id, creating separate columns for amount and offer_id from value col, dropping transaction rows whose customer_id is not in profile:customer_id, converting time in hours to time in days, segregating offer and transaction data, finally dropping duplicates if any

### File Descriptions <a name="files"></a>
1. data:

- portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.).
- profile.json - demographic data for each customer.
- transcript.json - records for transactions, offers received, offers viewed, and offers completed.
2. Starbucks_Capstone_notebook.* : contains notebook file.

### Results<a name="results"></a>
The main observations of the code are published [here](https://medium.com/@harsha.kumar3/a-smarter-way-to-send-out-starbucks-offers-f81f5bbfb2f5).

### Author <a name="author"></a>
 [Harsha Kumar](https://github.com/HarshaKumarKS)
