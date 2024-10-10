# Machine-Learning-projects

The data coupons.csv gives an insight into different factors contirbuting towards making the decision of whether to accept the coupon or not.
These factors are behavioral, demographical and contextual in nature.

Key Attributes:
The dataset captures a wide range of variables that provide context for each coupon offer:

Demographic Information:

Columns such as age, gender, education, income, and maritalStatus provide details on the demographic background of individuals receiving the coupons.
Behavioral Information:

Variables like Bar, CoffeeHouse, RestaurantLessThan20, and CarryAway represent the frequency with which individuals visit these establishments.
Contextual Information:

Contextual features such as weather, time, passanger (who the person is traveling with), and direction (the direction of travel relative to the coupon location) provide additional context for when and where the coupon was offered.
Coupon Acceptance:

The Y column is a binary indicator (0 or 1) that specifies whether the coupon was accepted (1) or not (0). This is the primary target variable for analysis.


Before beginning the analysis, it is essential to identify and remove any data that does not contribute meaningfully to the decision-making process. This step, known as data cleaning or preprocessing.
We are going to do this by traversing through the columns and 
finding out which features have missing values greate than 1 and then compare them 


![image](https://github.com/user-attachments/assets/d4956318-4830-4019-8670-d44bd5890de6)







Based on the image above we can conclude that the car feature has the maximum number of missing values, hence we could ignore this features, as this doens't seem to contribute towards the decision making of whether to accept the coupon or not, hence we choose to not include it in our analysis, since rest of the features/ cloumns are non categorical or non numerical we use mode value of their respective data and replace the missing value with that. 


Analysis of different coupons:

This helps to identify how many times each type of coupon (e.g., Restaurant(<20), Bar, Carry out & Take away) appears in the data, giving a sense of the dataset’s composition.


![image](https://github.com/user-attachments/assets/64e610a5-3325-4ae8-8606-1b6156af24ca)


Based on the above image it can be said that 

1) Some coupon types may have higher counts, indicating that they are more prevalent in the dataset.
For example, if Carry out & Take away has the highest count, it means that this type of coupon was offered more frequently in the study or survey.
2) "Carry out & Take away" may have the highest count, indicating it was the most frequently offered coupon in the dataset.
"Bar" coupons may have a lower count compared to others, suggesting they were less commonly offered.
3)A higher count for a particular coupon type means that there are more data points for that type, which could make the analysis for that coupon type more reliable.
If one coupon type is significantly underrepresented, any conclusions drawn for that type should be interpreted with caution.




Bar Coupon Analysis:

1) Frequent Bar-Goers who who visit bars more than 3 times a month have a significantly higher acceptance rate for bar coupons.
2) Younger individuals (under the age of 30) show a higher acceptance rate for bar coupons.
3) Drivers traveling with passengers who are not kids have a higher acceptance rate for bar coupons, suggesting that these promotions are more appealing in adult social contexts.
4) Individuals who earn less than 50K and visit cheaper restaurants frequently are less likely to accept bar coupons, indicating that these promotions may not align with their spending habits or preferences.


We also decided to analyze each column/feature and see which one of them had maximum acceptance as that would give us an overview regarding which factor has maximum contribution towards coupn acceptance.
The tope 5 contributors are 
1) Education
2) Bar
3) Occupation
4) CoffeeHouse
5) Restraunt20to50

![image](https://github.com/user-attachments/assets/81b20e7e-f353-4be4-b2c4-73e6d865ece1)


Out of this the feature having highest coupn acceptance rate is 'Some High School' value for Education feature.
Here is the plot for different values for Education feature and their rates of accepatnce

![image](https://github.com/user-attachments/assets/95feb9b4-fe3a-45e1-b396-0a9650585b7d)

Based on the results the High School Gradute students seem more likely to accept the coupons and the Graduate students seem to have a lower acceptance rate
This insight could help revist the marketing strategies to attract more Graduate students at the same time retaining the High School Graduate students.







