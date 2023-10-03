# Practical-Application-1
Will customers accept coupons sent to their smartphones?

## Problem Statement: Smartphone Coupons
The following analysis focuses on visualizing and identifying differences between people who accepted coupons sent to their smartphones and those who rejected the coupons. Two types of coupons were investigated: bar coupons and takeaway food coupons. The following factors were considered: monthly bar attendance rates, monthly food takeout rates, coupon expiration time, age, occupation, destination, type of passenger, income, education, time of day, and gender.  Please also see the Jupyter notebook for more details including the actual Python code. 

## Background: Will a Customer Accept the Coupon?
Imagine driving through town and a coupon is delivered to your smartphone for a restaurant near where you are driving. Would you accept that coupon and take a short detour to the restaurant? Would you accept the coupon but use it on a subsequent trip? Would you ignore the coupon entirely? What if the coupon was for a bar instead of a restaurant? What about a coffee house? Would you accept a bar coupon with a minor passenger in the car? What about if it was just you and your partner in the car? Would weather impact the rate of acceptance? What about the time of day?
Obviously, proximity to the business is a factor on whether the coupon is delivered to the driver or not, but what are the factors that determine whether a driver accepts the coupon once it is delivered to them? How would you determine whether a driver is likely to accept a coupon?

## Data
This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the driver whether he or she will accept the coupon. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’. There are five different types of coupons -- less expensive restaurants (under $20), coffee houses, carry out & take away, bar, and more expensive restaurants ($20 - $50).

## Summary: Key Findings and Recommendations for Next Steps
### Bar Coupon Acceptance
The bar coupon acceptance rate increases strongly with high bar attendance; drivers who go to the bar 4-8 times or more per month have a very high acceptance rate of 77%. Also, drivers who go to the bar at least once a month generally have high acceptance rates of 70% or more, provided that they are less than 30 years old, or have passengers who are not kids. Drivers who often attend bars seem rather price-sensitive since they make sure to use their coupons. Next step should be to investigate what factors could encourage people who never, or rarely, go to the bar, by analyzing and better understanding people in these categories who did accept their bar coupons. 

### Takeaway Food Coupon Acceptance
Very high coupon acceptance rates of around 80% to 90% were found for takeaway coupons with 1-day expiration times when delivered to customers who regularly take out food 1-8 times a month, are in their twenties, go to non-urgent places, are alone, either unemployed or students, and in early evenings around 6 pm. Targeting customers who meet a combination of the above attributes can even reach a coupon acceptance rate of 100% in certain conditions.

However, simply giving coupons to customers who already take out your food products and are happily paying the full price could deteriorate your profit margin by providing discounts to customers who would buy your products anyway.

Therefore, a more restrictive and targeted strategy is needed. For example, you could focus on addressing and growing new customer segments that currently do not buy much of your products, such as targeting your coupons to people who never, or rarely take out foods, or offering lunch coupons to those who usually take out dinner meals. Also, you could offer coupons that meet the preferences of both drivers and their passengers to grow your business beyond customers driving alone, or target employees who need lunch or dinner at work rather than going after the majority of customers who go to non-urgent places. 

