# Prediction-of-Product-Sales
## Project Overview
As part of my data science bootcamp, this project aims to support a group of homeowners in Ames, Iowa, who are concerned about the declining value of their properties. The goal is to analyze raw housing market data to uncover actionable insights and deliver data-driven recommendations for increasing home value prior to sale.
<img width="800" height="450" alt="image" src="https://github.com/user-attachments/assets/fa2e7121-b93b-4f32-85fa-4af969ea18ec" />

## Objectives
- Explore and clean the Ames housing dataset
- Identify key features that influence property value
- Build predictive models to estimate home prices
- Deliver practical suggestions for value-boosting renovations or improvements
## 📊 Exploratory Visuals & Insights

### 1. Distribution of Sale Price
- Sale prices are **right-skewed**, with most houses selling between \$100K–\$250K.  
- A log transformation may help normalize the target variable for modeling.

---

### 2. Sale Price by Alley Type (Boxplot)
- Most homes **do not have alley access**.  
- Among those that do, **paved alleys sell for slightly more** than gravel, but the impact on value is limited.

---

### 3. Correlation Heatmap
- Features such as **Overall Quality, Living Area, and Garage Cars** show strong positive correlations with SalePrice.  
- Suggests buyers value **quality, size, and garage capacity** most.  
- ⚠️ Heatmaps only capture **linear** relationships. For non-linear effects, scatterplots or tree-based models are better.

---

### 4. Living Area vs Sale Price (Scatter)
- Clear positive relationship: **larger homes → higher prices**.  
- Diminishing returns appear for very large homes, with a few luxury outliers above \$1M.

---

### 5. Overall Condition vs Sale Price (Boxplot)
- **Condition scores** don’t align strongly with higher prices.  
- Suggests **quality (materials/finishes)** matters more to buyers than overall condition ratings.

---

### 6. Median Sale Price by Year (Line Plot)
- Prices **peaked in 2007** and declined after, reflecting the **2008 housing crisis**.  
- Timing plays an important role in resale value.

---

### 7. Count of Sales per Year (Bar Plot)
- Most sales occurred **2006–2009**, with a **drop in 2010**.  
- Matches slowing demand during the financial downturn.

---

### 8. Sale Price by Neighborhood (Boxplot)
- **Neighborhood has a major effect** on property value.  
- StoneBr, NridgHt, and Crawfor command higher prices compared to other areas.  
- Location remains one of the strongest predictors of house prices.

---

### 9. Sale Price vs Year Built (Regplot)
- **Newer homes sell for more**, though returns flatten for very recent builds.  
- Some older, well-preserved homes remain luxury outliers.

---

### 10. Sale Price vs Year Remodeled (Regplot)
- **Recently remodeled homes sell at higher prices**.  
- Suggests renovations before selling can yield meaningful returns.
