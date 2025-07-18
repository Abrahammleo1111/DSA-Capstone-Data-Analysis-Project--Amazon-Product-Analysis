# DSA-Capstone-Data-Analysis-Project--Amazon-Product-Analysis
This is my first project to start my portfolio building while taking my Data Analysis class with the incubator hub

 ## Project Topic: Amazon Product Analysis

 ### Project Overview
This project focuses on analyzing a dataset of Amazon products to uncover patterns and insights that can inform strategic decisions for sellers, marketers, or consumers. The dataset includes key variables such as product category,rating,rating count, discount percentage, and reviews.

The primary goal is to explore how different factors influence product performance across various categories. Key questions include:

 How do average ratings and review counts vary by category?
 - Is there a correlation between discount percentage and customer ratings or review volume?
 - Which categories exhibit the highest engagement or customer satisfaction?
 - What product characteristics are most associated with high performance?

Through data cleaning, visualization, and exploratory data analysis (EDA), the project aims to provide actionable insights into consumer behavior and market trends on Amazon. The findings can help optimize product listings, pricing strategies, and promotional efforts for e-commerce success.

### Data Source
The primary source of Data used here is Amazon case study.xlsx and this is an open source data that can be freely downloaded from an open source online such as kaggle or FRED Or any other data respository site.

### Tools used
- Ms Excel for Data cleaning and for creating a report [Download Here](https://www.microsoft.com)


### 🧹 Data Cleaning and Preparation

Data cleaning and preparation is a critical step to ensure the dataset is accurate, consistent, and ready for analysis. The raw dataset used for this Amazon product analysis includes the following fields: product category,rating, rating count, discount percentage, and reviews. Below are the main steps taken to clean and prepare the data:

#### 1. Loading the Dataset

* Imported the dataset using `Pandas` (e.g., `pd.read_csv()` for CSV files).
* Performed an initial inspection using `.head()`, `.info()`, and `.describe()` to understand the structure and content.

#### 2. Handling Missing Values

* Identified missing values using `.isnull().sum()`.
* For numerical fields like rating and rating count, missing values were either:

  * Filled with the mean/median (if few values were missing), or
  * Removed (if too many were missing and unresolvable).
* For reviews missing text entries were filled with "No review provided" or excluded if irrelevant.

#### 3. Data Type Conversion

* Converted rating count and discount percentage to numeric types if they were incorrectly loaded as strings.
* Ensured discount percentage was represented as a float (e.g., 20% → 0.20).
* Standardized rating to one decimal place for uniformity.

#### 4. Text Cleaning for Reviews

* Removed unnecessary characters, HTML tags, punctuation, and emojis using regular expressions.
* Converted all reviews to lowercase.
* Removed stopwords (e.g., "the", "and", "is") to clean the text for future sentiment analysis.
* Tokenized and lemmatized words to reduce them to their base forms.


#### 5. Categorical Value Standardization

* Standardized product category values by removing extra spaces, correcting typos, and making categories consistent (e.g., "Electronics" vs. "electronic gadgets" → "Electronics").
* Encoded categories using label encoding or one-hot encoding depending on analysis requirements.

#### 6. Outlier Detection and Treatment

* Visualized numerical columns (like rating count and discount %) using boxplots to detect outliers.
* Treated extreme values by:

  * Removing them if they were clearly data entry errors.
  * Applying transformations (e.g., log scaling) to normalize skewed distributions.

#### 7. Duplicate Removal
Checked for duplicate rows using `df.duplicated()` and removed them if necessary to avoid bias.

#### 8. Data Normalization (Optional)
 Scaled numerical features like rating count and discount percentage for consistent analysis (especially if applying machine learning).

After cleaning and preparing the data, the dataset was structured, reliable, and ready for visualization, exploration, and modeling.

Sure! Here's a concise **Exploratory Data Analysis (EDA)** section for your Amazon product analysis project:

---

###  Exploratory Data Analysis (EDA)

The exploratory data analysis phase focused on uncovering trends, patterns, and relationships within the dataset to better understand product performance across different categories on Amazon.

### Key steps and insights included:

### Distribution of Product Ratings:
  Most products had ratings between 3.5 and 4.5, indicating generally positive customer feedback. A small number of products had extremely low ratings, which may require further investigation.

### Rating Count vs. Product Categories:
  Some categories, such as Electronics and Home & Kitchen, had significantly higher rating counts, suggesting more consumer engagement and visibility.

  ### Discount Percentage Analysis:
  Products offering higher discounts did not always have higher ratings. However, some categories (like computer gadget) showed a positive trend between discounts and customer engagement.

### Review Sentiment Preview (if included):
  A preliminary analysis of product reviews revealed that positive reviews often mentioned quality and fast delivery, while negative ones focused on defects or poor packaging.

  ### Correlation Analysis:
  A weak correlation was observed between discount percentage and rating count, suggesting that discounts may influence purchase frequency but not always customer satisfaction.
Visualizations such as bar charts, histograms, scatter plots, and word clouds (for reviews) were used to support these findings.
This EDA provided valuable insights into customer behavior, product popularity, and potential areas for business improvement. It also guided feature selection for deeper analysis or modeling steps.

### Data Analysis

This is where functions used for the data analysis are included:

``` Excel
=IF(A2=1,"91-100%",INT(A2*100/10)*10 & "-" & (INT(A2*100/10)*10 + 10) & "%")

```

### Analysis
[Amazon 101](https://github.com/user-attachments/assets/90ef951f-d8b3-4457-bf9c-c392ac8968c9)
[Amazon102](https://github.com/user-attachments/assets/d5d98529-7e31-4078-bfeb-b98265d63c1b)
 




















