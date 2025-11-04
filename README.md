# Prediction-of-Houses-Sales
## Project Overview
As part of my data science bootcamp, this project aims to support a group of homeowners in Ames, Iowa, who are concerned about the declining value of their properties. The goal is to analyze raw housing market data to uncover actionable insights and deliver data-driven recommendations for increasing home value prior to sale.
<img width="800" height="450" alt="image" src="https://github.com/user-attachments/assets/fa2e7121-b93b-4f32-85fa-4af969ea18ec" />

## Objectives
- Explore and clean the Ames housing dataset
- Identify key features that influence property value
- Build predictive models to estimate home prices
- Deliver practical suggestions for value-boosting renovations or improvements



##  Exploratory Visuals & Insights

### 1. Distribution of Sale Price
![Sale Price Histogram](Plots/hist_saleprice.png)  
- Sale prices are **right-skewed**, with most houses selling between \$100K–\$250K.  

---

### 2. Correlation Heatmap
![Correlation Heatmap](Plots/heatmap_correlation.png)  
- Features such as **Overall Quality, Living Area, and Garage Cars** show strong positive correlations with SalePrice.  
- Suggests buyers value **quality, size, and garage capacity** most.  
- Heatmaps only capture **linear** relationships. For non-linear effects, scatterplots or tree-based models are better.

---

### 3. Living Area vs Sale Price (Scatter)
![Living Area vs SalePrice](Plots/scatter_livarea_saleprice.png)  
- Clear positive relationship: **larger homes → higher prices**.  
- Diminishing returns appear for very large homes, with a few luxury outliers above \$1M.

---

### 5. Median Sale Price by Year (Line Plot)
![Median Sale Price by Year](Plots/line_median_saleprice_by_year.png)  
- Prices **peaked in 2007** and declined after, reflecting the **2008 housing crisis**.  

---

### 6. Count of Sales per Year (Bar Plot)
![Sales Count by Year](Plots/bar_sales_by_year.png)  
- Most sales occurred **2006–2009**, with a **drop in 2010**.  
- Matches slowing demand during the financial downturn.

---

### 7. Sale Price by Neighborhood (Boxplot)
![Sale Price by Neighborhood](Plots/box_saleprice_by_neighborhood.png)  
- **Neighborhood has a major effect** on property value.  
- StoneBr, NridgHt, and Crawfor command higher prices compared to other areas.  
- Location remains one of the strongest predictors of house prices.

---

### 8. Sale Price vs Year Built (Regplot)
![Year Built vs SalePrice](Plots/year_built_sale_price.png)  
- **Newer homes sell for more**, though returns flatten for very recent builds.  
- Some older, well-preserved homes remain luxury outliers.

---

### 9. Sale Price vs Year Remodeled (Regplot)
![Year Remodeled vs SalePrice](Plots/Year_remodeled_sale_price.png)  
- **Recently remodeled homes sell at higher prices**.  
- Suggests renovations before selling can yield meaningful returns.


###  Model Recommendation & Evaluation Summary

#### **Recommended Model**
- **Random Forest Regressor (Default Parameters)**
- Achieved **highest accuracy** and **best generalization** compared to Linear Regression.

---

#### **Performance Comparison**

| Model | Train R² | Test R² | Train RMSE | Test RMSE | Diagnosis |
|--------|-----------|----------|-------------|------------|------------|
| Linear Regression | 0.65 | 0.81 | 54,063 | 30,585 | Slight underfit |
| **Random Forest (Default)** | **0.96** | **0.84** | **17,321** | **28,203** | Mild overfit ✅ |

---

#### **Interpretation for Stakeholders**
- The Random Forest model explains about **84% of the variation** in sales values.
- This means it can **predict sales fairly accurately** and capture complex relationships between features.
- On average, its predictions differ from actual sales by around **\$28,000**.

---

#### **Chosen Metric: RMSE (Root Mean Squared Error)**
- Shows the **average prediction error in dollars**, same unit as the target.
- Penalizes large mistakes more heavily, making it **reliable for sales forecasting**.
- Easier for non-technical readers to interpret than R² or MSE.

---

#### **Overfitting / Underfitting Check**
- **Train R² (0.96)** vs **Test R² (0.84)** → small gap indicates **slight overfitting**, but within acceptable range.
- The model **generalizes well** and performs strongly on unseen data.

