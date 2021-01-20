# **The Young and the Credit-less**

Project 2 by Lauren Tayara, Robert Troutman, Becca Gerdon, Surafel Gebre-Yesus and Christina Sullivan


### *Project Research Question*
How do we create a model that helps institutions avoid risk of young loan applicants yet allows the young applicants the opportunity to gain credit?

Our group chose this question to bring attention to the little knowledge that young loan applicants have. Based on our findings in our models we explore:
Which age group is the least likely to apply for loans?
Which group is most likely to default on loans?


### *Machine Learning Model*
This project uses a dataset from kaggle.com containing information on lending application information including applicant age, income, homeownership status, length of employment, loan intent, grade, amount, interest rate, status (default or no default), percent income, default on file, and credit history length. The dataset was used to create a binary classification model using a deep neural network to determine loan approval, focusing on the younger demographic. This model contained 11 numerical variables, some of which were string variables that had to be converted to binary, giving us 26 variables total, in order to build the best model. 


### *Data Preparation and Model Training Process*
First, we read in the data we retrieved from Kaggle and dropped all null values in the dataset. Then, using the Pandas' get_dummies feature, we were able to convert any string variables into binary allowing the data to be used to build a model. After selecting our X and y, we then trained our data, scaled/fit data, and transformed data, in order to build our model. Using Tensorflow we  made an LSTM model with a dropout percentage, to randomly drop 20% of the units on each epoch. Finally, we compiled and trained the model.


### *Techniques Used to Evaluate Model*
We created plots to visualize how different factors affected loan status:
- Age groups
* And what is the ratio of good loans to bad loans for the age groups
- Homeownership status
- Loan Intent
- Previous default on loan or not


### *StatsModel*
Considered as the R of Python, OLS MODEL (Ordinary List  Square) a type of model used to estimate the unknown parameter in a linear regression model, helps to minimize the difference between observed and predicted values. The t-score is a ratio between the difference between two groups and the difference within the groups. The larger the t score, the more difference there is between groups. The smaller the t score, the more similarity there is between groups (OUR SCORE -3.095). R-squared reflects the fit of the model. R-squared values range from 0 to 1, where a higher value generally indicates a better fit, assuming certain conditions are met (OUR SCORE  .00). The Const coefficient is the Y-intercept. It means that if both the person age and loan status coefficients are zero, then the expected output (i.e., the Y) would be equal to the const coefficient. Interest_Rate coefficient represents the change in the output Y due to a change of one unit in the interest rate (everything else held constant).


### *Findings and Summary*
The LSTM showed 92.2% accuracy for predicting loan status and had a 22.5% loss. Out of all of the age groups 25 and under is the least likely to apply for loans (besides 55 and over, who would be the least at then end of their careers). This group is also most likely to default on loans. Although the 25-40 age group clearly had the most applicants the under 25 category was more likely to default with 23.2% (25-40 had 20.9%).


### *Implications*
The findings from this research model lead us to further questions. Why don’t people from this group take out more loans? Why are they more likely to default on loans? Is there something lenders can do to help this group build credit? Are there other factors that lenders could use to determine whether to give loans or not? One thing we can do to help this age group is to provide more education on credit and loans.


### *QnA Bot*
In order to help this group, using AWS QnA Bot, we created a tool that is aimed to test the user’s credit knowledge, provide some extra information, and give them a score at the end. We input a question, a correct answer, and three incorrect answers for the user to choose from. Once the user selects an answer, the bot tells them whether they were correct or not and if not it shows the correct answer. We intended for this to be helpful for younger individuals and also other age groups to learn about what credit is and how they can improve their score.
[Visit the Credit QnA Bot here](https://jpya3ma0d8.execute-api.us-west-2.amazonaws.com/prod/static/client.html)


#### *Sources*
[Applying for a Loan](https://www.consumerfinance.gov/ask-cfpb/what-information-do-i-have-to-provide-a-lender-in-order-to-receive-a-loan-estimate-en-1987/)
[Machine Learning Libraries](https://blog.bitsrc.io/top-5-javascript-machine-learning-libraries-604e52acb548)
[Lending Tree](https://www.lendingtree.com/personal/personal-loans-statistics/)
[Data World](https://data.world/nerb/sba-loan-guarantee-data)
[LEnding Club Statistics](https://www.lendingclub.com/info/statistics.action) 
[Microlending](https://data.world/cityofchicago/chicago-microlending-institute-cmi-microloans)
[NY Open Data](https://data.world/data-ny-gov/22ew-dxez)
[Avergae Debt by Age](https://www.cnbc.com/select/average-american-debt-by-age)
