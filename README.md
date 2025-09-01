# Boston_Housing_Price_Prediction
This project applies **supervised machine learning** to predict **median house prices** in Boston suburbs using the **Boston Housing dataset**. The analysis uses **Decision Tree Regressor** and other regression techniques to explore how features influence housing prices.  

---

## Dataset  
- Source: [Scikit-learn Boston Housing dataset (deprecated in latest versions)](https://scikit-learn.org/stable/datasets/toy_dataset.html#boston-house-prices-dataset)  
- Features include:  
  - CRIM: Per capita crime rate  
  - ZN: Proportion of residential land zoned for lots  
  - INDUS: Proportion of non-retail business acres per town  
  - CHAS: Charles River dummy variable  
  - NOX: Nitric oxide concentration  
  - RM: Average number of rooms per dwelling  
  - AGE: Proportion of owner-occupied units built before 1940  
  - DIS: Weighted distances to employment centers  
  - RAD: Index of accessibility to radial highways  
  - TAX: Property tax rate  
  - PTRATIO: Pupil-teacher ratio  
  - B: Proportion of Black population  
  - LSTAT: % lower status population  
- Target: **MEDV** = Median value of owner-occupied homes (in $1000s).  

---

## Summary  
The project demonstrates:  
1. Loading and preparing the dataset.  
2. Exploratory Data Analysis (EDA) using **visualizations**.  
3. Training a **Decision Tree Regressor** to predict house prices.  
4. Evaluating performance using metrics such as **Mean Squared Error (MSE)** and **R² score**.  
5. Visualizing the decision tree structure to interpret regression splits.  

---

##  Results  
- The Decision Tree model captured non-linear relationships between housing features and prices.  
- Features like **RM (average rooms per dwelling)**, **LSTAT (% lower status population)**, and **PTRATIO** had the highest impact on house price prediction.  
- With pruning (`max_depth`, `min_samples_split`), the model achieved a good trade-off between accuracy and generalization.  

---

## Analysis and Insights  
- Houses with **more rooms (higher RM)** are strongly correlated with higher prices.  
- Higher **LSTAT** (lower socioeconomic status) leads to lower housing prices.  
- **Proximity to Charles River (CHAS = 1)** slightly increases house prices.  
- Without tuning, deep decision trees tend to overfit. Regularization improves predictive performance.  

---

## Recommendations  
- Use **Random Forest Regressor** or **Gradient Boosting Regressor** to improve performance.  
- Perform **hyperparameter tuning** with GridSearchCV to optimize depth and splitting criteria.  
- Try **feature scaling** and **normalization** to improve learning for certain models.  
- Incorporate **cross-validation** for more reliable accuracy estimation.  