## Visualizations, observations, and interpretations. Differences between those who accepted and rejected their coupons
### Bar Coupons
![Bar attendance](https://github.com/fredrik-pettersson/Practical-Application-1/assets/146313002/cd954d37-e261-468b-b691-a6483786e63c)


The less often people go to bars, the more likeley they are to reject their bar coupons. Conversely, the more often they go to bars, the likelier they are to accept their coupons. 


![High bar attendance income](https://github.com/fredrik-pettersson/Practical-Application-1/assets/146313002/31a3b954-1c23-4d80-8ff3-c84c6a87492e)

The acceptance rates are very high for people who attend bars more than three times a month, especially in the $37.5k to $50k income group. While people in this group seem to make enough money to frequently attend bars, they are still price-sensitive and value the coupon discount. Interestingly, coupon acceptance is also very high in the $100k+ income group, which would be something to investigate as a next step.     



### Takeout Food Coupons
#### Monthly Takeout Rates
![CarryAway rate](https://github.com/fredrik-pettersson/Practical-Application-1/assets/146313002/180ac9ce-fc44-4c4c-8624-44f00fa5a8e9)

People who take out food between 1 to 8 times a month drive more than 70% of all accepted takeout coupons (yellow bars denote coupons that were accepted, and blue bars denote coupons that were rejected). On the other hand, people who never take out food accept very few coupons in absolute numbers. This is similar to the bar coupons in the previous section; those who attend bars frequently are more likely to accept bar coupons while those who never attend bars are less likely to accept bar coupons.   



#### Expiration Time
![Expiration](https://github.com/fredrik-pettersson/Practical-Application-1/assets/146313002/776da186-7f89-4a6b-a996-1873f11f3e3f)

There is a clear tendency to accept coupons with a 1-day expiration time over those with a 2-hour expiration time, while there is no difference among those who rejected the coupons (in blue). Offering 1-day expiration coupons gives customers more flexibility and time to plan their purchases which seem to increase coupon acceptance. 



#### Age
![Age](https://github.com/fredrik-pettersson/Practical-Application-1/assets/146313002/9dbb2648-4a80-4f8b-97fb-228a35c6fb17)

People in their twenties accept about 40% of all coupons and is thereby the age group that accepts most coupons. Within that group, those aged 21-26 years tend to have a somewhat higher acceptance rate and a lower rejection rate than those aged 26-31 years. A potential explanation is that the twenties age group may be more outgoing and have less money to spend and are therefore more likely to accept coupons. People under 21 years old tend to accept the least number of coupons, probably because of limited spending in general. 



#### Occupation
![Occupation](https://github.com/fredrik-pettersson/Practical-Application-1/assets/146313002/deb8457e-7b32-4dd4-8af9-ae530b402528)

The unemployed and students are the two occupational groups that accept the most coupons (about a quarter of all coupons) with the unemployed having somewhat higher acceptance rates and lower rejection rates than students. Retired people tend to accept the least number of coupons. Also, retirees and people in Arts Design Entertainment Sports & Media tend to have higher rejection rates and lower acceptance rates than people in Business & Financial. 



#### Destination
![Destination](https://github.com/fredrik-pettersson/Practical-Application-1/assets/146313002/af94a3eb-d9e4-473d-9739-360cf4672834)

People who take out food and go to a non-urgent place accept more than 40% of all coupons. Those who go to work tend to have the lowest acceptance rates and highest rejection rates of all segments. The reason for this might be that those going to a non-urgent place have more flexibility and time, while those at work are more constrained and have limited time. 



#### Passengers
![Passenger](https://github.com/fredrik-pettersson/Practical-Application-1/assets/146313002/96da835a-5509-4f23-acbd-8b7dff57ae3e)

Drivers who were alone accepted close to 60% of all coupons. Drivers with kids or partners accepted the least number of coupons. Drivers who are alone might have more freedom to select exactly the coupon they like without having to compromise with anyone else, and this might contribute to more accepted coupons.  



#### Income
![Income](https://github.com/fredrik-pettersson/Practical-Application-1/assets/146313002/975a9999-0ba3-4e4c-843e-ff5e849cc0ff)

More than 30% of coupons are accepted by people making between $12.5k and $37.5k, where the segment making $25k-$37.5k tends to have higher acceptance rates and lower rejection rates compared to those making $12.5k=$25k. These income segments are at the lower end and people in these segments might be more likely to accept coupons due to being more price-sensitive in general. The highest coupon rejection rate is found in the $100k or more segment, which might reflect a lower level of price-sensitivity for people making more than $100k per year.  



#### Education
![Education](https://github.com/fredrik-pettersson/Practical-Application-1/assets/146313002/b3cee409-e98a-42be-9501-7951bffa9089)

Those with some college – no degree or a bachelor’s degree accepted close to 70% of all coupons.  Those with some college – no degree also have a higher acceptance rate and a lower rejection rate compared to those with a bachelor's degree.  One possible explanation could be that those with some college – no degree might earn somewhat less than those with a bachelor's degree and are therefore more price sensitive and more open to accept coupons. 



#### Time of Day
![Time of Day](https://github.com/fredrik-pettersson/Practical-Application-1/assets/146313002/2baf72ed-3230-4588-8382-e8d6ff6fa17d)

The time period with the largest difference between accepted and rejected coupons is 6 pm. People taking out food at 6 pm tend to have higher acceptance rates than those taking out food at 10 am or 10 pm, probably because 6 pm is a common time to have dinner. 



#### Gender
![Gender](https://github.com/fredrik-pettersson/Practical-Application-1/assets/146313002/2dbd25f5-ad6c-485b-ad76-f2a2c84894c3)

Females and males accept about the same number of coupons, but females tend to reject coupons (in blue) at a somewhat higher rate than males.



#### Analysis on acceptance rates 
The following table summarizes the takeaway coupon acceptance rates for different combinations of customer attributes (see Python code for additional details):
![Table](https://github.com/fredrik-pettersson/Practical-Application-1/assets/146313002/80e52ce5-4d9f-4662-8c0e-427a21cfbd09)



### Next steps and recommendations
If the objective is simply to maximize the acceptance rate of takeout coupons, then providing coupons with 1-day expiration times (or possibly longer) to customers who regularly take out food 1-8 times a month, are in their twenties, go to non-urgent places, are alone, either unemployed or students, and at around 6 pm will likely result in high acceptance rates. 

However, this approach would be too simplistic. The risk is that you will be giving coupons to people who aready take out food and are willing to pay the full price in any case, thus deteriorating your profit margin by unnecessarily discounting your products to people who are willing to buy without discounts.

Therefore, a more restrictive strategy is needed. For example, you could focus on growing customer segments that currently do not buy much of your products, such as targeting your coupons to people who never, or rarely take out foods, or offering lunch coupons to those who usually only take out meals for dinner. Also, you could offer coupons that meet the preferences of both drivers and their passengers to grow your business outside of customers who are alone, or target employees who need lunch or dinner at work rather than the majority of customers who go to non-urgent places.

