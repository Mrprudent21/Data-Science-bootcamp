# Titanic Survival Prediction - Professional Machine Learning Analysis

**Author:** Ayuba Abdulazeez  
**Date:** September 2025  
**Status:** Complete  
**Best Model Accuracy:** 81.56%

---

## Project Overview

A comprehensive machine learning analysis of the Titanic disaster, demonstrating professional data science practices from data exploration through model deployment. This project identifies key survival factors and builds predictive models with 81.56% accuracy.

## Business Problem

**Objective:** Analyze historical Titanic passenger data to:
- Identify factors that influenced survival during the disaster
- Build predictive models for emergency preparedness protocols
- Generate actionable insights for maritime safety planning

**Value Proposition:** Understanding survival patterns can inform modern emergency response protocols and resource allocation strategies.

## Key Findings

### Critical Survival Factors Identified:

1. **Gender Impact:** 74.2% female survival vs 18.9% male survival (4x advantage)
2. **Social Class:** 1st class (63%) vs 3rd class (24.2%) survival (2.6x advantage)  
3. **Age Factor:** Children had 59% survival vs 36.3% for adults
4. **Family Size:** Small families (2-4 people) had optimal 57.9% survival rate
5. **Economic Status:** Premium fare passengers had 3x better survival than low-fare

### Business Implications:
- "Women and children first" maritime protocol was followed
- Economic privilege significantly affected survival chances
- Optimal family groupings improved survival probability
- Social status indicators (titles, cabin assignments) predicted outcomes

## Technical Implementation

### Dataset
- **Source:** Kaggle Titanic Competition
- **Size:** 891 passengers, 12 original features
- **Target:** Binary survival classification (Survived: 0/1)

### Professional Approach

**Data Quality:**
- Smart demographic-based imputation for 19.9% missing ages
- Strategic feature transformation for 77.1% missing cabin data
- Mode-based filling for minimal missing values

**Feature Engineering (6 new features created):**
- Title extraction from names (social status indicator)
- Family size categorization (alone/small/large)
- Age group segmentation  
- Fare-based economic categories
- Child indicator (under 16)
- Mother identification

**Models Developed:**
1. Logistic Regression (Baseline) - **81.56% accuracy**
2. Random Forest Classifier - 78.21% accuracy

### Model Performance

**Best Model: Logistic Regression**
- **Accuracy:** 81.56%
- **ROC-AUC:** 0.864
- **Precision (Survived):** 78%
- **Recall (Survived):** 72%

**Key Predictive Features:**
1. Gender (22.3% importance)
2. Fare/Economic status (14.9%)
3. Social title (13.2%)
4. Age (11.5%)
5. Passenger class (7.1%)

## Project Structure

titanic-analysis/
- ├── data/
- │   ├── train.csv
- │   └── test.csv
- ├── notebooks/
- │   └── titanic_professional_analysis.ipynb
- ├── results/
- │   └── visualizations/
- ├── PROJECT_DOCUMENTATION.md
- └── README.md

## Technologies Used

- **Python 3.x**
- **Data Analysis:** pandas, numpy
- **Visualization:** matplotlib, seaborn
- **Machine Learning:** scikit-learn
- **Version Control:** Git/GitHub

## Key Skills Demonstrated

- Professional data preprocessing and cleaning
- Smart missing value imputation strategies
- Feature engineering from domain knowledge
- Exploratory data analysis with business insights
- Multiple model comparison and evaluation
- Professional documentation and code organization
- Version control and project management

## How to Run

1. Clone repository
2. Install requirements: `pip install pandas numpy matplotlib seaborn scikit-learn`
3. Open `notebooks/titanic_professional_analysis.ipynb`
4. Run cells sequentially

## Results & Insights

The analysis successfully identified that survival on the Titanic was primarily determined by:
- **Social factors:** Gender and class-based protocols
- **Economic factors:** Wealth indicators (fare, cabin, class)
- **Demographic factors:** Age and family composition

The 81.56% accuracy demonstrates that machine learning can effectively model complex human decision-making during crisis situations.

## Future Enhancements

- Deploy interactive web application using Streamlit
- Implement ensemble methods for improved accuracy
- Add cross-validation for robust performance estimation
- Create API for real-time survival probability predictions

## Contact

- https://github.com/Mrprudent21/Data-Science-bootcamp 
- https://www.linkedin.com/in/mrprudent-50857829a?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app 
- ayubaazeez11@gmail.com 

---

**Note:** This project demonstrates professional data science practices including systematic analysis, business thinking, and production-ready code quality.
