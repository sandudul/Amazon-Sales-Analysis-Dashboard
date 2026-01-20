# Amazon Sales Data Analysis & Preprocessing

A comprehensive data cleaning and preprocessing project analyzing Amazon product sales data, demonstrating expertise in data wrangling, feature engineering, and preparing datasets for business intelligence and machine learning applications.

## 📊 Project Overview

This project performs end-to-end data preprocessing on Amazon sales dataset containing 1,465 product records with customer reviews, pricing information, ratings, and product categories. The analysis transforms raw, messy data into a clean, analysis-ready format suitable for business insights and predictive modeling.

## 🎯 Key Achievements

- **Data Quality Improvement**: Cleaned and standardized 1,465 records across 23 features
- **Currency Normalization**: Processed pricing data by removing currency symbols (₹) and formatting inconsistencies
- **Feature Engineering**: Created calculated metrics including savings analysis and category hierarchies
- **Text Processing**: Handled large text fields with truncation and length analysis for NLP readiness
- **Missing Data Handling**: Implemented intelligent imputation strategies for rating data

## 🛠️ Technologies & Skills Demonstrated

### Programming & Libraries
- **Python 3.11+**
- **Pandas**: Data manipulation and transformation
- **NumPy**: Numerical operations and array processing
- **Jupyter Notebook**: Interactive data analysis and documentation

### Data Preprocessing Techniques
- String manipulation and regex for currency/percentage cleaning
- Type conversion (string → numeric)
- Missing value imputation using statistical methods
- Categorical data splitting and hierarchical structuring
- Feature engineering for derived metrics

## 📁 Dataset Features

### Original Data Issues Resolved
1. **Price Columns** (`discounted_price`, `actual_price`)
   - Removed currency symbols (₹) and thousands separators
   - Converted string format to numeric (float)
   - Range: ₹39 - ₹139,900

2. **Discount Percentage**
   - Stripped percentage symbols
   - Normalized to numeric values (0% - 94%)

3. **Rating Count**
   - Removed comma separators from large numbers
   - Converted to integer format
   - Range: 2 - 426,973 reviews

4. **Product Ratings**
   - Ensured numeric consistency (2.0 - 5.0 stars)
   - Filled missing values with statistical mean (4.10)

5. **Category Hierarchies**
   - Split pipe-delimited categories into structured hierarchy
   - Created `Main_Category` (9 unique) and `Sub_Category` (207 unique)
   - Enabled better product segmentation

6. **Text Fields Processing**
   - Created truncated versions for visualization
   - Generated length metrics for analysis
   - Preserved original data for NLP applications

### Engineered Features
- **Savings**: Calculated as `actual_price - discounted_price` (avg: ₹2,319.68)
- **Review Length Metrics**: Character counts for sentiment analysis readiness
- **Category Splits**: Main and sub-category extraction for hierarchical analysis

## 📈 Business Insights Enabled

The cleaned dataset supports:
- **Pricing Strategy Analysis**: Discount effectiveness and competitive pricing
- **Customer Behavior**: Rating trends and review engagement patterns
- **Product Performance**: Category-wise sales and rating analysis
- **Inventory Optimization**: High-performing product identification

## 🚀 How to Run

### Prerequisites
```bash
pip install pandas numpy jupyter
```

### Execution
1. Open `data Preprocessing.ipynb` in Jupyter Notebook
2. Run all cells sequentially
3. Cleaned data exports to `amazon_cleaned.csv` (UTF-8 encoding)

### Input/Output
- **Input**: `amazon.csv` (raw data, 1,467 rows)
- **Output**: `amazon_cleaned.csv` (processed data, 1,465 rows × 23 columns)

## 📊 Data Quality Metrics

| Metric | Before | After |
|--------|--------|-------|
| Numeric Columns | Mixed string/numeric | 100% numeric |
| Missing Ratings | 1 | 0 (imputed) |
| Category Structure | Flat pipe-delimited | Hierarchical (2 levels) |
| Price Format | Text with symbols | Clean numeric |
| Text Fields | Raw only | + Truncated + Metrics |

## 💡 Skills Highlighted

- **Data Cleaning**: Handling real-world messy data with inconsistent formats
- **ETL Pipeline**: Extract, Transform, Load workflow implementation
- **Feature Engineering**: Creating business-relevant calculated fields
- **Statistical Analysis**: Understanding data distributions and central tendencies
- **Python Programming**: Writing clean, reusable functions for data processing
- **Documentation**: Comprehensive code commenting and reporting

## 📂 Project Structure

```
amazon-sales-analysis/
│
├── amazon.csv                    # Raw dataset
├── amazon_cleaned.csv            # Cleaned dataset (output)
├── data Preprocessing.ipynb      # Main preprocessing notebook
└── README.md                     # Project documentation
```

## 🎓 Learning Outcomes

This project demonstrates proficiency in:
- Identifying and resolving common data quality issues
- Implementing reproducible data preprocessing pipelines
- Balancing data integrity with analytical requirements
- Creating production-ready datasets from raw sources
- Documenting technical work for stakeholder communication

## 📝 Future Enhancements

- Exploratory Data Analysis (EDA) with visualizations
- Sentiment analysis on review text
- Predictive modeling for product ratings
- Price optimization recommendations
- Interactive dashboard for business users

---

**Author**: Data Analyst Portfolio Project  
**Date**: January 2026  
**Tools**: Python, Pandas, NumPy, Jupyter Notebook  
**Status**: Completed ✓
