# Predicting-Order-Returns
**Objective** 

Predict whether an online order will be returned for an online retailer as a step to increase net margins and improve supply chain & inventory management 

**Motivation and Pain Point** 

Today, Amazon is the number one online retailer globally offering customers the opportunity to order on the fly along with free returns of items they don't like. As people who shop regularly from Amazon, we often wonder how much does it cost Amazon to restock those products. This is what initially sparked our interest and motivated us to pursue this project about predicting whether a customer will return a product.

After further research about this we found that this is a huge issue for retailers in terms of net margins from online sales. Below we have outlined the major issues faced by the retailers:

1) According to [KPMG](https://medium.com/sizolution/the-problem-of-returning-clothes-to-online-stores-89ddf3854f5d), the cost of handling a return can be as high as three times compared to the cost of delivery.

2) According to a [Medium article](https://medium.com/sizolution/the-problem-of-returning-clothes-to-online-stores-89ddf3854f5d), retailers churn 31% of new customers and 8% of repeat buyers due to poor return services, and 20% of new customers report finding the returns process to be complicated. Hence, predicting returns in advance will help retailers forecast their inventory and also, place the right return services in place to reduce customer churn rate and increase net margins.

3)  As per a [Barclays report](https://home.barclaycard/press-releases/), 57% of retailers say that dealing with returns has a negative impact on the day-to-day running of their business.

4) Finally, according to a CNBC article, 25% (~5 billion pounds) of the returns end up in landfill.

These are massive pain points for online retailers which have not been solved yet and our prediction tool will be a means to an end towards companies optimizing their return procedures. 

**Related Work**

As mentioned above, our initial idea came from us wondering about the pain points for companies like Amazon when customers return their orders. Articles above that describe the pain points further consolidated our interest as we found that this problem is soon expected to become [a trillion dollar (in terms of product cost) problem.](https://www.cnbc.com/2019/01/10/growing-online-sales-means-more-returns-and-trash-for-landfills.html)

Note: While companies like Amazon have already started to address this issue (conversation with an Amazon employee), smaller retailers are still catching up and this prediction system will certainly help them address the issues of product returns.

**Machine Learning to the rescue** <Br>
The target is to predict orders which would be returned (binary classification problem) with 100k rows of labelled data given as training data. For this task, we plan to utilize Machine Learning classification algorithms such as Random Forest, Logistic Regression, Support Vector Machines, Naive Bayes along with selective ensemble modelling for improvement of performance metrics. 
<br>
<br>
**Domain** <br>
We will be analyzing and performing prediction on retail data provided by an online retailer. The task is to predict the orders that are likely to be returned. Applying Binary Classification using Supervised Learning, we aim to develop models that will help address the pain points of the retailer. The best model to be deployed will be chosen on difference performance metrics that are suitable for the task at hand. 
<br>
<br>
**P(T, E+ ΔE) > P(T,E)** <br>
* **Task**- Prediction of orders that are likely to be returned by the customers.
* **Experience**- Past experience or training data includes 100k rows of labelled data by the retailer with target variable being "return" [0,1] where 0 is NOT RETURNED and 1 is RETURNED. With this experience we aim to automate prediction using trained Machine Learning models on unseen data consisting of 50k rows. 
* **Performance**- To measure the performance of our models on unseen data we will use metrics like Recall, Precision, Specificity, the AUC-ROC curve and Accuracy. Aim is to utilize the training data which provides experience to our models in order to maximize these metrics. Weightage for each of these performance metrics will be given based on the distribution of the target label in the training dataset. 

**Dataset (Datasets in Drive Folder)** 

The anonymous online retailer has provided us with real-world data in the form of two-csv files. It is available on [Kaggle](https://www.kaggle.com/competitions/bads1718/overview) as part of a competition in 2019:
1. [BADS_WS_1819_known.csv](https://www.kaggle.com/competitions/bads1718/data): Number of Columns:14 Number of rows: 100K
2. [BADS_WS1819_unknown.csv](https://www.kaggle.com/competitions/bads1718/data): Number of Columns:13 Number of rows: 50k

***BADS_WS_1819_known.csv***→ Training data for which the RETURN variable is known. Here RETURN is the target variable and the training data consists of attributes such as order_date, delivery_date, item_id, item_size, item_color, brand_id, item_price, user_id, user_title, user_state, user_reg_date. The item and user attributes have been combined here, for our prediction task we will utilize features which play a vital role in deciding the outcome of the target variable. All in all the training data is clean however we will use feature engineering to come up with more useful features for our prediction. We will split some of this data for testing our models.

**BADS_WS1819_unknown.csv** → This does not contain return information and will not be used/

**Roadmap**
* Perform a brief visualization on the training data to analyze the distribution of the target variable and its correlation with different features present. 

* Performing data cleaning by doing null checks, and dropping rows/ features if they do not seem to be important for our prediction task. 

* Peform feature engineering to come up with additional effective features that will enhance performance of our models. 

* Predicting the performance of testing data initially using **baseline models** which will provide us with basline metrics score that need to be improved using the advanced classification alogrithms. We can implement dummy classifiers or baseline classifiers to perform this task and the purpose of doing this would be to set a baseline score from which to improve upon using different Machine Learning techniques using regularization.

* Training state of the art classification algorithms with tuned parameters and hyperparameters. Performance on test data will then be analyzed to examine the impact these models will have in acheiving the objective at hand. 

* Coming up with Call to Actions (Insights) for the online retailer based on the findings from the task. 

**Value Proposition**

Anticipating order returns will help retailers:
* Understand where to place their warehouses in order to cut the costs of returns and also, ship the product from that warehouse if the next order delivery is closer to that warehouse.
* Decrease customer churn rate by improving their process of handling returns by allocating their resources to places that need it the most. For example, based on geographical locations that tend to have higher returns (NYC).
* Improve day-to-day business operations by being able to forecast the required warehouse space, inventory, man force, transportation services, and much more in relation to supply chain management.
* Reduce the amount of products that end up in landfill by knowing which products are commonly returned and for them, reducing the price for resale.
* Improve product sales by using personalized marketing strategies based on customer behavior.
