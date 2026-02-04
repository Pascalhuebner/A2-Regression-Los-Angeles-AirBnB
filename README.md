# A2 Regression Project: Los Angeles Airbnb Price Prediction Analysis

**Los Angeles, Team 8**
**Course: BAN 0200**
**Assignment: A2 - Regression Analysis**

---

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Executive Summary](#executive-summary)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Methodology](#methodology)
- [Key Findings](#key-findings)
- [Results](#results)
- [Business Recommendations](#business-recommendations)
- [Requirements](#requirements)
- [Team Information](#team-information)
- [References](#references)

---

## 🎯 Project Overview

This comprehensive analysis examines Airbnb listings in Los Angeles to build a regression model predicting listing prices. The project follows the **SEMMA methodology** (Sample, Explore, Modify, Model, Assess) and incorporates proximity to key Los Angeles attractions as a predictive feature.

### Project Objective

The primary objective is to develop a robust regression model that predicts Airbnb listing prices in Los Angeles by analyzing:

- Property characteristics (size, type, amenities)
- Host attributes (experience, reputation, response rates)
- Location factors (coordinates, neighborhoods)
- Proximity to major attractions

### Why Regression Analysis?

This project is highly suitable for regression analysis because:

1. **Continuous Target Variable**: Price is a continuous numerical variable
2. **Multiple Predictor Variables**: 79 features providing rich predictive information
3. **Linear Relationships**: Clear linear relationships between property characteristics and price
4. **Business Value**: Enables pricing optimization and investment decisions
5. **Sufficient Sample Size**: 45,886 listings for robust statistical modeling
6. **Real-World Application**: Fundamental business analytics problem with practical applications

---

## 📊 Executive Summary

Our analysis reveals that **location proximity to major attractions, property characteristics, and host reputation significantly influence Airbnb pricing** in Los Angeles. The best model achieved an **R² of 0.81**, explaining 81% of price variation.

### Key Highlights

- ✅ Comprehensive SEMMA methodology implementation
- ✅ 15+ regression models built and compared
- ✅ 16+ professional visualizations
- ✅ Rigorous statistical evaluation (R², Adjusted R², MSE, MAE, p-values, VIF)
- ✅ Actionable business recommendations
- ✅ Excellent model performance (R² = 0.81)

---

## 📁 Dataset

- **Source**: [Inside Airbnb](https://insideairbnb.com/)
- **Location**: Los Angeles, California
- **File**: `listings.csv`
- **Total Records**: 45,886 listings
- **Features**: 79 columns covering:
  - Property characteristics (size, type, amenities)
  - Location data (coordinates, neighborhoods, attraction distances)
  - Host attributes (experience, reputation, response rates)
  - Review metrics

> **⚠️ Important**: The `listings.csv` file must be downloaded from [Inside Airbnb](https://insideairbnb.com/) and placed in the project directory for the analysis to work. The dataset is not included in this repository.

### Key Attractions Analyzed

As specified for Los Angeles Team 2, the analysis focuses on proximity to:

1. **Hollywood Sign** (34.1341° N, 118.3215° W)
2. **Griffith Observatory** (34.1184° N, 118.3004° W)
3. **Getty Center** (34.0780° N, 118.4742° W)
4. **Santa Monica Pier** (34.0089° N, 118.4973° W)
5. **Disneyland** (33.8121° N, 117.9190° W)

---

## 📂 Project Structure

```
A2 Regression Project/
│
├── A2_Regression_Los_Angeles_Analysis.ipynb    # Main Jupyter notebook
├── listings.csv                                 # Airbnb dataset
└── requirements.txt                             # Python dependencies
```

---

## 🚀 Installation

### Prerequisites

- Python 3.8 or higher
- pip (Python package installer)
- Jupyter Notebook (optional, for interactive analysis)

### Step 1: Clone or Download the Project

Navigate to the project directory:

```bash
cd "A2 Regression Project"
```

### Step 2: Download the Dataset

**Download `listings.csv` from Inside Airbnb:**

1. Visit [Inside Airbnb - Los Angeles](https://insideairbnb.com/get-the-data/)
2. Download the `listings.csv` file for Los Angeles
3. Place the file in the project directory (same folder as the notebook)

> **Note**: The dataset file (`listings.csv`) is required for the analysis to run. Make sure it's in the same directory as `A2_Regression_Los_Angeles_Analysis.ipynb`.

### Step 3: Create Virtual Environment (Recommended)

**macOS/Linux:**

```bash
python3 -m venv venv
source venv/bin/activate
```

**Windows:**

```bash
python -m venv venv
venv\Scripts\activate
```

### Step 4: Install Dependencies

```bash
pip install -r requirements.txt
```

This will install:

- pandas >= 2.0.0
- numpy >= 1.24.0
- matplotlib >= 3.7.0
- seaborn >= 0.12.0
- scikit-learn >= 1.3.0
- scipy >= 1.10.0
- statsmodels >= 0.14.0
- jupyter >= 1.0.0
- ipykernel >= 6.0.0
- python-docx >= 1.0.0
- geopy >= 2.3.0

---

## 💻 Usage

### Option 1: Jupyter Notebook (Interactive)

1. Start Jupyter Notebook:

   ```bash
   jupyter notebook
   ```
2. Open `A2_Regression_Los_Angeles_Analysis.ipynb`
3. Run cells sequentially or execute all cells

### Option 2: Python Script

Run the Python script directly:

```bash
python A2_Regression_Los_Angeles_Analysis.py
```

### Option 3: View HTML Export

Open `A2_Regression_Los_Angeles_Analysis.html` in any web browser to view the complete analysis with outputs.

---

## 🔬 Methodology

The analysis systematically follows the **SEMMA framework**:

### 1. Sample (Data Loading)

- Loaded 45,886 listings with 79 features
- Initial data exploration and understanding

### 2. Explore (Exploratory Data Analysis)

- **Univariate Analysis**: Distribution of individual variables
- **Bivariate Analysis**: Relationships between pairs of variables
- **Multivariate Analysis**: Complex relationships across multiple variables
- **16+ Visualizations**: Professional charts and graphs

### 3. Modify (Data Preprocessing)

- **Missing Values**:
  - Dropped columns with >50% missing data
  - Imputed remaining missing values appropriately
- **Outlier Treatment**: Removed outliers at 1st and 99th percentiles
- **Feature Engineering**:
  - Calculated distances to major attractions
  - Created host experience metrics
  - Derived price per person feature

### 4. Model (Regression Modeling)

- Built and compared **15 different regression models**
- Various feature combinations tested
- Model types include:
  - Simple Linear Regression
  - Multiple Linear Regression
  - Polynomial Regression
  - Regularized Regression (Ridge, Lasso)

### 5. Assess (Model Evaluation)

- **Performance Metrics**:
  - R² (Coefficient of Determination)
  - Adjusted R²
  - MSE (Mean Squared Error)
  - MAE (Mean Absolute Error)
- **Statistical Significance**: p-values for coefficients
- **Multicollinearity Checks**: Variance Inflation Factor (VIF)

---

## 🔍 Key Findings

### Data Insights

1. **Price Distribution**: Right-skewed with median price around **$155**
2. **Property Characteristics**: Strong correlation between bathrooms, accommodates, bedrooms and price
3. **Location Impact**: Proximity to attractions (especially Santa Monica Pier and Getty Center) significantly impacts pricing
4. **Property Type**: Entire home/apt properties command significantly higher prices
5. **Host Characteristics**: Superhost status and response rate influence pricing

### Model Performance

- **Best Model R²**: **0.81** (explains 81% of price variation)
- **Adjusted R²**: Accounts for model complexity
- **Low MSE/MAE**: Indicates good prediction accuracy
- **Statistically Significant**: Key predictors have p-values < 0.05
- **Low Multicollinearity**: VIF values within acceptable range

### Significant Predictors

1. **Property Size**: Number of bathrooms, bedrooms, accommodates
2. **Property Type**: Entire home/apt vs. private/shared rooms
3. **Location**: Proximity to major attractions
4. **Host Reputation**: Superhost status, review scores
5. **Host Experience**: Response rate, years as host

---

## 📈 Results

### Model Comparison Summary

The analysis compared 15 different regression models with various feature combinations. The final selected model demonstrates:

- **High Predictive Power**: R² = 0.81
- **Good Generalization**: Strong performance on test data
- **Statistical Validity**: All assumptions met
- **Business Relevance**: Interpretable coefficients

### Visualization Highlights

The analysis includes 16+ professional visualizations covering:

- Price distribution and summary statistics
- Correlation matrices
- Scatter plots for key relationships
- Box plots for categorical variables
- Residual plots for model diagnostics
- Feature importance charts

---

## 💼 Business Recommendations

Based on the analysis, we provide the following actionable recommendations:

### 1. Location Optimization

**Hosts should optimize their properties' proximity to major attractions**, especially:

- Santa Monica Pier
- Getty Center
- Hollywood Sign

### 2. Review Score Management

**Maintaining high review scores is crucial for premium pricing**. Hosts should:

- Focus on guest satisfaction
- Respond promptly to reviews
- Address negative feedback quickly

### 3. Property Type Strategy

**Entire home/apt properties command significantly higher prices**. Investors should consider:

- Converting shared spaces to entire units where possible
- Highlighting property type in listings

### 4. Superhost Status

**Superhost status provides pricing advantages**. Hosts should:

- Maintain eligibility requirements
- Leverage superhost badge in marketing

### 5. Pricing Strategy

- Use the regression model to set competitive prices
- Adjust prices based on proximity to attractions
- Consider seasonal variations (future enhancement)

---

## ✅ Requirements

### Assignment Requirements Met

- ✅ Follow SEMMA process strictly
- ✅ At least 10 visualizations (16+ provided)
- ✅ Handle missing values and outliers appropriately
- ✅ Build up to 15 regression models
- ✅ Evaluate using R², Adjusted R², MSE, p-values
- ✅ Check for multicollinearity (VIF)
- ✅ Provide business recommendations
- ✅ Word count: 1,500-2,000 words

### Technical Requirements

- ✅ Comprehensive data cleaning and preprocessing
- ✅ Feature engineering (attraction distances, derived features)
- ✅ Multiple model comparison
- ✅ Statistical validation
- ✅ Professional visualizations
- ✅ Clear documentation

---

## 👥 Team Information

- **Team**: Los Angeles Team 8
- **Course**: BAN 0200 - Business Analytics
- **Assignment**: A2 - Regression Analysis
- **Author**: Pascal Huebner
- **Year**: 2025

---

## 📚 References

- **Dataset**: [Inside Airbnb](https://insideairbnb.com/)
- **SEMMA Methodology**: SAS Institute
- **Statistical Analysis**: scikit-learn, statsmodels
- **Visualization**: matplotlib, seaborn
- **Geographic Analysis**: geopy

---

## 📝 Notes

- **⚠️ The dataset (`listings.csv`) must be downloaded from [Inside Airbnb](https://insideairbnb.com/) and placed in the same directory as the notebook/script for the analysis to work**
- All visualizations are saved automatically when running the notebook
- The analysis can be run end-to-end without manual intervention
- Results may vary slightly due to random seeds in train-test splits

---

## 🤝 Contributing

This is an academic project. For questions or suggestions, please contact the project author.

---

## 📄 License

This project is for academic purposes only. The dataset is from Inside Airbnb and is used for educational analysis.

---

**Last Updated**: February 2025
