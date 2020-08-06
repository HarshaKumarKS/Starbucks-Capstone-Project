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


The dataset has the simulated data which mimics the behaviour of the customer using  Starbucks rewards mobile app. An offer may be simply a commercial for a drink or a real provide including a reduction or BOGO (buy one get one free) or just an informational provide which has the product information. A few customers probably won’t get any offers during specific weeks. So, Starbucks can most likely increase the likelihood that the customer opens the offer claim it. By reminding them of the latest information on the product and help to improve customer loyalty.

Challange here is that, not all customers receive the same offer. 

### Project Motivation <a name="project-motivation"></a>
Dataset is obtained from the program which creates data and simulates the way of customers purchasing decisions and analyse how those particular decision is motivated by the offers given. Our aim is to build a recommendation engine which recommends which offer Starbucks to be sent to a particular customer by answering the following questions,

We are interested to answer the following two questions:

1. Which offer should be sent to a particular customer to let the customer buy more?
2. Which demographic groups respond best to which offer type?


### Data Preparation <a name="data-preparation"></a>
There are 3 datasets provided and for further analysis each dataset is cleaned and preprocessed. The target features for analysis are offer_success, percent_success.

1. Portfolio - Column “Id” was renamed to “offer_id” and columns “Channels” and “offer_type” were one-hot encoded.
2. Profile - Column “Id” was renamed to “customer_id”, “Age” value 118 is replaced to NaN, Readable date format created in “became_member_on” column, rows with no income, age and gender data are dropped.
3. Transcript - Column “person” was renamed to “customer_id”, different columns for “amount” and “offer_id” created using “value” column, in the rows where “customer_id” is not present in “profile:customer_id” is dropped.

### File Descriptions <a name="files"></a>
1. data:

- portfolio.json: Metadata about each offers and their offer ID’s -10 rows x 6 columns
- profile.json : Each customer demographic data — 17000 rows x 5 columns
- transcript.json: Transaction records, received, viewed and completed offers — 306534 x 4 columns.
2. Starbucks_Capstone_notebook.* : contains notebook file.

### Results<a name="results"></a>
The main observations of the code are published [here](https://medium.com/@harsha.kumar3/a-smarter-way-to-send-out-starbucks-offers-f81f5bbfb2f5).

### Author <a name="author"></a>
 [Harsha Kumar](https://github.com/HarshaKumarKS)
