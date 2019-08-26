# sparkify: Big Data analysis using pyspark 

Sparkify is a music streaming service just as Spotify and Pandora. In this project Spark MLlib is used to build a machine learning model using pyspark.The dataset consist of log data for user usage of sparkify system. The target of the classification model is to predict churn, whick happens for both paid and free users. The system should be able to predict if a specific user will choose to cancel his registration. The analysis is preformed on a small dataset and run locally on the machine. To train the full dataset the program should be run using a cloud service such as AWS which is not implemented here. 

# Motivation
The motivation behind this project is to learn to use Apache Spark for data analysis and building models for big data. I wanted to add to my data science skills the ability to analyse and work with big data. Apache Spark is a very popular framework, and very powerful, a data scientist can accomplish alot using this framework.
Moreover the project tackels a very important business problem; predictin when a user churn can happen helps businesses to take prevented measures, such as sending new offers for users or making discounts. Making good predictions can save busnisses alot of money.

# Files
The following files can be downloaded to start working on the project:
- sparkify.ipynb: jupyter notebook containing the data analysis and the training.
- sparkify.html: html version of the notebook
- sparkify.pdf: pdf version of the notebook

# Librarie used in the project
- pyspark.sql
- pyspark.sql.functions
- pyspark.sql.types
- pyspark.ml
- pyspark.ml.feature
- pyspark.ml.classification
- pyspark.ml.evaluation
- pyspark.ml.tuning
- numpy
- pandas
- matplotlib.pyplot
- seaborn as sns

# Methodolgy
In order to build the machine learning model first a spark Session is created, and the data is loaded from a file into a pyspark dataframe. The the data engineeering process started. The data was cleaned from null values then exploratory data analysis was conducted to have a bettern understanding for the dataset and the relation between the input features. In the original dataframe each user has many rows each is a log for a user activity. For building the model a new dataframe is build with each user has only one row with aggregate data extracted from the user log and a new column was added the indicate if the user churned or not. to traing and fit the model a pipeline is created and the Random forest classifier is used since its a classification problem for churn or not. 

# Results
The Random Forest Classifier could proedit churn on the test dataset with excellent accurecy and the f1-score was around 96%. The model consisted of a good number of features that extracted as much relevant data to the problem in hand as possible. Which helped to build a useful model for churn prediction.  

#Blog Post
To read a blog post about the project please check the following blog post: [Spark for Predicting Users Churn](https://medium.com/@laraquadan/spark-for-predicting-users-churn-c93dc0ee9de6)

# Aknowledgment
This project is a capstone project of Udacity Data Science Nanodegree program. Special thanks to all Udacity team, for the work on this Nanodegree program. They push you to learn and grow with every lesson and project. For this project the Apache spark course by Udacity was a great help.
