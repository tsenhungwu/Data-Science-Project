
<p align="middle">
  <img width="450" height="380" src="https://github.com/tsenhungwu/Data-Science-Project/blob/master/Finding%20Donors/Images/fundonor.png" />
  
# Introduction
Compared with relational databases ([My PostgreSQL Data Modeling Project](https://github.com/tsenhungwu/Data-Engineer-Project/tree/master/Isongs)) and NoSQL databases ([My Apache Cassandra Data Modeling Project](https://github.com/tsenhungwu/Data-Engineer-Project/tree/master/Isongs_Apache_Cassandra)), Data Warehouses implemented and hosted on a cloud-based platform (Amazon Web Services or AWS) have severl advantages:

The advantages of using AWS to build cloud-based data warehouses:
  - Lower barrier to enter (we don't buy stuff but rent!)
  - May add or change as we need
  - Scalability and elasticity out of the box (add and remove resources)


Now, a music streaming platform has grown its user base and song database, and thus moving its data on the cloud might be a good choice. Currently, data resides in AWS S3 in a directory of JSON logs on user activity on the platform, as well as a directory with JSON metadata on it.

Again, using AWS, we can still answer the specific questions proposed by the analytics team:  
  - What types of songs and artists are users listening to?
  - When is the most frequent time users logging into the app?
  - How long have users stayed on the app for each logging activity?

# Objectives
Throughout this project, I have achieved the following tasks:

- Built an ETL pipeline which extracts data from S3 bucket and stages data in Redshift.
- Optimized table design in Redshift to achieve a faster data ingestion process.
- Transformed data into a set of dimensional tables and fact table for continued analysis.


# Technology
<p align="middle">
  <img height="125" width="250" src="https://github.com/tsenhungwu/Data-Engineer-Project/blob/master/Isongs_AWS/Images/aws_redshift.png"/>
  <img height="200" width="300" src="https://github.com/tsenhungwu/Data-Engineer-Project/blob/master/Isongs_AWS/Images/aws_s3.png"/>
  <img height="150" width="250" src="https://github.com/tsenhungwu/Data-Engineer-Project/blob/master/Isongs_AWS/Images/aws_ec2.png"/>
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


