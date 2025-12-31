# Restaurant Revenue Inferential Analysis

[![R](https://img.shields.io/badge/R-4.0%2B-blue.svg)](https://www.r-project.org/)
[![Statistical Analysis](https://img.shields.io/badge/Analysis-Statistical%20Inference-brightgreen.svg)]()
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)]()

A comprehensive statistical analysis identifying key drivers of restaurant customer footfall using advanced Poisson regression modeling and inferential statistics. This project demonstrates rigorous statistical methodology, data analysis skills, and business insights relevant to the food service industry.

## 📊 Project Overview

This analysis investigates which explanatory variables have the strongest association with monthly customer visits to restaurants. Using a synthetic dataset of restaurant operational metrics, I employ quasi-Poisson regression to model count data while addressing overdispersion, providing statistically robust insights into factors driving customer traffic.

**Research Question:** *Which explanatory variable has the strongest association with the number of customers visiting a restaurant per month, based on the significance and magnitude of coefficients in a Poisson regression model?*

## 🎯 Key Findings

- **Monthly Revenue** shows the strongest positive association with customer footfall (p < 0.001)
  - Each $1 increase in revenue associates with a 1.0042x multiplicative increase in customer count
- **Promotions** significantly increase customer visits (p = 0.034)
  - Restaurants with active promotions see ~4.5% more customers
- **Overdispersion detected** (dispersion parameter = 5.58), successfully addressed using quasi-Poisson modeling
- Identified multicollinearity issues affecting Menu Price and Marketing Spend coefficients

## 🛠️ Technologies & Methodologies

**Statistical Methods:**
- Quasi-Poisson Regression (GLM with log link)
- Deviance Residual Analysis
- Overdispersion Testing
- Coefficient Significance Testing

**R Packages:**
- `tidyverse` - Data manipulation and visualization
- `broom` - Statistical model tidying
- `ggcorrplot` - Correlation visualization
- `ggplot2` - Advanced graphics

## 📁 Project Structure

```
restaurant-revenue-analysis/
├── README.md
├── report/
│   ├── Final Report Akshat.ipynb    # Complete analysis with R code
│   └── Final Report Akshat.html     # Rendered HTML report
└── data/                             # Dataset (download via Kaggle API)
```

## 📈 Analysis Workflow

1. **Data Acquisition** - Dataset loaded via Kaggle API
2. **Exploratory Data Analysis** - Correlation analysis, variable distributions
3. **Model Development** - Initial Poisson regression
4. **Overdispersion Detection** - Identified dispersion parameter >> 1
5. **Model Refinement** - Quasi-Poisson regression implementation
6. **Model Assessment** - Residual diagnostics and validation
7. **Interpretation** - Statistical inference and business implications

## 🔍 Dataset

**Source:** [Restaurant Revenue Prediction Dataset](https://www.kaggle.com/datasets/mrsimple07/restaurants-revenue-prediction) (Kaggle)

**Variables:**
- `Number_of_Customers` (Response) - Monthly customer count
- `Menu_Price` - Average menu prices
- `Marketing_Spend` - Marketing expenditure
- `Cuisine_Type` - Restaurant cuisine category
- `Average_Customer_Spending` - Average spend per customer
- `Promotions` - Binary indicator for promotional activities
- `Reviews` - Number of customer reviews
- `Monthly_Revenue` - Simulated monthly revenue

## 🚀 Getting Started

### Prerequisites

- R (version 4.0+)
- Kaggle API credentials (for data download)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/restaurant-revenue-analysis.git
cd restaurant-revenue-analysis
```

2. Install required R packages:
```r
install.packages(c("tidyverse", "broom", "ggcorrplot"))
```

3. Set up Kaggle API credentials (in the notebook):
```r
kaggle_api <- '{"username":"YOUR_USERNAME","key":"YOUR_API_KEY"}'
```

### Running the Analysis

Open and run `report/Final Report Akshat.ipynb` in RStudio or Jupyter with R kernel.

## 📊 Key Visualizations

The analysis includes:
- Correlation heatmaps identifying multicollinearity
- Coefficient estimate plots with confidence intervals
- Deviance residual plots for model diagnostics
- Distribution analyses of predictor variables

## 💡 Statistical Insights

**Model Performance:**
- Successfully addressed overdispersion through quasi-Poisson modeling
- Identified significant predictors at α = 0.05 level
- Conducted comprehensive residual diagnostics

**Limitations & Future Work:**
- Multicollinearity between revenue, marketing spend, and menu price
- Future analyses could employ variable selection techniques (stepwise regression, LASSO)
- Potential for causal inference with experimental data

## 📝 Academic Context

- **Course:** STAT V 301 - Statistical Inference
- **Institution:** University of British Columbia
- **Date:** April 2025
- **Focus:** Applied inferential statistics in business analytics

## 📄 License

This project is available under the MIT License.

## 🤝 Contact

**Akshat Kalra**
- GitHub: [@yourusername](https://github.com/yourusername)
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/yourprofile)
- Email: your.email@example.com

---

*This project demonstrates proficiency in statistical modeling, R programming, data analysis, and business analytics—skills applicable to data science and analytics roles.*
