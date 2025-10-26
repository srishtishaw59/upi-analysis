# UPI Transaction Analysis & Forecasting

A comprehensive data analysis project focused on analyzing and forecasting UPI (Unified Payments Interface) transaction data using machine learning techniques.

## 📊 Project Overview

This repository contains a detailed analysis of UPI transaction data, implementing Linear Regression models to forecast transaction volumes and values. The project demonstrates data preprocessing, feature engineering, model training, and visualization techniques for financial time series data.

## 🗂️ Repository Contents

### 1. UPI_ANALYSIS.ipynb
The main Jupyter notebook containing comprehensive UPI transaction analysis with the following components:

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

### 2. Air-canvas.py
A computer vision project implementing a virtual air canvas using OpenCV. This allows users to draw in the air using color tracking.

**Features:**
- Real-time webcam-based color detection
- HSV color space trackbars for dynamic color adjustment
- Multi-color drawing support (Blue, Green, Red, Yellow)
- Clear canvas functionality
- Separate windows for tracking, painting, and mask visualization

**Technical Implementation:**
- Color detection using HSV thresholding
- Contour detection for pointer identification
- Morphological operations (erosion, dilation, opening)
- Deque-based point storage for smooth line drawing
- Multiple color channels management

**Note:** This file appears to be unrelated to the UPI analysis and may have been included accidentally.

## 🛠️ Technologies Used

### Data Science & Machine Learning
- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computations
- **scikit-learn**: Linear Regression modeling
- **matplotlib**: Data visualization
- **seaborn**: Statistical data visualization

### Computer Vision (Air-canvas.py)
- **OpenCV (cv2)**: Image processing and computer vision
- **numpy**: Array operations
- **collections.deque**: Efficient point storage

## 📋 Requirements

```
pandas
numpy
scikit-learn
matplotlib
seaborn
opencv-python (for Air-canvas.py)
jupyter
```

## 🚀 Getting Started

### Running the UPI Analysis

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

4. **Execute cells sequentially** to perform the complete analysis

### Running Air Canvas

1. **Install OpenCV:**
   ```bash
   pip install opencv-python
   ```

2. **Run the script:**
   ```bash
   python Air-canvas.py
   ```

3. **Controls:**
   - Adjust HSV trackbars to calibrate color detection
   - Use the colored marker in front of webcam to draw
   - Click "CLEAR" button to reset canvas
   - Press 'q' to quit

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

- The notebook includes outputs and visualizations from previous runs
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
