## Prediction Product AD Campaign Performance
#### Problem Statement :  
Our client, a leading outdoor apparel company, seeks to predict the performance of product ad campaigns before launch to optimize their marketing efforts. 
This project aims to develop a predictive model that forecasts key performance indicators (KPIs) for future campaigns, providing valuable insights for strategic decision-making and resource allocation. 
Ultimately, this will enhance marketing effectiveness and improve the ROI by focusing on the most effective channels and strategies.

#### About the dataset:
- limit_infor: limits or restrictions associated with the marketing campaign or product.
- campaign_type: type of marketing campaign, such as email, social media, print advertising,etc
- campaign_level: level or scale of the marketing campaign, for example, national, regional, or local.
- product_level: level or category of the product being marketed, such as high-end, mid-range, or budget.
- resource_amount: resources (e.g., budget, personnel, or materials) allocated for the marketing campaign.
- email_rate: email delivery rate or open rate.
- price: selling price of the product.
- discount_rate: discounts or promotional offers associated with the product.
- hour_resources: the number of labor hours or human resources dedicated to the marketing campaign or product sales efforts.
- campaign_fee: fees or costs associated with running the marketing campaign.
- orders: number of orders or sales generated for the product during the marketing campaign.

#### Here are the key details about the dataset used in this project:
- Our has 731 entries and 11 columns.  The columns  include 
- There are three columns with float data types and eight with integer data types. 
- The dataset has 5 categorical variables namely limit_infor, campaign_type, campaign_level, product_level, resource_amount whose values have been represented by single digit numbers. Here, the target variable is "orders"

#### Exploratory Data Analysis (EDA)
- EDA is used to  provides a provides a better understanding of data set variables and the relationships between them.
- The dataset had no duplicates and 2 missing values in "price" which was 0.27% of total data. Hence, the rows with missing values were dropped.
- While observing the relationship of numeric values with "orders", the campaign_fee had one outlier which was removed for a cleaner data.
- Correlation coefficient revealed that 'discount_rate' (0.232), email_rate' (0.628), 'hour_resouces' (0.664), and 'campaign_fee' (0.929) have positive correlations with 'orders'. 'price' (-0.103) has a weak negative correlation with 'orders'.
- The ANOVA results provide insights into the relationship between each categorical variable and the numerical variable 'orders'. 'product_level' and 'resource_amount' appear to have a significant relationship with 'orders', while the other categorical variables do not.
- To ensure consistent scales for numerical features,  MinMax Scaler  was employed during preprocessing.
#### Splitting the data into X and y
- In this step, we divided the dataset into two parts: X and y.
- X contains all the independent variables, which are the features used to make predictions.
- Meanwhile, y represents the dependent variable or target variable, which is the outcome we want to predict.
#### Train-Test Split
- The dataset was split into training and testing sets.
- An 80:20 ratio was used, with 80% of the data allocated to training and 20% to testing, and the test size set to 0.2.
- A random state of 42 was specified to ensure the reproducibility of results across different runs
#### Model Selection
The Prediction Product AD Campaign Performance is a regression problem. Hence following models were used:
- Linear Regression is best for simple, linear relationships and offers high interpretability.
- Support vector machine is versatile for both linear and non-linear relationships but can be computationally expensive.
- Random Forest is powerful for complex, non-linear relationships and provides robust performance but is less interpretable and more computationally intensive.
#### Conclusions
- The analysis and predictions provide valuable insights that can significantly enhance the ad campaign performance for the company.
- Campaign Fee and Hour Resources: Increasing campaign fees and allocating more resources positively influence the number of orders, suggesting that investments in these areas are likely to yield higher returns.
- Pricing Strategy: Higher prices tend to reduce the number of orders. Therefore, maintaining competitive and minimal prices can attract more customers and boost sales.
- Discount Rates: While higher discount rates can slightly increase the number of orders, their impact is minimal. This indicates that focusing primarily on pricing and resource allocation may be more effective than relying heavily on discounts.
- Model Performance: Linear regression outperforms SVM and random forest regression due to the linear relationship between features and the target variable. This finding underscores the importance of using a simpler, well-suited model to avoid overfitting and ensure accurate predictions.
- By leveraging these insights, the company can strategically allocate resources, optimize pricing, and fine-tune their ad campaigns to maximize effectiveness and improve the overall return on investment (ROI).
