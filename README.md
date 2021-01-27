# My-Projects
This is my list of personal and professional projects that i've done. Feel free to look and give feedbacks if you want!
p.s. : The list is sorted from the latest projects i've done.

1. [Cross-sell Prediction Hackathon](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/)

Cross-selling identifies products or services that satisfy additional, complementary needs that are unfulfilled by the original product that a customer possesses. As an example, a mouse could be cross-sold to a customer purchasing a keyboard. Oftentimes, cross-selling points users to products they would have purchased anyways; by showing them at the right time, a store ensures they make the sale.

In this case, we are tasked to cross-sell our vehicle insurance product to people who bought our health insurance. But we can't just pitch everyone into buying them because it will be time consuming. So, how do we know which one we have to ask to buy the insurance?

**Approach**

By creating Machine Learning model to predict customer's response, we could :

1. Maximize revenue by capturing all of the market share
2. Cut the time and cost of selling those insurance

Also, by exploring our data we could gain new insight of our customer's behaviour.

**EDA**

Here's the features correlation heatmap, notice that 'Previously_Insured' has the highest correlation on the 'Response'<br>
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/heatmapcorr.png 'Correlation Heatmap')<p>
Pretty sure that only people who currently don't have vehicle insured will response positively<br>
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/previnsured.png 'Previously_Insured countplot')<p>
Here we can see how the vehicle age and damage distribution based on their response<br>
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/vehage.PNG 'Vehicle Age based on the response')<p>
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/vehcomp.PNG 'Vehicle Composition')<p>

**Model Evaluation**

Classification Metrics of CatBoost model with auto-balanced class weight<br>
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/classweightmetric.PNG)<p>
Confusion Matrix of CatBoost model with auto-balanced class weight<br>
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/conclassweight.png)<p>
ROC-AUC plot CatBoost model with auto-balanced class weight<br>
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/rocaucclassweight.png)

2. [AV Healthcare Analytics II Hackathon](https://github.com/kimichiaveli/AV-Healthcare-Analytics-II-Project/)
3. [Titanic](https://github.com/kimichiaveli/Titanic/)
