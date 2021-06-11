# Lead-Scoring-using-Supervised-Learning-Logistic-Regression
Build a logistic regression model to help an online education company improve its lead conversion rate. The model will help to assign a lead score to each of the leads which can be used by the company to target potential leads, such that the customers with with higher lead score have a higher conversion chance and the customers with lower lead score have a lower conversion chance. The target lead conversion rate to be increased from 30% to around 80%.

## Introduction

X Education is an education company that sells online courses to industry professionals. Many professionals who are interested in the courses land on their website and browse for courses. The company markets its courses on several websites and search engines like Google. Once these people land on the website, they might browse the courses or fill up a form for the course or watch some videos. When these people fill up a form providing their email address or phone number, they are classified to be a lead. Moreover, the company also gets leads through past referrals. Once these leads are acquired, employees from the sales team start making calls, writing emails, etc. Through this process, some of the leads get converted while most do not. The typical lead conversion rate at X education is around 30%, which is not a good number.

The company needs to improve their lead conversion score. The CEO, in particular, has given a ballpark of the target lead conversion rate to be around 80%. Therefore X Education wishes to analyse the data to identify the most potential leads, also known as ‘Hot Leads’, i.e. the leads that are most likely to convert into paying customers. They require a model to be built, wherein a lead score is assigned to each of the leads such that the customers with higher lead score have a higher conversion chance and the customers with lower lead score have a lower conversion chance. This will help to increase the over all conversion rates as well as help the sales team to focus more on communicating with the potential leads.

## Project Description
The data is cleaned, wrangled and then Exploratory Data Analysis & Outlier treatment is performed using python and its libraries. The relationship between the target variable and the input variables, and multicollinearity between different numeric variables is explored. Univariate and Bivariate analysis is performed, and dummy variables created for the categorical variables. To perform Data Modelling, the data is divided into Training and Testing data. The X (feature variables) and y (target variable) are determined and are scaled. Using RFE: Recursive feature elimination technique, selected the top 20 variables and a Logistic Regression Model is built using the RFE selected variables.

Then we drop one variable at a time.The general rule of thumb to be followed for dropping variables is in this order:

i) first drop the features with both high p-value(>0.05) and high VIF(>5)

If p-value and VIF are both not high (condition i is not satisfied) , then dropping preference is in the below order:

ii) the feature with high p-value and low VIF iii) the feature with high VIF and low p-value

When dropping on the basis of VIF, we do not always drop just on the basis of high VIF alone. We might also need to consider other aspects, that is, look at the EDA analysis to see how the target variable and dependent variable are related, and use domain knowldege to decide which variable to drop and which to retain. As we drop variables one at a time, the p-values and VIF of all the variables will change as we rebuild our model aafter every drop.

In the final model, all the variables have a p-value which is less than the significance level of 0.05, and a VIF lower than 5 (low multicollinearity). Next we proceeded with model prediction using our final model and calculation of various evaluation metrics.  From the different metrics we observed that the classification model is predicting well and as per our requirement. From the coefficients of our final model, we found the variables which contribute most towards the probability of a lead getting converted. Finally we assigned a lead score between 0 and 100 to each of the leads which can be used by the company to target potential leads. 

## Technologies Used
Python

Libraries: pandas, numpy, matplotlib, seaborn, sklearn, statsmodel, scipy

Jupyter Notebook

## Results
From the final model, the top variables contributing the most towards the probability of a lead getting converted, along with their coefficients are found. A lead score between 0 and 100 is assigned to each of the leads which can be used by the company to target potential leads. The sensitivity score of our final model is 85.5%, which is a good score. 
