# Marketing Mix Modeling (MMM) – Revenue Prediction

This project implements a **Marketing Mix Modeling (MMM)** pipeline to analyze and predict weekly revenue based on marketing spends, promotions, and other factors. It leverages time-series data, feature engineering, and machine learning models to understand the effectiveness of marketing channels and forecast business performance.

The project is built using Python, scikit-learn, and visualization libraries like Matplotlib and Seaborn, with data preprocessing, cross-validation, and model evaluation incorporated into a structured workflow.

---

## 📂 Dataset

The dataset used is `MMM Weekly.csv`, which contains weekly data about:

- Marketing spends across multiple channels (Facebook, Google, TikTok, Instagram, Snapchat)
- Promotional activities
- Customer engagement metrics (emails sent, social followers, SMS campaigns)
- Target variable: Weekly revenue


## 🔑 Features Engineered

- **Binary flags** for active spend channels (`*_is_active`)
- **Log transformations** (`log1p`) for skewed numerical columns
- **Time-based features** such as `week_of_year`, `month`, `year`, with cyclical encoding (`week_of_year_sin`, `week_of_year_cos`)
- **Mediated features** such as `social_total_spend` and `social_effect`
- **Target transformation** using `log1p` for better scaling and modeling

---

## 📈 Models Compared

The project compares several machine learning models using time-series cross-validation:

✅ Ridge Regression  
✅ Lasso Regression  
✅ Random Forest Regressor  
✅ Gradient Boosting Regressor  

(You can also extend this by adding models like XGBoost and LightGBM.)

---

## 📊 Evaluation Metrics

The models are evaluated on the test set using the following metrics:

- **R² Score** – Explained variance
- **Mean Absolute Error (MAE)** – Average absolute difference
- **Mean Absolute Percentage Error (MAPE)** – Percentage-based error
- **Mean Squared Error (MSE)** – Squared differences

Additionally, residuals are visualized to check prediction accuracy, and feature importances are plotted to interpret model decisions.

---

## 🛠 Tools Used

- Python 3.x
- Pandas, NumPy – Data manipulation
- scikit-learn – Preprocessing, modeling, metrics
- Matplotlib, Seaborn – Visualization
- Google Colab – Execution environment

---


## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/marketing-model.git
cd marketing-model

###2. Install dependencies
We recommend using a virtual environment.
pip install -r requirements.txt

3. Run the notebook
Launch Jupyter and open the notebook:
jupyter notebook marketing.ipynb

4.
