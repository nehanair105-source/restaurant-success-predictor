# Restaurant Success Predictor

##  Project Overview
This project aims to analyze restaurant data and predict whether a restaurant will be successful based on factors like cuisine, price, location, and ratings.

---

##  Dataset Description
The dataset was collected by scraping publicly available restaurant data from Zomato.

###  Dataset Size:
- Number of rows: 3834  
- Number of columns: 11  

###  Features (Raw Dataset):
- name: Restaurant name  
- cuisine: Type of food offered  
- cost_for_two: Average cost for two people  
- location: Restaurant location  
- dining_rating: Rating for dine-in experience  
- delivery_rating: Rating for delivery service  
- dining_votes: Number of votes for dining  
- delivery_votes: Number of votes for delivery  

---

##  Data Collection Method

###  Tools Used:
- Chrome Web Scraper Extension
- Google Chrome Browser

###  Process:
1. Created sitemap for Zomato pages  
2. Selected elements (name, cuisine, price, rating, etc.)  
3. Used selectors to extract data  
4. Scraped multiple pages  
5. Exported data as CSV  

---

##  Problem Understanding
Restaurant success depends on factors like pricing, location, and customer ratings. This project analyzes these factors to predict success.

---

##  Success Metric
Restaurants are classified based on their ratings:
- Rating ≥ 4.0 → Successful
- Rating < 4.0 → Not Successful

This threshold is chosen because restaurants with ratings above 4 are generally considered highly rated and preferred by customers.

---

# Data Cleaning & Exploratory Data Analysis (EDA)

##  Data Cleaning

The raw dataset collected in Week 1 contained missing values, inconsistent formats, and non-numeric entries. The following cleaning steps were performed:

- Removed invalid values like 'New' and '-' from rating columns  
- Converted dining_rating and delivery_rating to numeric format  
- Cleaned price column by removing text and converting to numeric values  
- Standardized location column (cleaned and formatted properly)  
- Converted votes columns to numeric by removing commas  
- Handled missing values by filling with 0 or removing invalid rows  

---

##  Feature Engineering

New features were created to improve analysis:

- Success:
  - 1 → Successful (rating ≥ 4)  
  - 0 → Not successful  

- Has Delivery:
  - 1 → Delivery available  
  - 0 → No delivery  

- Price Category:
  - Low (0–300)  
  - Medium (300–600)  
  - High (600–1000)  
  - Luxury (1000+)  

---

##  Exploratory Data Analysis (EDA)

Various visualizations were created to understand the dataset:

- Distribution of dining ratings  
- Distribution of price  
- Distribution of votes  
- Top cuisines  
- Top locations  
- Success vs non-success comparison  
- Delivery availability analysis  

---

#  Model Building & Evaluation

## Model Preparation

Before training the models, the dataset was preprocessed:

- Removed unnecessary columns like name  
- Applied log transformation on votes to reduce skewness  
- Encoded categorical features:
  - Price category → Label Encoding  
  - Cuisine → MultiLabelBinarizer  
- Created location-based features  
- Handled class imbalance using appropriate weights  

---

## Train-Test Split

The dataset was split into:

- 80% Training Data  
- 20% Testing Data  

Random state was set to ensure reproducibility.

---

## Models Used

The following machine learning models were trained and evaluated:

- Logistic Regression  
- Support Vector Machine (SVM)  
- Decision Tree  
- Random Forest  
- XGBoost  

---

## Hyperparameter Tuning

Hyperparameter tuning was performed on XGBoost using GridSearchCV:

- n_estimators: 100, 200, 300  
- max_depth: 3, 5, 7  
- learning_rate: 0.01, 0.1, 0.2  

---

## Evaluation Metrics

The models were evaluated using:

- Accuracy  
- Precision  
- Recall  
- F1 Score  

---

## Final Model

- Best performing model: XGBoost (after tuning)  
- Provided the best balance between precision and recall  
- Handled class imbalance effectively  

---

## Feature Importance

The most important features affecting restaurant success:

- Dining rating  
- Dining votes  
- Location  
- Price category  
- Cuisine  

---

#  Results & Insights

Key insights obtained from the analysis:

- Restaurants with higher ratings (≥ 4) are more likely to be successful  
- Location plays a significant role in determining success  
- Medium-priced restaurants tend to perform better  
- Popular cuisines attract more customers  
- Restaurants offering delivery services show better performance  

---

# Conclusion

This project successfully predicts restaurant success using machine learning techniques.

- Data cleaning and preprocessing improved model performance  
- Ensemble models like XGBoost performed better than basic models  
- The model can be useful for business decision-making  
 

---



