Step#1: Review the Coupon dataset
The dataset is reviewed using:
1. datasetname.isnull().values.any() to check for any NaN in the dataset
2. datasetname.coulumnname.unique() is used to check the values in each column.

Step#2: Data Cleanup Steps:
After reviewing the dataset, I gathered that:
1. The values "less1" and "never" esentially mean 0 and can be replaced by 0
2. The value gt8, 50plus, below21 can be replaced by 8+, 50+, <21 respectively
3. The car value is null for 12577 records and I decided to replace it by "Unknown" instead of dropping car column as it is needed for the data analysis later.
4. There are NaN values of Bar, CoffeeHouse, CarryAway, RestaurantLessThan20, Restaurant20To50 columns too. I decided to to replace them by "Unknown" as well.  
5. Few column names can be renamed for better readability.

Step#3: Investigate the Bar Coupons  
Below are the hypothesis based on the observations:
1. Hypothesis #1 - The drivers who visit bar less than 3 times a month accept coupons more compared to the drivers who visit bar more than 3 times a month.
2. Hypothesis #2 - The drivers are more likely to visit bar alone than with partners, friends or kids.
3. Hypothesis #3 - The drivers over 25 years of age visited bar more than once.

Step#4: Independent Investigation:
Compare the acceptance rate of coupons of restaurants under $20, restaurants between 20 - 50, carry away and bar by the people from the following group and who visit restaurants more than 3 times per month:
1. Married males
2. Married females
3. Single males
4. Single females
5. Divorced males
6. Divorced females
7. Widowed males
8. Widowed females

Findings:
1. Carry Away is the most favourite among most of the groups.
2. Single males like to visit carry away, expensive restaurants and bars the most among the study groups.
3. Widowed males do not visit restaunts, bars and carry away more than 3 times a month.
4. Widowed females do not visit expensive restaurants and bars more than 3 times a month.
5. Divorced females do not visit bars more than 3 times a month.

It will be intersting to study the effect of other factors, like income, distance from coupon, direction etc on the
behavior of the above groups. Based on the above study, it looks like there is a scope to send more lucrative coupons
to divorced and widowed. Also, more coupons for the expensive restaurants will help all the groups.  

Jupyter Notebook: 
The implementation can be found in Assignment 5.ipynb
