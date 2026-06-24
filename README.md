# 🏠 House Price Prediction using Machine Learning

A complete end-to-end Machine Learning project that predicts house prices using various property features such as area, number of bedrooms, bathrooms, floors, location, condition, garage availability, and year built.

The project demonstrates the full Machine Learning workflow including:

- Data Collection & Loading
- Exploratory Data Analysis (EDA)
- Data Visualization
- Data Preprocessing
- Feature Engineering
- Model Training
- Cross Validation
- Hyperparameter Tuning
- Model Evaluation
- House Price Prediction System

---

## 🚀 Project Overview

This project uses a House Price Prediction dataset containing 2,000 housing records and multiple property features.

The objective is to build and optimize machine learning models capable of estimating house prices accurately based on housing characteristics.

---

## 📂 Dataset Features

| Feature | Description |
|----------|------------|
| Id | House Identifier |
| Area | Area of house (sq.ft.) |
| Bedrooms | Number of bedrooms |
| Bathrooms | Number of bathrooms |
| Floors | Number of floors |
| YearBuilt | Construction year |
| Location | Downtown, Urban, Suburban, Rural |
| Condition | Excellent, Good, Fair, Poor |
| Garage | Yes / No |
| Price | Target Variable |

Dataset Shape:

```text
2000 Rows × 10 Columns
```

---

## 📊 Exploratory Data Analysis (EDA)

The project includes:

- Dataset overview
- Missing value analysis
- Duplicate detection
- Statistical summaries
- Feature distribution analysis
- Correlation analysis
- Outlier detection

### Visualizations

- Count Plots
- Histograms
- KDE Plots
- Box Plots
- Correlation Heatmap
- Residual Analysis

---

## ⚙️ Data Preprocessing

### Numerical Features

- Median Imputation
- Standard Scaling

### Categorical Features

- Most Frequent Imputation
- One-Hot Encoding

### Pipeline Architecture

```text
Input Data
    │
    ├── Numerical Features
    │       ├── Imputer
    │       └── StandardScaler
    │
    └── Categorical Features
            ├── Imputer
            └── OneHotEncoder
                    │
            ColumnTransformer
                    │
               ML Model
```

---

## 🤖 Machine Learning Models Used

The following models were evaluated using 5-Fold Cross Validation:

### Regression Models

- Linear Regression
- Ridge Regression
- Lasso Regression
- Random Forest Regressor
- HistGradientBoosting Regressor

---

## 📈 Model Selection

Evaluation Metrics:

- RMSE (Root Mean Squared Error)
- MAE (Mean Absolute Error)
- R² Score

Cross-validation was performed using:

```python
KFold(
    n_splits=5,
    shuffle=True,
    random_state=42
)
```

---

## 🔧 Hyperparameter Tuning

The best-performing model was optimized using GridSearchCV.

### Tuned Parameters

- learning_rate
- max_depth
- max_leaf_nodes
- min_samples_leaf
- l2_regularization

### Optimization Method

```python
GridSearchCV
```

Total Configurations Tested:

```text
243 Parameter Combinations
1215 Model Fits
```

---

## 🏆 Final Model

### HistGradientBoostingRegressor

Best Parameters:

```python
{
    'learning_rate': 0.03,
    'max_depth': 3,
    'max_leaf_nodes': 15,
    'min_samples_leaf': 100,
    'l2_regularization': 1.0
}
```

---

## 📊 Final Performance

### Training Performance

| Metric | Value |
|----------|----------|
| RMSE | 110,586 |
| MAE | 90,594 |
| R² | 0.839 |

### Test Performance

| Metric | Value |
|----------|----------|
| RMSE | 308,911 |
| MAE | 259,971 |
| R² | -0.227 |

---

## 🔮 House Price Prediction System

The project includes a reusable prediction function:

```python
predict_house_price()
```

### Example

```python
predict_house_price(
    model=hgb_best,
    house_id=2001,
    area=2500,
    bedrooms=3,
    bathrooms=2,
    floors=2,
    year_built=2015,
    location="Downtown",
    condition="Excellent",
    garage="Yes"
)
```

### Output

```text
Predicted House Price: ₹492,558.03
```

---

## 🛠️ Technologies Used

### Language

- Python 3.x

### Libraries

- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-Learn

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/nigamkumar3435-spec/ML_Learning.git
cd ML_Learning
```

Install dependencies:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

---

## ▶️ Run Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

or

```bash
jupyter lab
```

Open the notebook and execute all cells sequentially.

---

## 🎯 Learning Outcomes

Through this project, you will learn:

- Data preprocessing techniques
- Feature engineering
- Machine learning pipelines
- Cross-validation
- Hyperparameter tuning
- Model evaluation
- Building real-world predictive systems

---

## 🔮 Future Improvements

- Feature Selection
- XGBoost Implementation
- LightGBM Implementation
- CatBoost Implementation
- Streamlit Web Application
- Model Deployment on Cloud
- Advanced Feature Engineering

---

## 👨‍💻 Author

**Nigam Kumar**

🎓 B.Tech CSE  
🏫 Indore Institute of Science and Technology, Indore  
💻 Machine Learning & Full Stack Development Enthusiast

GitHub: https://github.com/nigamkumar3435-spec

---

## ⭐ Support

If you found this project useful, please give it a ⭐ on GitHub.

**Happy Coding & Keep Learning Machine Learning! 🚀**
