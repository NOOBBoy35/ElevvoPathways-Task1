# Student Performance Analysis - Level 1 Task 1

## 📊 Project Overview

This project analyzes student performance factors using machine learning techniques to predict exam scores based on various academic and personal factors. The analysis includes data cleaning, visualization, and multiple regression models.

## 📁 Files

- `Level1-Task1-fixed.ipynb` - Main Jupyter notebook with complete analysis
- `StudentPerformanceFactors.csv` - Dataset containing student performance data
- `README.md` - This documentation file

## 🎯 Project Requirements

### Core Requirements:
1. **Data Cleaning & Basic Visualization**
   - Load and examine the dataset
   - Handle missing values
   - Create visualizations for data distribution
   - Analyze relationships between variables

2. **Dataset Splitting**
   - Split data into training and testing sets (80/20 split)
   - Use Hours_Studied as the primary feature

3. **Linear Regression Model**
   - Train a linear regression model
   - Predict exam scores based on study hours

4. **Model Evaluation & Visualization**
   - Visualize actual vs predicted scores
   - Calculate performance metrics (MAE, MSE, R²)

### Bonus Requirements:
1. **Polynomial Regression**
   - Implement polynomial regression (degree=2)
   - Compare performance with linear regression

2. **Multi-Feature Analysis**
   - Use multiple features including:
     - Hours_Studied
     - Attendance
     - Sleep_Hours
     - Previous_Scores
     - Physical_Activity
     - Gender (encoded)

## 📈 Dataset Information

**File:** `StudentPerformanceFactors.csv`
**Size:** 6,607 students, 20 features

### Key Features:
- **Target Variable:** `Exam_Score` (55-101 range)
- **Numerical Features:** Hours_Studied, Attendance, Sleep_Hours, Previous_Scores, Physical_Activity, Tutoring_Sessions
- **Categorical Features:** Gender, Parental_Involvement, Access_to_Resources, Motivation_Level, etc.

### Data Quality:
- Missing values in: Teacher_Quality (78), Parental_Education_Level (90), Distance_from_Home (67)
- All target and primary features are complete

## 🚀 How to Run

### Prerequisites:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Running the Analysis:
1. **Using Jupyter Notebook:**
   ```bash
   jupyter notebook Level1-Task1-fixed.ipynb
   ```

2. **Using Python Script:**
   ```bash
   python -c "
   import pandas as pd
   df = pd.read_csv('StudentPerformanceFactors.csv')
   print('Dataset loaded successfully!')
   print(f'Shape: {df.shape}')
   "
   ```

## 📊 Analysis Results

### Model Performance:

1. **Simple Linear Regression (Hours_Studied only):**
   - MAE: 2.45
   - MSE: 10.86
   - R²: 0.23

2. **Polynomial Regression (degree=2):**
   - MAE: 2.44
   - MSE: 10.84
   - R²: 0.23

3. **Multi-Feature Model (5 features + Gender):**
   - MAE: 1.35
   - MSE: 5.33
   - R²: 0.62

### Key Insights:
- **Study hours have moderate correlation** with exam scores (R² = 0.23)
- **Multi-feature model significantly improves** prediction accuracy (R² = 0.62)
- **Gender encoding** helps improve model performance
- **Previous scores and attendance** are strong predictors

## 📈 Visualizations Included

1. **Distribution of Final Exam Scores** - Histogram with KDE
2. **Hours Studied vs Exam Score** - Scatter plot
3. **Actual vs Predicted Scores** - Model performance visualization
4. **Polynomial Regression Plot** - Non-linear relationship analysis

## 🔧 Technical Details

### Libraries Used:
- `pandas` - Data manipulation and analysis
- `matplotlib` & `seaborn` - Data visualization
- `scikit-learn` - Machine learning models and evaluation
- `numpy` - Numerical computations

### Model Pipeline:
1. Data loading and inspection
2. Missing value analysis
3. Feature engineering (one-hot encoding for categorical variables)
4. Train-test split (80/20)
5. Model training and evaluation
6. Performance visualization

## 📝 Code Structure

The notebook is organized into clear sections:
- **Load Dataset** - Data import and initial inspection
- **Requirement 1** - Data cleaning and visualization
- **Requirement 2** - Dataset splitting
- **Requirement 3** - Linear regression training
- **Requirement 4** - Model evaluation and visualization
- **Bonus 1** - Polynomial regression
- **Bonus 2** - Multi-feature analysis

## 🎓 Learning Outcomes

This project demonstrates:
- **Data preprocessing** and cleaning techniques
- **Exploratory data analysis** with visualizations
- **Machine learning model** development and evaluation
- **Feature engineering** and selection
- **Model comparison** and performance analysis

## 📞 Support

If you encounter any issues:
1. Ensure all required libraries are installed
2. Verify the dataset file is in the same directory as the notebook
3. Check that the file path is correct for your system

---

**Note:** This project was originally developed in Google Colab and has been adapted for local execution with the dataset file stored in the same directory. 