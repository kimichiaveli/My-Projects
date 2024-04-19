# HAKIM'S PORTOFOLIO:



## [E-Commerce Data Analytics](https://github.com/kimichiaveli/E-Commerce-Data-Analytics/)

Provided with the transaction data and relevant user information of an e-commerce platform, find out:

1. What factors contribute to users making a purchase?
2. What factors contribute to users generating higher basket amounts?

### Approach

1. Explore the Datasets
2. Find relevant features (in which the e-commerce can control to maximize the output)
3. Find correlation and pattern to prioritize the biggest deciding feature to the output
4. Explore the user’s behaviour to find the best strategy for each of them

### Insight

#### Purchases Analysis
Top 10 Contributors of Purchases Using SHAP Value.<br>
![alt text](https://github.com/kimichiaveli/E-Commerce-Data-Analytics/blob/255ce6d5404b49308f1ddef15ceca043f3dba515/purchase.png 'Purchase SHAP Value')<br><br>

#### Basket Amount Analysis
Top 10 Contributors of Basket Amount Using SHAP Value.<br>
![alt text](https://github.com/kimichiaveli/E-Commerce-Data-Analytics/blob/255ce6d5404b49308f1ddef15ceca043f3dba515/basket_amount.png 'Basket Amount SHAP Value')<br><br>
Top 10 Contributors of Basket Amount Using Feature Importance.<br>
![alt text](https://github.com/kimichiaveli/E-Commerce-Data-Analytics/blob/255ce6d5404b49308f1ddef15ceca043f3dba515/basket_amount_fi.png 'Basket Amount Feature Importance')<br><br>
Using insights from above we can make a business decisions such as:
1. Maximize promotion to province 1 users
2. Give out voucher/promo code to users who already purchased something in the same month (users who have not bought anything yet don't really need to be given voucher/promo code)
3. By giving voucher/promo code to users who already purchased something in the same month, especially in province 1 they probably will purchased something again with higher basket_amount
4. user_group 1 tends to do transaction with higher basket_amount, but note that there's only slight difference in the median
5. Increasing window shopping experience will lead to longer session length (aov) of a user and will likely to be persuaded into buying something of a higher value/basket_amount

### Recommendations to Stakeholders
1. Promoting vouchers to new users with the probability of them making their first purchase below 50% to increase conversion rate.
2. Promoting to vouchers to users who live in province 1 and already made their purchase in the same month to increase basket_amount
3. Optimize voucher’s system to ensure users making purchase.

## [Cross-sell Prediction Hackathon](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/)

Cross-selling identifies products or services that satisfy additional, complementary needs that are unfulfilled by the original product that a customer possesses. As an example, a mouse could be cross-sold to a customer purchasing a keyboard. Oftentimes, cross-selling points users to products they would have purchased anyways; by showing them at the right time, a store ensures they make the sale.

In this case, we are tasked to cross-sell our vehicle insurance product to people who bought our health insurance. But we can't just pitch everyone into buying them because it will be time consuming. So, how do we know which one we have to ask to buy the insurance?

### Approach

By creating Machine Learning model to predict customer's response, we could :

1. Maximize revenue by capturing all of the market share
2. Cut the time and cost of selling those insurance

Also, by exploring our data we could gain new insight of our customer's behaviour.

### EDA

**Here's the features correlation heatmap, notice that 'Previously_Insured' has the highest correlation on the 'Response'**<br>
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/heatmapcorr.png?raw=true 'Correlation Heatmap')<br><br>
**Pretty sure that only people who currently don't have vehicle insured will response positively**<br>
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/previnsured.png?raw=true 'Previously_Insured countplot')<br><br>
**Here we can see how the vehicle age and damage distribution based on their response**<br>
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/vehage.PNG?raw=true 'Vehicle Age based on the response')<br><br>

### Model Evaluation

**Classification Metrics of CatBoost model with auto-balanced class weight**<br>
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/classweightmetric.PNG?raw=true)<br><br>
**Confusion Matrix of CatBoost model with auto-balanced class weight**<br>
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/conclassweight.png?raw=true)<br><br>
**ROC-AUC plot CatBoost model with auto-balanced class weight**<br>
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/rocaucclassweight.png?raw=true)<br><br>

## [AV Healthcare Analytics II Hackathon](https://github.com/kimichiaveli/AV-Healthcare-Analytics-II-Project/)

### Overview

Recent Covid-19 Pandemic has raised alarms over one of the most overlooked area to focus: Healthcare Management. While healthcare management has various use cases for using data science, patient length of stay is one critical parameter to observe and predict if one wants to improve the efficiency of the healthcare management in a hospital. 

This parameter helps hospitals to identify patients of high LOS risk (patients who will stay longer) at the time of admission. Once identified, patients with high LOS risk can have their treatment plan optimized to miminize LOS and lower the chance of staff/visitor infection. Also, prior knowledge of LOS can aid in logistics such as room and bed allocation planning.

### Approach

By creating Machine Learning model to predict patient LOS, we could :

1. Predict currently treated patient LOS, and..
2. Predict recently admitted patient would be LOS

to get an overview for better room management

### EDA

**Here's how the patient's LOS is distributed, notice that we are dealing with imbalanced data with 11 classes**<br>
![alt text](https://github.com/kimichiaveli/AV-Healthcare-Analytics-II-Project/blob/main/dis2.png?raw=true)

**This is how the patient's cases are distributed based on the hospital code and region**<br>
![alt text](https://github.com/kimichiaveli/AV-Healthcare-Analytics-II-Project/blob/main/fig2.png?raw=true)

**Here is the distribution of "Available Extra Rooms" when a patient is admitted**<br>
![alt text](https://github.com/kimichiaveli/AV-Healthcare-Analytics-II-Project/blob/main/fig3.png?raw=true)
![alt text](https://github.com/kimichiaveli/AV-Healthcare-Analytics-II-Project/blob/main/fig4.png?raw=true)
  
**This chart shows that majority of patient were admitted to the hospital outside their city. The inner chart shows the composition based on the severity of their case**<br>
![alt text](https://github.com/kimichiaveli/AV-Healthcare-Analytics-II-Project/blob/main/fig10.png?raw=true)

### Model Evaluation
 
**Using CatBoost algorithm with the class weight parameter set to be true, we built a model that does not over-predict a class**<br>
![alt text](https://github.com/kimichiaveli/AV-Healthcare-Analytics-II-Project/blob/main/cm.png?raw=true)
