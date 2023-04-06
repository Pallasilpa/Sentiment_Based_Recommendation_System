# Sentiment_Based_Recommendation_System

### Problem Statement
The e-commerce business is quite popular today. Here, you do not need to take orders by going to each customer. A company launches its website to sell the items to the end consumer, and customers can order the products that they require from the same website. Famous examples of such e-commerce companies are Amazon, Flipkart, Myntra, Paytm and Snapdeal.

Suppose you are working as a Machine Learning Engineer in an e-commerce company named 'Ebuss'. Ebuss has captured a huge market share in many fields, and it sells the products in various categories such as household essentials, books, personal care products, medicines, cosmetic items, beauty products, electrical appliances, kitchen and dining products and health care products.

With the advancement in technology, it is imperative for Ebuss to grow quickly in the e-commerce market to become a major leader in the market because it has to compete with the likes of Amazon, Flipkart, etc., which are already market leaders.

### Steps to acheive solution for sentiment based recommendation system
1. Data Cleaning and Pre-Processing :
Performed all data quality checks and addressed all data quality issues in the right way (especially the missing value treatment).

2. Text Processing :
Data Cleaning, Visualization and Text Preprocessing are applied on the dataset. TF-IDF Vectorizer is used to vectorize the textual data(review_title+review_text). It measures the relative importance of the word with respect to other documents.SMOTE Oversampling technique is used before applying the model.

3. Feature Extraction :
TF-IDF Vectorizer is used to vectorize the textual data.

4. Model Building :
Machine Learning Classification Models such as Logistic Regression, Naive Baiyes, Tree Algorithms (Decision Tree, Random Forrest, xgboost) are applied on the vectorized data and the target column (user_sentiment).The objective of this ML model is to classify the sentiment to positive(1) or negative(0).The Best Model is selected based on the various ML classification metrics (Accuracy, Precision, Recall, F1 Score, AUC). Xgboost is selected to be a better model based on the evaluation metrics.

5. Building the Recommendation System :
xgboost is selected to be a better model based on the evaluation metrics.

6. Recommendation of Top 20 Products to a Specified User :
Colloborative Filtering Recommender system is created based on user-user and item-item approaches.we used RMSE metric for evaluation.
*SentimentBasedProductRecommendation.ipynb* Jupiter notebook contains the code for Sentiment Classification and Recommender Systems.
Top 20 products are filtered using the better recommender system, and for each of the products predicted the user_sentiment for all the reviews and filtered out the top 5 products that have higher Postive User Sentiment (model.py)

7. Fine-Tuning the Recommendation System and Recommendation of Top 5 Products : 
Predicted the sentiment (positive or negative) of all the reviews in the train data set of the top 20 recommended products for a user. For each of the 20 products recommended, found the percentage of positive sentiments for all the reviews of each product. Filtered out the top 5 products with the highest percentage of positive reviews.

8. Deployment Using Flask and Heroku :
Machine Learning models are saved in the pickle files(under the pickle); Flask API (app.py) is used to interface and test the Machine Learning models. Bootstrap and Flask jinja templates (templates\index.html) are used for setting up the User interface. End to End application is deployed in Heroku.
