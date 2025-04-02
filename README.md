# **Identifying Vulnerable Countries for Humanitarian Aid Using Clustering**

## **Introduction**  
The dataset comprises socio-economic and health metrics for **167 countries**, including variables like GDP per capita (`gdpp`), child mortality rate (`child_mort`), income per capita (`income`), and life expectancy (`life_expec`). The goal of this project is to **identify the most vulnerable countries** that require urgent humanitarian aid from **HELP International NGO**. By leveraging **clustering algorithms (KMeans and Hierarchical)**, we segment countries based on their economic and health conditions to prioritize aid distribution effectively.

---

## **Objective**  
The primary objective is to:  
- **Cluster countries** into distinct groups based on economic and health indicators.  
- **Identify the most struggling nations** with high child mortality, low income, and low GDP per capita.  
- **Provide actionable insights** to the NGO for targeted aid allocation.  

---

## **Steps Conducted**  
1. **Data Preprocessing**  
   - Handled outliers by capping extreme values (e.g., 95th percentile for `gdpp`).  
   - Scaled features using `StandardScaler` for unbiased clustering.  

2. **Exploratory Data Analysis (EDA)**  
   - Visualized distributions and outliers using histograms and box plots.  
   - Observed high child mortality in underdeveloped nations and economic disparities.  

3. **Clustering**  
   - **KMeans Clustering**:  
     - Determined optimal clusters (`k=3`) using the **Elbow Method** and **Silhouette Score**.  
     - Identified **Label 0** as the most vulnerable cluster (high `child_mort`, low `gdpp`).  
   - **Hierarchical Clustering**:  
     - Used **complete linkage** for clearer dendrogram interpretation.  
     - Confirmed **3 clusters**, though results were imbalanced.  

4. **Cluster Profiling**  
   - Compared mean values of key metrics (`child_mort`, `income`, `gdpp`) across clusters.  
   - Validated findings using **box plots and scatter plots**.  

5. **Final Recommendations**  
   - Ranked countries needing aid based on economic and health distress signals.  

---

## **Results**  
- **Top 5 Vulnerable Countries (KMeans Label 0)**:  
  1. **Burundi** (Lowest GDP: $231, High Child Mortality: 93.6)  
  2. **Liberia** (Income: $700, Child Mortality: 89.3)  
  3. **Congo, Dem. Rep.** (Lowest Income: $609, Child Mortality: 116.0)  
  4. **Niger** (Child Mortality: 123.0, GDP: $348)  
  5. **Sierra Leone** (Highest Child Mortality: 160.0, GDP: $399)  

- **Key Insights**:  
  - Countries in **Label 0** exhibit **extreme poverty, low healthcare access, and high child mortality**.  
  - **KMeans outperformed Hierarchical Clustering** in balanced segmentation.  

---

## **Conclusion**  
This project successfully **identified the most economically and socially vulnerable countries** using clustering techniques. **HELP International NGO** should prioritize aid to **Burundi, Liberia, Congo (Dem. Rep.), Niger, and Sierra Leone**, focusing on **healthcare, economic support, and education** to mitigate critical challenges.  

**Future Work**:  
- Incorporate additional indicators like political stability or education rates.  
- Test other clustering algorithms (e.g., DBSCAN) for comparison.  

**Tools Used**: Python, Pandas, Scikit-learn, Matplotlib, Seaborn  

**Author**: Jay Thakur
