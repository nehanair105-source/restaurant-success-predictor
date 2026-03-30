# Restaurant Success Predictor

##  Project Overview
This project aims to analyze restaurant data and predict whether a restaurant will be successful based on factors like cuisine, price, location, and ratings.

---

##  Dataset Description
The dataset was collected by scraping restaurant data from Zomato.

###  Dataset Size:
- Number of rows: 3834
- Number of columns: 11

### Features:
- Name
- Cuisine
- price
- Location
- Dining rating
- Delivery rating
- Dining votes
- Delivery votes

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
- Rating ≥ 4.0 → Successful  
- Rating < 4.0 → Not Successful  

---

##  Folder Structure

- data/ → contains raw scraped dataset  
- notebooks/ → will contain analysis notebooks (future work)  

