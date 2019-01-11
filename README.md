# Data-Science-Project
Hi! My name is Tsen-Hung Wu. I have complied all my hard works in school projects in the Data Science Project.

 <p align="middle">
  <img height="200" width="300" src="https://github.com/xbellyx/Data-Science-Project/blob/master/Yelp%20Data%20Challenge/Yelp_image.jpg" /> 
  <img height="200" width="300" src="https://github.com/xbellyx/Data-Science-Project/blob/master/Lending%20Club/Lending_Club_image.jpg" /> 
</p>
<p align="middle">
<img height="100" width="400" src="https://github.com/tsenhungwu/Data-Science-Project/blob/master/Deep%20Learning%20Quora/Quora_image.jpg" />
</p>

## Motivation
Each data science project is unique and has different problems that needed to solve. I found doing data science projects are interesting and encourages me to achieve valuable goals for organizations. As a continuous learner, I keep accumulating the knowledge and the practical experience across projects.

## Project Titles and Descriptions
1. Bank Marketing Campaigns - How to attract more customers to subscribe term deposits?

(1) Addressed an unbalance label issue using SMOTE, an efficient over-sampling technique.

(2) Completed a model comparison experiment among nine machine learning models.

(3) Optimized hyperparameters of each model by Bayesian Optimization.

(4) 97% AUC was achieved on the test data by the validated Gradient Boosting. 

(5) Feature importance results were compared and interpreted between statistical hypothesis testings and model outputs.

2. Yelp Data Challenge – Sentiment Analysis and Recommender System

    •   Through this project, I solved two main problems:
    
    (1) Classified negative and positive reviews by a self-defined metric. After the model fitting, gained insights about 
        what words usually contribute to the negative or positive review. A restaurant can summarize what's the main 
        aspect such as food or service that resulted in a lower rating.
            
    (2) Used unsupervised learning to cluster users into groups. Identified and understood the common user preference 
        within each of the group by inspecting the cluster centroids. Built a restaurant recommender system using 
        collaborative filtering and matrix factorization based on users’ past visits and ratings.

3. Lending Club Data Challenge - Loan repayment ability and risk adjusted interest rate predictions”
    
    •   Main tasks have accomplished under this project: 
    
    (1) Imputed missing data, and dealt date-time data with feature engineering.
    
    (2) Performed feature selection through exploratory analysis and statistical testings such as two sample t-test and 
        chi-square test.
    
    (3) Applied machine learning algorithms including Regularized Logistic Regression, Random Forest, and Gradient Boosting 
        Decision Tree to predict a corresponding loan status and grade for each loan applicant.
        
    (4) Predicted an interest rate for each loan application using regression models containing Bagged Decision Tree 
        Regressor, Random Forest Regressor, and Gradient Boosting Regressor.

    (5) Compared classification models by AUC and accuracy scores, and regression models by mean squared error and R-square.
    
    (6) Hyper-parameter tuning on models to achieve the optimal performance based on the predefined objective.
    
    • Four response variables are predicted and the results were summarized as four tables: 
    
    (1) loan_status_binary: A binary classification problem, whether a loan application is "Default" or not. 
    
    Model | AUC | Accuracy | Precision
     ---  | --- | --- | --- 
    Logistic Regression | 0.9561 | 0.9923 | 0.7979 
    Random Forest | 0.9713 | **0.9924** | 0.7755
    GBDT | **0.9735** | 0.9913 | **0.8367**
    
    (2) loan_status: A multi-classification problem. Labels are 'Current', 'Fully Paid', 'Late (31-120 days)', 'Charged Off',
       'Late (16-30 days)', and 'In Grace Period'.
       
    Model | Accuracy (All labels)
     ---  | --- 
    Logistic Regression | 0.9879
    Random Forest | **0.9880**
    GBDT | 0.9866
    
    (3) grade: A multi-classification problem. Labels from grade A (best) to grade G (least).
    
    Model | Accuracy | Accuracy (from grade D to G)
     ---  | --- | --- 
    Logistic Regression | 0.8006 | 0.7979
    Random Forest | 0.9109 | 0.7755
    GBDT | **0.9564** | **0.8367**
    
    (4) int_rate: A continuous prediction or a regression problem.
    
    Model | MSE | R-squared
     ---  | --- | --- 
    Bagged Decision Tree Regression| 1.31 | 0.94
    Random Forest Regression | 2.51 | 0.89
    GB Regression | **0.73** | **0.97**

4. Quora Automated Q&A about Bitcoin - question matchings and answer recommendations

    • Used web scraping techniques to collect unstructured text data including labels, full contents of answers, upvotes, 
      questions from the Quora website.
      
    • Performed Exploratory Data Analysis (EDA) on raw data to receive important insights that might be beneficial to the 
      following tasks.  
      
    • Identified duplicate questions and saved searching time for askers on Quora through our designed search engine.
    • Classified labels for each question using Linear SVC classifier.
    
    • Compared Vector Space Model, Support Vector Machine, Random Forest, and Convolutional Neural Network (89% accuracy) 
      model performances under the task of question matchings and answer recommendations.
      
    • Provided the most reliable answer to the asker given a question via CNN.
    
    • Tuned hyperparameters of models to attain the optimal prediction.
