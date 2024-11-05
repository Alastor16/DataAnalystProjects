### overview
This project is based on analyzing a data base from a callcenter. 
Target of the analysis: the callcenter owners and managers. 
Objective: We want to learn which operators have a low performance. Delivery: an analysis of low performers, with an extension on how to define them and any information relevant to the case.
The dataset has the information on the client that made the call, the operator that answered (identified by their operator_id) and other relevant data such as if the called was amissed call, the duration of the calls, and the wait times.
Based on the objective we need to find the operators that have a low performance. For that part we need to define how we are measuring performance, what is the values that we are taking into account, and what are the thresholds for them. Then we can create a tag of high performer vs low performer. Once we have a dataset of low performer and high performers we can start to compare them so we can see if there is any pattern present in the low performers, or the high performers. Afterwards we will formulate hypothesis based on those patterns, and test them. The hypothesis must be tested because there can be false associations between the data and we want to pinpoint the reasons for the low performers.
## tools used
Python, SNL

## 1. Pre procesing  of the data
We will check the data base, see if there is any null values or repeated values. in the data provided all columns are useful so we will try to keep them all. 
In this step we are going to clean the data, check for data types if needed and make some assumptions for future tests.
At the end of this step we will have a cleaned data set that we can work with. 

## 2. Pre analysis of the data
In this step we will check for average for each value in the columns, see if there are any correlations between them. Count the values and graph the overall behaviour of the operators, such as wait times, number of incoming calls, number of outgoing calls, if the calls are external or internal. We will check
The information from the pre analyzis will help streamline the check for the low performing operators.

## 3. Check for low performing operators 

We will check which operators are having a low performance. Low performance is defined by the next data

    1.High number of lost incoming  calls.
    We will evaluate by grouping the number of incoming calls in quartiles, the operators that fall on the Q1 will be defined as low performers. If the number is very high we will increase the number of quantiles. 
    2.Large wait times for incoming calls.
    We will check the wait times for incoming calls and separate them in quartiles, once again any operator in the Q1 will be defined as low performer. 
    3.if they need to make outgoing calls, a low number is also an indicator for this
    We will match the number of outgoing calls in order to check for the low performers. 
    
An important point is that an operator can fall into any of the above three categories. Depending on the preanalysis of the data we will check for the relevance of each and weight them against each other. Number 1 and 2 are the most important Measurment but the presence of 3 works to define an off case vs a low performer. 

Once we have the low performers for each value checked we will standarize them and create a tag on the dataset for them. 
IN this step we wil check for the thresholds for each value in order to avoid inconclusive data. We will graph the behaviours and check for the outliers in a normal curve 

## 4. Check patterns in the low performin operators 
Once we have isolated the low performing operators we will analyze the subset and compare it to the rest of the columns. 
In this step we want to check for patterns in the data, check fi there is any correlation between the values and the behaviour of the low performers. 
We will graph those patterns and generate hypothesis for the next step 

We have extra information besides the number of calls. Once we have defined three  groups, A- High performers (Q4), B- normal performers (Q2,Q3) and C- Low performers (Q1) we can compare them on the other metrics. Some examples of the possible correlations 

Time: We can check to see if the low performers are always attending at certain times of the day, this could indicate an issue with managment or the timeshift themselves( for example overnight shifts) 
Number of outgoing and incoming calls: We can check if the low performers have an abnormal number of outgoing calls or incoming calls compared to the rest. This could indicate that their performance is tied to certain values or conditions. 
Clients: We can check to see if the low performers are tied to specific clients accounts, this could indicate that those are problematic clients. 
Client start date and plan : similar to the client correlation above, we can see if the low performers are related to when did the client start the plan, or even the type of plan itself. If the low performers are related to a specific plan it could indicate issues on the plan. 

## 5. Hypothesis testing 

Once we have some patterns pin down on the data we will check on the hypothesis to compare them. The hypothesis wil allow us to see if the correlations are true and if they are relevant to the data for the client.  

# Conclusions 
🔍 Key findings : The low performers have an anormally long wait time but behave similar to the other operators. The lowperformers despite being less than 8% of the total operators handle the 27% of the total incoming calls which is correlated on the type of users. 

The key difference is that the member in tarif plan B or C have a higher prevalence in the operators that are classified as low performance. 

| 🤔 Impact of personal choices : In this project we choose the thresholds to define the low performers based on the graphs generated and removing the extreme outliers. If there are other elements needed to classify someone as low performer they weren't considered  

🚀 Limitations :

The study had the limitation of the available data. The following data could help improve the analysis 
	
1.The time of the call. We can see if the operators had any relationship with the time they take the calls, such as early morning calls. 
 2.More information on the type of call, the dataset presents all information as equal but a failed service call is different than a sales call, or a payment call. 
3.If the user had called before in the datetime it can help know if it happened in the same day and another operator took the call. The order of the calls could help elucidate the reason for the low performers.
4. Date of contract for the operators, the experience the operators have could also impact their ability to solve the calls in a quickly and efficient manner. 


📝 final coments:

The low performers have a higher rate of interaction with those in B and C tarif plans, there are some outliers in the number of calls a certain users makes but most call at around 200 times in the 4 months of the study while the ones engaged with the low performing operator had a median of 400 calls. 
