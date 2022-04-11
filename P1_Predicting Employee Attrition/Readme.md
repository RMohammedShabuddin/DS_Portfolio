
<h2> Predicting Employee Attrition</h2>

## Business Problem
Employee attrition is one of the critical factors which affects the organization. Affecting the organization can be of different reasons which include employee knowledge is lost and can be taken to rival organizations. Some of the reasons which affect an organization less are job mismatch, retirement, etc. Attrition is not only the cost of losing the resources, but we also invest in training the newly hired resource. For organizations to be successful, it is essential that the employer and the employee have a good relationship. If the employee decides to leave the organization, there will be challenges the organization faces. It will impact productivity, revenue, experience, and time invested in training. So, we can use some of the machine learning techniques to predict the same. Thus, it is essential for an organization to understand why the employee is leaving them.

## Background/History
According to the FinancesOnline Review for Business, There are around 18.9 million Americans either exit the labor force or change occupation every year. Around 3.5 million workers quit their jobs at the beginning of 2020. The average turnover rate in the U.S. is about 20% annually. In February, the number of total separations initiated changed to 6.1 million and 4.1 percent. Attrition will cause a big issue for organizations both in-process and in cost. If an organization performs successfully, the organization and the employee should have a good relationship and understanding. When an employee decides to quit, there will be a lot of challenges for the organization. It will impact their productivity, revenue, experience, and time invested in training the employee. There is around $630Billion in overall costs of employee turnover in the US. The cost of replacing an employee who resigned is around 33% of the employee's annual salary. So, it is important for employers to understand why employees are leaving the company. Using the dataset from Kaggle to uncover the factors that lead to employee attrition and explore important questions such as ‘The time is taken to travel from home to work is a factor for attrition, Among critical factors, is Monthly income a factor to keep employees happy, Will the highly educated employees more tend to leave the organization, Work-life balance relates to employee retention. 

## EDA Analysis: 
Here are examples of few graphs created for EDA.
### Employee Attrition count 
![image](https://user-images.githubusercontent.com/39715185/162350015-49b69cf9-98cd-4b53-978b-801942296746.png)

### Employee Attrition Percentage

![image](https://user-images.githubusercontent.com/39715185/162659818-cfbf9c34-8664-42ad-986f-c59a2dbe7b9c.png)

### Years at Company vs Monthly Income
More people are likely to leave at early stage of the company or during there 10 years approx..
![image](https://user-images.githubusercontent.com/39715185/162659861-f7a957b6-db6e-458a-bc25-d99a7b93b373.png)

### Distance From Home vs Monthly income
![image](https://user-images.githubusercontent.com/39715185/162659918-9a7ab90c-76c0-4d7f-9c34-215589af7b6e.png)


### Age factor vs attrition count
People with age of 26 to 35 tend to leave the organization.
![image](https://user-images.githubusercontent.com/39715185/162350104-cea5d530-5781-4b2a-aafb-52a7a4c14d4e.png)

### Distance from home distribution by Attrition
The travel distance is more than 10miles from home, the employee is more likely to leave the company. 
![image](https://user-images.githubusercontent.com/39715185/162350164-1b99ac0d-b612-4dd2-a933-bb24c75833e5.png)

### Years at company distribution by Attrition
Employee under 4 years at company is more likely to leave the company
![image](https://user-images.githubusercontent.com/39715185/162350249-54b6d9a8-d245-49ed-af52-76cbd1da0233.png)

### Total Working experience by Attrition
Employee under 8 years of total work experience are more likely to leave the company
![image](https://user-images.githubusercontent.com/39715185/162350299-8b5726c6-4f62-4865-b937-b70b0fbfa6b1.png)

### Monthly income distribution (in %) by Attrition
Employees with a monthly income of less than 5,000 are more likely to leave the company.  
![image](https://user-images.githubusercontent.com/39715185/162350356-67f0b395-2b9c-4f60-88f2-7c078de5ddd3.png)

### EducactionField with highest attrition
The top 3 fields where the attrition is higher are HR, Technical Degree and Marketing.
![image](https://user-images.githubusercontent.com/39715185/162350405-9a645f6d-d0dd-415d-b234-a35ef683de23.png)

### Overtime vs attrition
Employees who do overtime are more likely to leave the company
![image](https://user-images.githubusercontent.com/39715185/162350469-600592b5-872e-43dd-92d0-1c23b9ec47ad.png)

## Models 
For modeling we used Logistic regression, Decision tree, Random Forest and SGDClassifier models. Below is table which shows the accuracy based on used machine learning algorithm used.<BR>
![image](https://user-images.githubusercontent.com/39715185/162350589-4460112f-75db-4913-be19-8af465db325b.png)<BR>
Logistic Regression is selected for further performance tuning. Logistic Regression model is tuned with hyper parameters using Grid Search CV. The Grid SearchCV on Logistic Regression classifier increased the ROC-AUC score to 81%. 

## Conclusion
The employees are the backbone of the organization. If the employee leaves, he takes away most of the stuff. Which includes domain expertise and knowledge.  For an organization, it is important to understand the causes of employee attrition. It would be better to have the attrition rate below the acceptable threshold. With the help of machine learning algorithms, employers will be able to predict employees who are at risk of leaving the company and attempt to retain them, and also determine the factors that lead to employee attrition. I believe ingesting more data into a machine learning model will help us get better results from what we have achieved here in our research.


