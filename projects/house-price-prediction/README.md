# House Price Prediction - Advanced Regression Analysis

**Author:** Ayuba Abdulazeez  
**Date:** October 2025  
**Status:** Complete  
**Best Model R²:** 91.4%  
**RMSE:** $26,259.81

---

## Project Overview

An advanced regression machine learning project demonstrating professional data science practices on the Ames Housing dataset. This project predicts house prices with 91.4% accuracy (R²), exceeding industry targets through strategic feature engineering and model optimization.

## Business Problem

**Objective:** Build accurate house price prediction models to:
- Help real estate agents price properties competitively
- Enable buyers to identify fair market values
- Assist sellers in setting realistic asking prices
- Support investment decisions with data-driven insights

**Value Proposition:** Accurate price predictions reduce market inefficiencies and enable better financial decisions for all stakeholders in real estate transactions.

## Key Achievements

### Performance Metrics (Exceeded All Targets):

- **R² Score:** 0.914 (Target: >0.85) ✅ **+7.6% above target**
- **RMSE:** $26,259 (Target: <$30,000) ✅ **$3,740 better than target**
- **MAE:** $15,619 (Average prediction error)
- **Accuracy:** 91.4% of price variance explained

### Critical Success Factors:

1. **Target Transformation:** Log-transformed highly skewed prices (skewness 1.74 → -0.015)
2. **Smart Feature Engineering:** Created 10 new features, 3 became top predictors
3. **Strategic Missing Data:** Dropped 4 useless features (>80% missing), intelligently imputed rest
4. **Model Selection:** Random Forest captured non-linear relationships 33% better than linear models

## Dataset Details

- **Source:** Ames Housing Dataset (Kaggle)
- **Size:** 2,930 houses
- **Original Features:** 82 (reduced to 78 after cleaning)
- **Final Features:** 88 (after engineering 10 new features)
- **Target:** SalePrice (ranging $12,789 - $755,000)

## Technical Implementation

### Data Quality Challenges Solved:

**Missing Data (27 features affected):**
- Dropped features >80% missing (Pool QC, Misc Feature, Alley, Fence)
- Neighborhood-based imputation for Lot Frontage (preserved local patterns)
- Logical fills (Garage Year Built = House Year Built)
- Strategic 'None' fills for categorical features (missing = "doesn't have")

**Target Variable Issues:**
- Highly right-skewed distribution (1.74 skewness)
- Wide price range (59x difference between min/max)
- Solution: Log transformation achieved near-perfect normality

### Feature Engineering (10 New Features):

**Top Performing Engineered Features:**
1. **Total_SF** (29.9% importance) - Combined all living space areas
2. **Quality_Index** (5.0% importance) - Overall Quality × Condition interaction
3. **Total_Bathrooms** (2.2% importance) - Simplified bathroom counting

**Additional Features:**
- House_Age, Years_Since_Remod (temporal features)
- Total_Porch_SF (combined all porch types)
- Binary indicators (Has_Pool, Has_Garage, Has_Basement, Has_Fireplace)

### Models Developed & Compared:

| Model | RMSE | R² | MAE |
|-------|------|-----|-----|
| **Random Forest** | **$26,259** | **0.914** | **$15,619** |
| Ridge Regression | $38,730 | 0.813 | $17,843 |
| Linear Regression | $38,932 | 0.811 | $17,833 |

**Winner:** Random Forest Regressor (100 trees, max_depth=15)

### Top 10 Most Important Features:

1. Overall Qual (43.8%) - Quality rating dominates prediction
2. Total_SF (29.9%) - *Engineered feature*
3. Quality_Index (5.0%) - *Engineered feature*
4. Total_Bathrooms (2.2%) - *Engineered feature*
5. Garage Area (1.7%)
6. Lot Area (1.6%)
7. Gr Liv Area (1.3%)
8. House_Age (1.3%) - *Engineered feature*
9. Garage Cars (1.2%)
10. Garage Yr Blt (1.0%)

