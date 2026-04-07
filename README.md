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

##  Key Insights

- Most restaurants have ratings between 3.5 and 4.5  
- Popular cuisines dominate the dataset  
- Certain locations have higher restaurant density  
- Higher-rated restaurants tend to have more votes  
- Many restaurants offer delivery services  

---

##  Outcome 

- Cleaned dataset ready for analysis  
- New features created for better insights  
- Key patterns identified using visualizations  

