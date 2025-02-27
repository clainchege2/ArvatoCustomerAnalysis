# Arvato Customer Analysis

This is a comprehensive and well-structured project on identifying customer segments using unsupervised learning techniques. Below is a summary of the key steps and findings:

### Project Summary: Identify Customer Segments

#### Objective:
To identify segments of the population that form the core customer base for a mail-order sales company in Germany using unsupervised learning techniques.

#### Steps and Findings:

1. **Data Loading and Initial Exploration:**
   - Loaded the general demographics data (`Udacity_AZDIAS_Subset.csv`) and the feature summary file (`AZDIAS_Feature_Summary.csv`).
   - Initial exploration showed the structure and some sample data points.

2. **Preprocessing:**
   - **Assess Missing Data:**
     - Converted missing value codes to NaNs.
     - Assessed and handled missing data in each column and row.
     - Removed columns with more than 20% missing values and rows with more than 3 missing values.
   - **Feature Selection and Re-encoding:**
     - Re-encoded categorical features.
     - Engineered new features from mixed-type features.
     - Dropped mixed-type features after engineering.

3. **Feature Transformation:**
   - **Feature Scaling:**
     - Applied mean imputation and standard scaling to handle missing values and normalize the data.
   - **Dimensionality Reduction:**
     - Applied PCA to reduce the dimensionality of the data.
     - Retained 100 principal components, which account for approximately 87.85% of the total variance.

4. **Clustering:**
   - **K-Means Clustering:**
     - Applied K-Means clustering to the PCA-transformed data.
     - Used the Elbow Method to determine the optimal number of clusters (k=10).
     - Obtained cluster assignments for the general population data.

5. **Applying the Same Steps to Customer Data:**
   - Loaded and cleaned the customer demographics data (`Udacity_CUSTOMERS_Subset.csv`).
   - Applied the same preprocessing, feature transformation, and clustering steps to the customer data.
   - Obtained cluster assignments for the customer data.

6. **Comparing Customer Data to General Population Data:**
   - Compared the proportion of data points in each cluster for the general population and the customer data.
   - Identified overrepresented and underrepresented clusters in the customer data.
   - Interpreted the characteristics of these clusters using principal component weights.

#### Key Findings:
- **Overrepresented Clusters in Customer Data:**
  - Cluster 7 (Principal Component 7) is overrepresented in the customer data.
  - This cluster includes features like high social status (`LP_STATUS_GROB_1.0`), high wealth (`CAMEO_DEUG_2015_9`), and urban living (`ANZ_HAUSHALTE_AKTIV`).
  - These findings suggest that the company's products or services are popular among affluent, urban individuals with high social status.

- **Underrepresented Clusters in Customer Data:**
  - Cluster 8 (Principal Component 8) is underrepresented in the customer data.
  - This cluster includes features like smaller family types (`LP_FAMILIE_FEIN_2.0`), specific life stages (`LIFE_STAGE`), and middle-class wealth (`CAMEO_DEUG_2015_3`).
  - These findings suggest that the company's products or services are less popular among smaller families and middle-class individuals.

#### Conclusion:
The analysis identified key segments of the population that are more likely to be part of the company's customer base. The company can use these insights to tailor its marketing strategies and product offerings to better target these segments. Additionally, the underrepresented clusters suggest potential new markets that the company could explore to expand its customer base.

#### Next Steps:
- Further investigate the characteristics of the identified clusters to develop targeted marketing campaigns.
- Explore additional data sources or features that could provide deeper insights into customer preferences.
- Implement and evaluate the impact of new marketing strategies based on these findings.

This project demonstrates a thorough application of unsupervised learning techniques to identify and understand customer segments, providing actionable insights for strategic decision-making.
---