**Note:** 4 of top 10 features are engineered - demonstrating value of domain-driven feature creation.

## Project Structure
```
house-price-prediction/
├── data/
│   └── AmesHousing.csv
├── notebooks/
│   └── house_price_professional_analysis.ipynb
├── results/
│   └── visualizations/
├── PROJECT_DOCUMENTATION.md
└── README.md
```

## Technologies Used

- **Python 3.x**
- **Data Analysis:** pandas, numpy, scipy
- **Visualization:** matplotlib, seaborn
- **Machine Learning:** scikit-learn
  - Regression: LinearRegression, Ridge, RandomForestRegressor
  - Preprocessing: StandardScaler, LabelEncoder
  - Metrics: RMSE, R², MAE
- **Version Control:** Git/GitHub

## Key Skills Demonstrated

- **Regression analysis** (vs classification in Titanic project)
- **Advanced feature engineering** from domain knowledge
- **Target variable transformation** for skewed distributions
- **Strategic missing data handling** (27 features with missing values)
- **Feature importance analysis** for model interpretability
- **Multiple model comparison** with proper evaluation metrics
- **Professional documentation** and reproducible workflow

## How to Run

1. Clone repository
2. Install requirements: `pip install pandas numpy scipy matplotlib seaborn scikit-learn`
3. Open `notebooks/house_price_professional_analysis.ipynb`
4. Run cells sequentially (Kernel → Restart & Run All)

## Results & Business Insights

The Random Forest model achieved 91.4% accuracy in predicting house prices, with average error of $15,619. For houses averaging $180,796, this represents ~8.6% error rate - excellent for real estate pricing.

**Key Pricing Factors Identified:**
1. **Quality matters most** - Overall quality rating is 1.5x more important than all other features
2. **Size is critical** - Total square footage explains 30% of model decisions
3. **Combined indicators work** - Engineered features (Quality Index, Total SF, Total Bathrooms) outperform individual metrics
4. **Age impacts value** - Newer homes command premium prices
5. **Garage matters** - Garage size/presence significantly affects price

**Business Applications:**
- Real estate agents can justify pricing recommendations with data
- Buyers can identify overpriced/underpriced properties
- Sellers can optimize asking prices for faster sales
- Investors can estimate ROI on property improvements

## Comparison with Titanic Project

**Complexity Evolution:**

| Aspect | Titanic | House Prices |
|--------|---------|--------------|
| Task Type | Classification | Regression |
| Features | 12 original | 82 original |
| Missing Data | 3 features | 27 features |
| Target Variable | Binary (0/1) | Continuous ($) |
| Best Model Accuracy | 81.56% | 91.4% R² |
| Feature Engineering | 6 features | 10 features |

This project demonstrated ability to handle significantly more complexity while maintaining professional standards.

## Future Enhancements

- **Hyperparameter Optimization:** GridSearchCV for Random Forest tuning
- **Ensemble Methods:** Stack multiple models for improved performance
- **Advanced Features:** Polynomial features, interaction terms
- **Cross-Validation:** K-fold CV for robust performance estimates
- **Outlier Handling:** Special treatment for luxury homes (>$340K)
- **Deployment:** Streamlit web app for interactive price predictions

## Lessons Learned

**Technical:**
- Log transformation is critical for skewed regression targets
- Feature engineering often outperforms complex models
- Random Forest handles non-linear relationships well
- Domain knowledge drives valuable feature creation

**Professional:**
- Strategic decisions (what to drop, what to keep) matter more than perfect imputation
- Understanding data distribution before modeling prevents issues
- Simple engineered features can be more powerful than complex ones
- Documentation during work (not after) saves time

## Contact

**GitHub:** [Your GitHub Profile]  
**LinkedIn:** [Your LinkedIn]  
**Email:** [Your Email]

---

**Note:** This project demonstrates progression from classification (Titanic) to regression, handling increased complexity while maintaining professional standards and exceeding performance targets.
