## Executive Summary
The purpose of this project is to predict credit card approval by analyzing the impact of different fields on the approval for a credit card. Being able to predict what type of customer are likely to default on their payment comes in handy when dealing with approval of applicants of the credit card to avoid future risk. According to a data from the Federal Reserve Bank of New York, in the first quarter of 2021, the 90-day failure to make outstanding payment was 9.98% compare with 9.09% at the same time in 2020.
            The dataset for credit card approval for prediction was taken from Kaggle. Approval of application for the credit card depends on number of factors such as their credit payment status, their total income earned, age, year of employment and so on. Using all the required features and through the use of predictive analytics and machine learning, patterns and relationship among the variables were analyzed. To create a model, we used logistic regression, decision tree, random forest, support vector classifier, KNN and XGBoost.
            
## Background
Credit card issuing institutions are becoming meticulous in approving credit cards for customers. In addition, the downturn of financial institutions during the US subprime mortgage and the European sovereign crisis has raised concerns about risk management properly.  Hence, these challenges have attracted significant attention from researchers and practitioners. A wide range of statistical and machine learning techniques have been developed to solve credit card related problems. It is found that machine learning techniques are superior to other traditional statistical techniques in dealing with credit scoring.
The decision of approving a credit card or loan is majorly dependent on the personal and financial background of the applicant. There are two basic risks: one is a business loss that results from not approving the good candidate, and the other is the financial loss that results from approving the candidate who is at bad risk. It is very important to manage credit risk and handle challenges efficiently for credit decisions as it can have adverse effects on credit management. Therefore, evaluation of credit approval is significant before jumping to any granting decision.

## EDA Analysis
Here are examples of few graphs we created for EDA. The Status shows the binary values of either 1 or 0. 0 indicates that the applicant has paid their credit due on time or has no loan remaining. Whereas 1 indicates that they are behind on their payments. 

![image](https://user-images.githubusercontent.com/39715185/162340751-9d2a25df-cb6d-42da-8386-598601c2fdda.png)<br/>
The above graph shows that the applicants are not good candidates if Total income & years of Employment is less. 

![image](https://user-images.githubusercontent.com/39715185/162340784-4e981eda-db05-4114-8153-b30d3f815af5.png)<br/>
The above graph shows that, majority of applicants who have higher income are more likely to pay their due on time.  There is no correlation with age with their payments. We also analyzed the applicant’s distribution data, here are some results that we found:	
### Majority of applicant’s are married
![image](https://user-images.githubusercontent.com/39715185/162340805-3730e212-6f2a-4147-bc3a-4deb9c08b742.png)<br/>
### Majority of applicant's lives in House / Apartment
![image](https://user-images.githubusercontent.com/39715185/162340855-fc4820c9-682b-41c1-9b23-972b06cfb8a8.png)<br/>
### Majority of applicant's are 25- 65 years old                   
![image](https://user-images.githubusercontent.com/39715185/162340891-3f6a2c05-4689-4b49-8379-56311ae23c37.png)<br/>
### Majority of applicant's are Employed for 0 -7 years
![image](https://user-images.githubusercontent.com/39715185/162340916-1e8b0895-1733-4122-a7fc-086d6772d8c2.png)<br/>

### Correlation
Below we have the seaborn correlation heatmap which shows that the features are not highly correlated to each other. In addition to that, the features are also evenly split between positive and negative correlation between two variables. This graph also shows that there is no column (Feature) which is highly co-related with 'Status'
![image](https://user-images.githubusercontent.com/39715185/162340967-b4fde6f7-27de-4e36-b69b-d4e0eca4fbc8.png)

## Data Modelling: 
To prepare and apply a model to this dataset, we split the dataset into two subsets. The first is the training set on which we developed the model. The second is the test dataset which we used to test the accuracy of our model. We allocated 80% of the items to Training and 20% items to the Test set. 
For modeling we used Logistic regression, Decision tree, Random Forest, SVM, KNN and XGBoost models. Below is table which shows the accuracy based on used machine learning algorithm used.



<table>
  <thead>
    <tr>
      <th> Model </th>
      <th> Accuracy </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Logistic Model Accuracy</td>
      <td>50.60 %</td>
    </tr>
    <tr>
      <td>Decision Tree Model Accuracy</td>
      <td>69.55 %</td>
    </tr>
    <tr>
      <td>Accuracy Score</td>
      <td>99.94%</td>
    </tr>
    <tr>
      <td>Random Forest Model Accuracy</td>
      <td>76.00 %</td>
    </tr>
    <tr>
      <td>Support Vector Classifier Accuracy</td>
      <td>49.79 %</td>
    </tr>
    <tr>
      <td>KNN Model Accuracy</td>
      <td>45.98 %</td>
    </tr>
    <tr>
      <td>XGBoost Model Accuracy</td>
      <td>84.14 %</td>
    </tr>
  </tbody>
</table>


## Discussion/conclusion
<li>As the dataset is highly imbalanced, we have used SMOTE (Synthetic Minority Oversampling Technique) technique to understand which model performs better.</li>
<li> We took 2 passes at the Machine learning models, one with initial data and other with balanced data after performing SMOTE technique and the two results differed significantly. After applying all the Machine learning models on the balanced dataset, we got that XGBoost Model is giving the highest accuracy of 84.14 %. SMOTE Sampling methods provided much better results compared to raw data.</li>
<li>We will be refining our models and algorithms further in the coming weeks and if results remain the same then we will be choosing XGBoost as the preferred algorithm for any future credit card approval prediction. </li>
<li>For future work, the efficiency of the models can be improved if the dataset is larger, and balanced so, that the sampling method is not needed. If the original values of the dataset are known, then we can know how the data is correlated and which features are important and train accordingly. In the future different methods can be used to improve the results, more parameter tuning can be done.</li>

## References 
<li>Abbott, D. (2014). Applied Predictive Analytics: Principles and Techniques for the Professional Data Analyst (1st ed.). Wiley.
<li>Siegel, E. (2016). Predictive Analytics: The Power to Predict Who Will Click, Buy, Lie, or Die (Revised and Updated ed.). Wiley.
<li>Li, S. (2019, February 27). Building A Logistic Regression in Python, Step by Step. Medium. https://towardsdatascience.com/building-a-logistic-regression-in-python-step-by-step-becd4d56c9c8
<li>GeeksforGeeks. (n.d.). Python Programming Language. Retrieved October 2, 2021, from https://www.geeksforgeeks.org/python-programming-language/
<li>Credit Card Approval Prediction. (2020, March 24). Kaggle. https://www.kaggle.com/rikdifos/credit-card-approval-prediction
<li>Change column type in pandas. (2013, April 8). Stack Overflow. https://stackoverflow.com/questions/15891038/change-column-type-in-pandas
<li>Hongmei, ChenaYaoxin, Xianga,”The Study of Credit Scoring Model Based on Group Lasso”, Elseiver, Volume 122, 2017, Pages 677-684. 
<li>Ashlesha Vaidya, “Predictive and probabilistic approach using logistic regression: Application to prediction of loan approval”, ICCNT(2017), 10.1109/ICCCNT.2017.8203946 
            
            





[Other Projects](https://github.com/RamizuddinS/DS_Portfolio)
