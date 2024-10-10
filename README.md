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


Analysis of different coupns 



![image](https://github.com/user-attachments/assets/64e610a5-3325-4ae8-8606-1b6156af24ca)


Based on the above image it can be said that 

1)The "Carry out & Take away" coupon type has the highest acceptance rate among all categories, indicating that this type of promotion is particularly effective. This suggests that people are more likely to accept take-away or carry-out offers, possibly due to convenience and quick meal options.
2) "Restaurant (<20)" also shows a relatively high acceptance rate. This could mean that people are responsive to promotions for affordable dining options.
3)The "Bar" and "Restaurant (20-50)" coupons have the lowest acceptance rates. This suggests that individuals may not be as interested in bar-related promotions or more expensive restaurant offers compared to other options.
4)"Coffee House" falls in the middle, with an acceptance rate that is neither too high nor too low. This may indicate moderate interest in coffee house promotions, depending on factors like time of day or lifestyle preferences.




Bar Coupon Analysis:

1) Frequent Bar-Goers who who visit bars more than 3 times a month have a significantly higher acceptance rate for bar coupons.
2) Younger individuals (under the age of 30) show a higher acceptance rate for bar coupons.
3) Drivers traveling with passengers who are not kids have a higher acceptance rate for bar coupons, suggesting that these promotions are more appealing in adult social contexts.
4) Individuals who earn less than 50K and visit cheaper restaurants frequently are less likely to accept bar coupons, indicating that these promotions may not align with their spending habits or preferences.


We also decided to analyze each column/feature and see which one of them had maximum acceptance as that would give us an overview regarding which factor has maximum contribution towards coupn acceptance 


