# Criteo-Click-Through-Rate-Prediction
Apply Spark steaming and Spark ML Logistic Regression model to predict click through rate of advertisement 

#### Project team: Chloe Wu, Curtis Lin, Eddie Zhu, Kai Qi Lim

---

### Programming Language and Packages
- Python 3.6
- Spark 2.4.4 
- Spark ML
- Spark MLlib
- Spark SQL

### Platform
- Google Colab
- Google Cloud (GCP)

### Motivation and Dataset
- Marketing campaigns cost money. It is of every company's business interest to launch a targeted and effective marketing campaign. An important metric to gauge the performance of each digital advertisement is click through rate (CTR), which is a ratio to show "how often people who see your ad end up clicking it" (1). Therefore, the purpose of this project is to establish a model to accurately predict CTR, and more importantly, a model with scalability to be applied to large volume of data. It will help companies to improve the effectiveness of their digital marketing campaigns, and to maximize their ROI.

- Specifically, the question we want to answer is: based on a set of features, would the advertisement be clicked? Our dataset is obtained through Kaggle Display Advertising Challenge launched by CriteoLabs back in 2014. We downloaded train.csv (with a size of approximately **12 GB**) from Criteo (2). In this csv file, each row corresponds to a display ad served by Criteo, with target variable as the first column:
*1 for clicked*, and *0 for non-clicked*, and the rest being feature variables: I1 to I13: *A total of 13 columns of integer features*. C1 to C26: *A total of 26 columns of categorical features*. The values of these features have been hashed onto 32 bits for anonymization purposes.

### Analysis Strategies
- first split full data in train.csv into our training (80%) and testing data (20%); within the training dataset, we randomly sample 1,000 records to be our toy dataset;
- conduct EDA on our toy dataset;
- select a model based off the takeaways from our EDA;
- explain the mathematical theory behind Logistic Regression model; 
- to clearly articulate the mathematical mechanisms behind Logistic Regression model, we build a homegrown Logistic Regression model, create a mini toy dataset, and apply the homegrown model to our mini toy dataset;
- apply multiple techniques of feature engineering on our toy dataset (1,000 records);
- establish a Spark ML Logistic Regression model and apply to the toy dataset and eventually the full dataset;
- evaluate our model performance by calculating its accuracy and log loss;