# Customer-Segmentation
## 📌 Project Overview
This project aims to segment customers of an e-commerce platform using unsupervised machine learning techniques. The segmentation is based on customer demographic information and transactional behavior. By identifying distinct customer groups, the business can target specific segments with tailored offers, particularly focused on maximizing loyalty and satisfaction through coupon distribution.

The dataset consists of five interrelated tables containing information about customers, transactions, branches, and merchants. These tables have been merged and processed to extract meaningful features for clustering.

## 🔧 Data Preprocessing
The data undergoes the following preprocessing steps:<br>

**Merging Tables:** The Customers, Genders, Cities, Transactions, Branches, and Merchants tables are merged into a single DataFrame using customer_id, gender_id, city_id, etc., as keys.<br>
**Label Encoding:** Categorical variables such as gender_name, city_name, and merchant_name are label-encoded to numerical values.<br>
**Standardization:** Numerical features are standardized to have a mean of 0 and standard deviation of 1, improving the performance of the clustering algorithms.

## 🔧 Feature Selection
The features used for customer segmentation include:

**Demographic Features:** gender_name, city_name. <br>
**Transactional Features:** <br>
**Frequency of transactions:** Number of transactions per customer.<br>
**Transaction status:** Whether the coupon was claimed or burnt.<br>
**Coupon usage:** Different types of coupons used by customers.<br>
**Merchant name:** Merchant with whom the transaction occurred. <br>
These features are selected based on their ability to describe customer behavior.

## 🔧 Model Approach
The primary unsupervised learning technique used for customer segmentation is K-Means Clustering. Other models such as DBSCAN or Hierarchical Clustering can also be explored based on the use case.<br>

### **K-Means Clustering**<br>
**Feature Selection:** Features such as gender_name, city_name, transaction_status, coupon_name, merchant_name, and transaction_count are used.<br>
**Number of Clusters:** We experiment with different numbers of clusters (K) ranging from 2 to 10.<br>
**Evaluation:** The optimal number of clusters is selected based on evaluation metrics such as Inertia and Silhouette Score.

## 📈 Segment Analysis and Key Findings
Once the model has assigned customers to clusters, each segment is analyzed based on key features such as:<br>

**Average transaction count:** How frequently customers in this segment use the platform.<br>
**Coupon usage:** Types of coupons redeemed by customers.<br>
**City and Gender demographics:** Distribution of genders and cities in each segment.<br>
**Merchant preferences:** Most popular merchants in each segment.<br>

### Key Findings:<br>
**Segment 1:** High-frequency customers, predominantly using high-value coupons and interacting with specific merchants.<br>
**Segment 2:** Low-frequency users who rarely burn coupons and primarily use the platform for browsing.<br>
**Segment 3:** Loyal customers from major cities who frequently redeem coupons with multiple merchants.<br>
**Segment 4:** New or low-engagement customers with few transactions.
