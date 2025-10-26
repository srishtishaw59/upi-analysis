# UPI Transaction Analysis & Forecasting

A data analysis project that analyzes UPI (Unified Payments Interface) transaction data and uses Linear Regression to forecast future transaction volumes and values.

## 📊 Project Overview

This project analyzes UPI transaction data and builds simple Linear Regression models to predict future transaction volumes and values. It includes basic data cleaning, feature engineering using lagged values, and visualizations to understand model performance.

## 🗂️ Repository Contents

### UPI_ANALYSIS.ipynb
A Google Colab notebook with UPI transaction analysis.

#### What the notebook does:

**Data Exploration**
- Loads UPI data from `upi_data_enhanced.csv`
- Checks for duplicates and missing values
- Basic data inspection (shape, columns, data types)
- Descriptive statistics

**Data Columns Used:**
- `Month` - Month of transactions
- `Volume (in Mn)` - Transaction volume in millions
- `Value (in Cr.)` - Transaction value in crores
- `No. of Banks live on UPI` - Number of banks on UPI

**Three Linear Regression Models:**

1. **Volume Forecasting Model**
   - Uses previous month's volume to predict next month's volume
   - Creates a lagged feature from volume data
   - Shows R-squared score and forecast

2. **Value Forecasting Model (Simple)**
   - Uses previous month's value to predict next month's value
   - Basic single-feature model

3. **Value Forecasting Model (Two Features)**
   - Uses both lagged value AND number of banks
   - Shows how much each feature impacts predictions
   - Calculates prediction errors for each month
   - Identifies months with largest errors

**Visualizations:**
- Time series plot showing actual vs predicted values with future forecast point
- Histogram of prediction errors
- Scatter plot of lagged value vs actual value with regression line

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

## 📈 What You Get

- R-squared scores showing how well the model fits
- Feature coefficients showing impact of lagged values and number of banks
- Prediction errors for each historical month
- Forecast for the next period
- Charts showing actual vs predicted values

## 📊 Data Structure

Expected CSV format for `upi_data_enhanced.csv`:
```
Month,Volume (in Mn),Value (in Cr.),No. of Banks live on UPI
Jan,1000,50000,200
Feb,1100,55000,205
...
```

## 🎯 Future Plans

- Try better ML models like ARIMA or LSTM
- Add more factors like festivals, economic events
- Build an interactive dashboard
- Include seasonal patterns
- Use real-time data if available

## 📝 Notes

- Built in Google Colab
- The notebook has outputs from previous runs saved
- For future predictions, the model assumes number of banks stays the same
- Financial values are rounded to 2 decimal places

## 🔗 Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/srishtishaw59/121/blob/main/UPI_ANALYSIS.ipynb)

## 👤 Author

**Srishti Shaw**
- GitHub: [@srishtishaw59](https://github.com/srishtishaw59)

## 📄 License

This project is available for educational and research purposes.

---

**Last Updated:** October 2025
