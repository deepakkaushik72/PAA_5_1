Title: Drivers Coupon Acceptance Rate Analysis

Link to Readme file: https://github.com/deepakkaushik72/PAA_5_1/edit/main/README.md

Link to Code (ipynb file): https://github.com/deepakkaushik72/PAA_5_1/blob/main/prompt.ipynb

Overview

This data was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios, including the destination, current time, weather, and passenger, and then asks people whether they will accept the coupon if they are the driver. There are three possible answers people can choose from:
1.	“Right away” (Response Y=1)
2.	“Later, before the coupon expires” (Response Y=1)
3.	“No, I do not want the coupon” (Response Y=0)

Objective / Problem Statement

The objective of the Project is: 
1.	Recommend which customers to target to improve Bar Coupon acceptance rate which stands at 41% (lowest across coupon categories)
2.	Use Data Analysis and visualizations to distinguish between customers who accepted a driving coupon versus those who did not.
3.	Recommend Customers to target and improve the “Coupon Acceptance rate” across coupon categories.

Data / Tools and Technologies
       
   Data
   
   1.	Data Source: UCI Machine Learning Repository
   2.	5 different types of coupons: Less expensive restaurants (under $20), coffee houses, carryout and takeaway, bars, and more expensive restaurants ($20–$50).
   3.	Data set has 12684 records for each customer the Survey was administered 
   4.	26 Features or Columns: ['destination', 'passanger', 'weather', 'temperature', 'time', 'coupon', 'expiration', 'gender', 'age'', ………'Y']
   
	 Tools & Technologies
  
   1.	Python, Pandas, NumPy, Seaborn, Matplotlib, Jupyter

Methodology

  1.	Checked on Missing Values and Reasons for not excluding them
  2.	Conducted Exploratory Data Analysis and Descriptive Statistics on “Coupons Data”
  3.	Analyzed Data and Acceptance rate for all coupon categories
  4.	Focused on “Bar Coupon” data Analysis and Findings

Data Exploration and Decisions: Overall Coupons Data

1.	Missing Values in "Car", "Coffee House", "Restaurant20To50", "RestaurantLessThan20", "Bar", "Carry Away”
2.	Decided to keep the missing data as it is because for all missing data in Bar, Coffee House, Restaurant20To50, Carry Away and RestaurantLessThan20, there are coupons accepted values (Y=1) and do not want any Y=1 should be taken off from the table
3.	And there are only 13 records where there are missing values in above mentioned 5 columns (except "Car") and Y=0 (39 records have Y=1). 

Findings: “Overall Coupons Data”

Data
1.	The overall temperature data is a normally distributed data 
   •	Skewed to the LEFT with Mean as 63.3 and Median as 80
   •	For accepted coupons accepted (Y=1), data skewed to the LEFT with Mean as 64.3 and Median as 80
   •	For coupons not accepted (Y=0) data skewed to the RIGHT with Mean as 61.9 and Median as 55
   •	Median doesn’t show in the boxplot, as it either coincides with the Q1 or Q3 value
2.	The IQR for the overall temperature data is 25.0.
3.	Positive correlation between "Direction_opp to toCoupon_GEQ25 and toCoupon_GEQ15" AND "toCoupon_GEQ25 and toCoupon_GEQ15" 
4.	Negative correlation between "Response (Y) and toCoupon_GEQ25" AND "Response (Y) and Expiration"

Findings / Analysis Results

1.	Overall Coupons Acceptance Rate is 56.8% (including all Coupon categories) 
2.	Coffee House Coupons accounts for ~32% of Total Coupons (~4,000 out of 12,684)
3.	The coupon acceptance rate is highest at 80F (60%) and lowest at 30F (53%)
4.	The acceptance rate for Bar Coupons is Lowest at: 41%, Others: Coffee House: 50%, Restaurants(<20): 70.7%, Restaurants (20-50): 44%, Carry Out & Take Away: 73.5%
5.	The acceptance rate for Destination as “NO URGENT PLACE” is the highest at: 63.4% while for HOME and WORK, acceptance Rate stands at ~50%
6.	Coupon Acceptance Rate is highest for age “below 31” at 60%+ and Lowest in “50Plus” age group

Findings: “BAR Coupons Data”
1.	Overall Bar Coupon Acceptance Rate at 41% (Lowest across Coupon categories)
2.	Acceptance Rate for those who visited the bar 3 or fewer times is 37% and is almost half compared to those who visited the bar more than 3 times (is at 77%)
3.	Acceptance Rate for Age above 25 & Bar visit > once/months at 69.5% (30 ppts higher compared to who visit the Bar less than once/month and are below 25)
4.	72% Acceptance Rate for those who visited the bar > once/months and have No kids as passengers and occupation other than farming, fishing and forestry compared to only 50% for those who visited the bar < once/month and have kids as passengers or are alone, and occupation as farming, fishing and forestry.
5.	71.8%% Coupon Acceptance Rate for those who visited the bar > once/months and had passengers that were not kids and were not widowed compared to 72.2% for those who visited the bar > once/month and are under the age of 30. 45.3% Acceptance Rate For those who visited the cheap restaurants > 4 times/month and have income < 50K

Key Hypothesis and Conclusions Drawn

Drivers who are most likely to accept the Bar coupons could have the following characteristics:
1.	Frequent visitor (1-3, 4-8 and gt8) to the bar have higher Coupon acceptance rate
2.	Age between 21 and 26 should have the higher Coupon acceptance rate followed by 41 to 46 Age group 
3.	Professions other than Farming, Fisheries and Forestry should have higher acceptance rate
4.	Drivers with Friends as passenger should have higher Coupon acceptance rate (as compared to those with kids as passengers)
5.	Drivers are likely to have a higher acceptance rate at 55F (Pleasant weather) as compared to extremely hot or cold weather (30F or 80F)
6.	Drivers with marital status as “Single” likely to have higher coupon acceptance rate. "Widowed" are likely to have a lower acceptance rate
7.	Drivers who are SINGLE and MALE have a higher Coupon acceptance Rate
8.	10AM to 2PM Times may have a higher Bar Coupon Acceptance Rate

Recommendation:

"Target Frequent bar visitors (more than 2-3 times a month), people in the age Group “21-26” during late afternoon and evenings (2PM to 6PM) and are driving with Friends as passengers. This should drive the Bar coupon acceptance rate"

Next steps
1.	Drill down into other Coupon Categories: Coffee House, Restaurants (<20), Restaurants (20-50), Carryout and Takeaway, to understand what drives the Coupon Acceptance Rate.
2.	Identify the 6-8 most significant features that impact the Coupon Acceptance Rate by each Coupon Category and recommend STRATEGY for each segment
3.	Build a Machine Learning Model that helps better Customer Targeting thereby improving the “Coupon Acceptance Rate”

Contact
Deepak Kaushik
Email: xyz@gmail.com
