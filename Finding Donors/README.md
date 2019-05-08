
<p align="middle">
  <img width="450" height="380" src="https://github.com/tsenhungwu/Data-Science-Project/blob/master/Finding%20Donors/Images/fundonor.png" />
  
# Introduction
In this project, I used several supervised algorithms to accurately model individuals' income using data collected from the 1994 U.S. Census. I then chose the best candidate algorithm from preliminary results and further optimize this algorithm to best model the data. 

This sort of task can arise in a non-profit setting, where organizations survive on donations. Understanding an individual's income can help a non-profit better understand how large of a donation to request, or whether or not they should reach out to begin with.




# Objectives
Throughout this project, I have achieved the following tasks:

- Explored Data through visualizations.
- Data transformation on features having skew distribution.
- Constructed a model that accurately predicts whether an individual makes more than $50,000.
- Optimized model by Bayesian Optimization.
- Feature importance report


# Technology
<p align="middle">
  <img height="210" width="510" src="https://github.com/tsenhungwu/Data-Engineer-Project/blob/master/Isongs/Images/Python.png" />
</p>


# Raw Data Exploration
Data currently resides in the S3 bucket in a JSON format and it's divided into two domains, Log Data and Song Data.


Below, I took an example to demostrate a log file, such as '2018-11-12-events.json':

<img src="https://github.com/tsenhungwu/Data-Engineer-Project/blob/master/Isongs_AWS/Images/log-data.png"/> 

And, another example of a song file, such as 'TRAAABD128F429CF47.json':

<img src="https://github.com/tsenhungwu/Data-Engineer-Project/blob/master/Isongs/Images/song_data.png"/> 


# Key Methodology

## Schema Design

In order to answer the proposed questions, following dimension tables and a fact table were created: 

<p align="center">
  <img src="https://github.com/tsenhungwu/Data-Engineer-Project/blob/master/Isongs/Images/ERD.png"/>
</p>


# How does this project work?
To run the project successfully on a local machine, we need to have the following preparations:

**Step 1: Register an account in [AWS](https://aws.amazon.com/#)**

**Step 2: Create an IAM user in your AWS account, give it 'AdministratorAccess', and save your access and secret key**
- Notice that DO NOT share your Access key ID & Secret access key!!!

**Step 3: Create and modify your .cfg file (configuration file) to specify parameters for your Redshift cluster**

**Step 4: Create an IAM Role and construct a Redshift cluster in AWS_setting.ipynb**

**Step 5: Inside the terminal, type followings line by line**
```
python kevin_aws_create_tables.py 
```
- It will create staging tables copying data from S3 bucket, and form dimension and fact tables fitted for the predefined Star schema.
```
python kevin_aws_etl.py
```
- Insert corresponding records from staging tables into dimension and fact tables.

**Step 6: Finally, open kevin_aws_testing.ipynb to test whether tables created properly.**


