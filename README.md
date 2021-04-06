# IPO Market Forecasting
The project involves the following steps:

1. Understanding the IPO Market
- Importing the data downloaded from IPOScoop https://www.iposcoop.com/scoop-track-record-from-2000-to-present/

2. Data Cleaning
- Convert data into standard format
- Replace 'N/C' value
- Find and fix wrong date 

3. Data Exploration:
- The bar plots of mean and median of 1st day % change shows that the long right tail suggesting heavy returns for potential buyers at offering price
- The histogram of 1st day % change describes that the most returns are clustered around zero but there is a long tail to the right
- The histograms of % change  from Open to Close shows that the long tail on the right shows there is still a ray of hope to take advantage of

4. Feature Engineering:
- Weekly change
- Close to Opening change
- Total number of underwriters for each IPO
- The day/month of the purchase
- Open Gap % between Opening price and the $ Change Opening

5. Binary Classification using Logistic Regression and Random Forest Regression:
<img width="360" alt="Screen Shot 2021-04-06 at 4 39 43 PM" src="https://user-images.githubusercontent.com/69823722/113776082-81944b00-96f7-11eb-8bc4-0db7feaeece4.png">

- 1 means 'Purchase', 0 means'Not Purchase'
- Split the data to train and text: test the 2015 data, train all previous year
- Tried to set threshold from $1 to $0.25
- Applying the logistic regression and Random Forest Regresssion algorithm after feature engineering results in better results
- Plot the feature importance, shows that gap opening percentage and dollar change from opening are the most important features 
