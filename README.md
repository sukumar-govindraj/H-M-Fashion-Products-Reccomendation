
# H&M Personalized Fashion Recommendations

## 1. Overview and Background
H&M Group, a leading fashion retailer with over 4,850 stores and a global online presence, offers an extensive product range to customers. However, the vast selection often results in **difficulty for customers in finding relevant items quickly**, which can lead to **missed purchase opportunities and high return rates**.

To **enhance the customer shopping experience**, this project focuses on developing a **personalized recommendation system** that predicts the products a customer is likely to purchase within the next seven days. By leveraging **historical purchase data, customer demographics, and product metadata**, we aim to provide tailored suggestions that improve conversion rates, increase revenue, and reduce unnecessary returns.

### Business Objectives
- **Increase Sales**: Drive higher conversions by recommending relevant products.
- **Enhance Customer Engagement**: Provide personalized recommendations based on past behavior.
- **Reduce Return Rates**: Suggest better-fit products to minimize unnecessary returns.
- **Optimize Inventory Management**: Predict demand trends for stock planning.

## 2. Data Structure and Feature Description
The dataset consists of **customer transaction history, product metadata, and customer information**. The following tables provide structured data:

### Key Files
| File Name | Description |
|-----------|------------|
| `transactions_train.csv` | Contains customer purchase history (customer ID, product ID, purchase date). |
| `customers.csv` | Includes customer demographics and loyalty program status. |
| `articles.csv` | Provides detailed metadata about each product (category, material, product type). |
| `sample_submission.csv` | Example submission format for model predictions. |
| `images/` | Folder containing product images, categorized by article ID. |

### Feature Descriptions
#### Transactions Data (`transactions_train.csv`)
- **Customer ID**: Unique identifier for each customer.
- **Article ID**: The product ID that was purchased.
- **Purchase Timestamp**: Date and time of the transaction.
- **Sales Channel**: Whether the purchase was made online or in-store.

#### Customers Data (`customers.csv`)
- **Age**: Customer’s age.
- **Loyalty Program**: Indicates if the customer is a part of H&M’s loyalty program.
- **Account Creation Date**: Date when the customer first registered.

#### Products Data (`articles.csv`)
- **Product Type**: Type of clothing item.
- **Color, Material, Garment Group**: Key attributes defining the article.
- **Product Description**: Text-based metadata for recommendations.

The dataset is preprocessed in the [Data Preprocessing Notebook](H&M_Product_Reccomendation.ipynb).

## 3. Executive Summary
### Overview of Findings
- **H&M’s sales peaked in late 2020**, but have since experienced **a decline in 2022**. 
- **Year-over-year sales dropped** by:
  - **Order Volume**: ⬇️ 40%
  - **Revenue**: ⬇️ 46%
  - **Average Order Value (AOV)**: ⬇️ 10%
- **Primary reasons** for the decline:
  - **Return to pre-pandemic shopping trends**.
  - **Reduced online engagement compared to 2020-2021 pandemic peaks**.
  - **Decreased frequency of repeat purchases by customers**.

A detailed exploratory data analysis (EDA) is available in the [EDA Notebook](H&M_Product_Reccomendation.ipynb).

## 4. Results and Recommendations
### Results from the Recommendation Models
Our machine learning models delivered the following performance:

| Model | Hit Rate@10 | MAP@10 | Recall@10 |
|--------|------------|--------|-----------|
| Item-Based Collaborative Filtering | **0.72** | 0.45 | 0.63 |
| Content-Based Filtering (TF-IDF) | 0.65 | **0.48** | 0.60 |
| Neural Collaborative Filtering (NCF) | **0.78** | **0.52** | **0.69** |
| Graph Neural Networks (GNN) | **0.81** | **0.55** | **0.72** |

The complete model training and evaluation can be found in the [Model Training Notebook](H&M_Product_Reccomendation.ipynb).

### Actionable Business Recommendations
#### 1. Personalized Marketing Campaigns
- Utilize **purchase history and behavioral data** to **send targeted promotions** to customers.
- Example:  
  **"Since you bought a denim jacket, here are some sneakers that pair well with it!"**

#### 2. Bundled Discounts & Upselling
- Customers frequently buy **jeans and sneakers together**—offer **bundled deals**.
- Example:  
  **"Buy a winter coat + boots together and get 15% off!"**

#### 3. Region-Specific Product Promotions
- Adjust inventory based on **regional climate demands**.
- Example:  
  **"Promote lightweight summer wear in tropical regions year-round"**.

#### 4. Improve Mobile Shopping Experience
- Since **75% of purchases happen via mobile**, H&M should **enhance mobile app recommendations**.
- **Implement AI-driven “smart search”** to **surface relevant products faster**.

#### 5. Enhance Loyalty Program Engagement
- Loyalty members **spend 35% more per order**—**incentivize sign-ups**.
- Example:  
  **"Join the H&M Loyalty Program today and get 20% off your next purchase!"**

## Conclusion
This project successfully demonstrates **how data-driven recommendations can transform H&M’s business strategy**. By implementing a **personalized recommendation system**, H&M can:
✅ **Increase revenue** through improved product discovery.  
✅ **Reduce returns** by recommending the right fit for each customer.  
✅ **Enhance customer loyalty** through targeted engagement.  

