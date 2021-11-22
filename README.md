# Employee-Attrition-

Problem Statement
You are working as a data scientist with HR Department of a large insurance company focused on sales team attrition. Insurance sales teams help insurance companies generate new business by contacting potential customers and selling one or more types of insurance. The department generally sees high attrition and thus staffing becomes a crucial aspect.

To aid staffing, you are provided with the monthly information for a segment of employees for 2016 and 2017 and tasked to predict whether a current employee will be leaving the organization in the upcoming two quarters (01 Jan 2018 - 01 July 2018) or not, given:

Demographics of the employee (city, age, gender etc.) Tenure information (joining date, Last Date) Historical data regarding the performance of the employee (Quarterly rating, Monthly business acquired, designation, salary)



Approach
Following data is about an organization that is concerned about its staffing. Losing employees frequently impacts the morale of the organization and hiring new employees is more expensive than retaining existing ones. Some factors regarding to the monthly performance, quarterly ratings, salary etc. are given in this dataset so as to acknowledge a behavior pattern within the employees that affects them and eventually leads them to make a decision whether to leave the organization or not.

The very first step is that the target variable is not specifically mentioned in the train data. For constructing the target variable as shown in the definition, one should first look at the ‘LastWorkingDate’ column. Wherever the column has null values, that means the employee is continuing his/her work at the organization at least in the next year. Wherever any date record is appearing, that means the employee has left the organization on that particular date. So as per definition, we will put 0 where LWD column is null and 1 where LWD column has a date.

After that I have applied some data preprocessing techniques such as grouping, scaling, encoding etc. and try several supervised machine learning models. Whichever model gives the best accuracy as per the data we are feeding in the model, I have used that for predicting our test data.

The test data contains only the employee ids. Thus, for taking the performance and demographics of employees, I havd to perform inner join function between test and train to get those parameters in the same order as it is arranged in test data. After that we will predict the status of employees as per the performance parameters. At the end I have put that in the submission file and finally upload the solution.


