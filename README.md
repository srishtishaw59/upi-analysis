# UPI Transaction Analysis & Forecasting

A comprehensive data analysis project focused on analyzing and forecasting UPI (Unified Payments Interface) transaction data using machine learning techniques.

## 📊 Project Overview

This repository contains a detailed analysis of UPI transaction data, implementing Linear Regression models to forecast transaction volumes and values. The project demonstrates data preprocessing, feature engineering, model training, and visualization techniques for financial time series data.

## 🗂️ Repository Contents

### UPI_ANALYSIS.ipynb
A comprehensive Google Colab notebook containing UPI transaction analysis with the following components:

#### Data Analysis
- **Data Loading & Exploration**: Reads UPI transaction data from `upi_data_enhanced.csv`
- **Data Cleaning**: 
  - Duplicate removal
  - Missing value handling
  - Data type conversions
  - Month formatting and sorting

#### Key Features Analyzed
- **Volume (in Mn)**: Transaction volume in millions
- **Value (in Cr.)**: Transaction value in crores
- **No. of Banks live on UPI**: Number of active banks on the UPI platform
- **Month**: Temporal dimension for time series analysis

#### Machine Learning Models

**Model 1: Volume Forecasting**
- Predicts future transaction volume using lagged volume features
- Uses Linear Regression with historical volume as predictor
- Provides R-squared score for model performance evaluation

**Model 2: Value Forecasting (Single Feature)**
- Forecasts transaction value using previous month's value
- Implements lagged feature engineering
- Displays model coefficients and goodness-of-fit metrics

**Model 3: Value Forecasting (Multi-Feature)**
- Enhanced model using two features:
  - Lagged Value (previous month's transaction value)
  - Number of Banks live on UPI
- Provides feature importance analysis
- Shows coefficient interpretation for each predictor

#### Advanced Analytics
- **Prediction vs Actual Comparison**: Historical predictions with error analysis
- **Residual Analysis**: Calculates and analyzes prediction errors
- **Error Investigation**: Identifies months with largest prediction errors (both positive and negative)
- **Valuable Dataset Generation**: Creates comprehensive dataset with:
  - Actual values
  - Predicted values
  - Residuals (errors)
  - Month-wise breakdown

#### Visualizations
The notebook includes three key visualizations:

1. **Time Series Plot**: 
   - Actual vs. Predicted values over time
   - Historical fit analysis
   - Future forecast visualization
   - Trend identification

2. **Residual Distribution**: 
   - Histogram of prediction errors
   - KDE (Kernel Density Estimation) overlay
   - Error pattern analysis

3. **Scatter Plot**:
   - Lagged Value vs. Current Value relationship
   - Regression line visualization
   - Correlation analysis

## 🛠️ Technologies Used

- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computations
- **scikit-learn**: Linear Regression modeling
- **matplotlib**: Data visualization
- **seaborn**: Statistical data visualization
- **Google Colab**: Cloud-based notebook environment

## 📋 Requirements

```
pandas
numpy
scikit-learn
matplotlib
seaborn
```

**Note:** All libraries are pre-installed in Google Colab, so no installation is needed when running there.

## 🚀 Getting Started

### Running in Google Colab (Recommended)

1. **Open the notebook:**
   - Click the "Open in Colab" badge above, or
   - Go to [Google Colab](https://colab.research.google.com/)
   - Upload the `UPI_ANALYSIS.ipynb` file

2. **Upload your data:**
   - Create a folder named `sample_data` in the Colab file system
   - Upload `upi_data_enhanced.csv` to this folder
   - Or modify the file path in the notebook to match your data location

3. **Run the analysis:**
   - Execute cells sequentially from top to bottom
   - All required libraries are pre-installed in Colab

### Running Locally (Optional)

1. **Install dependencies:**
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn jupyter
   ```

2. **Prepare data:**
   - Ensure `upi_data_enhanced.csv` is in the `sample_data/` folder
   - The CSV should contain columns: Month, Volume (in Mn), Value (in Cr.), No. of Banks live on UPI

3. **Run the notebook:**
   ```bash
   jupyter notebook UPI_ANALYSIS.ipynb
   ```

## 📈 Model Performance

The Linear Regression models provide:
- **R-squared scores** indicating model fit quality
- **Feature coefficients** showing impact of each predictor
- **Residual analysis** for error pattern identification
- **Next period forecasts** for business planning

## 🔍 Key Insights

The analysis reveals:
- Historical trends in UPI transaction volumes and values
- Relationship between lagged values and current transactions
- Impact of banking infrastructure (number of banks) on transaction values
- Model accuracy through R-squared metrics
- Prediction errors for model improvement opportunities

## 📊 Data Structure

Expected CSV format for `upi_data_enhanced.csv`:
```
Month,Volume (in Mn),Value (in Cr.),No. of Banks live on UPI
Jan,1000,50000,200
Feb,1100,55000,205
...
```

## 🎯 Future Enhancements

Potential improvements:
- Implement additional ML algorithms (ARIMA, Prophet, LSTM)
- Add seasonality and trend decomposition
- Include external economic indicators
- Develop interactive dashboard with Plotly/Dash
- Add model comparison and ensemble methods
- Implement automated hyperparameter tuning

## 📝 Notes

- This project was developed in Google Colab for easy sharing and collaboration
- The notebook includes saved outputs and visualizations from previous runs
- Models assume the number of banks remains constant for next period forecasting
- Month indexing is used for time series visualization
- All financial values are rounded to 2 decimal places for clarity

## 🔗 Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/srishtishaw59/121/blob/main/UPI_ANALYSIS.ipynb)

## 👤 Author

**Srishti Shaw**
- GitHub: [@srishtishaw59](https://github.com/srishtishaw59)

## 📄 License

This project is available for educational and research purposes.

---

**Last Updated:** October 2025
