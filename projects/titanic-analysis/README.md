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
