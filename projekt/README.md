# 📊 Exam Score Prediction:  A Machine Learning Adventure

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0+-orange.svg)
![Status](https://img.shields.io/badge/Status-Complete-success.svg)
![Fun](https://img.shields.io/badge/Fun-100%25-ff69b4.svg)

*Predicting student exam scores using the power of data science and machine learning! * 🚀

</div>

---

## 🎯 What's This All About?

Ever wondered what really makes students ace their exams? Is it the hours spent studying?  The quality of sleep? Or maybe it's the power of good Wi-Fi? 🤔

This project dives deep into **20,000+ student records** to uncover the secrets of academic success using **7 different machine learning models**.  Spoiler alert: the answers might surprise you!

---

## 🌟 Features

- 📈 **Comprehensive EDA**:  Beautiful visualizations that tell the story of student performance
- 🤖 **7 ML Models**: From simple linear regression to powerful random forests
- 🎨 **Stunning Visualizations**: Because data should look as good as it performs
- 📊 **Feature Engineering**: Creating "study effectiveness" - because studying hard AND attending class = 💯
- 🏆 **Model Showdown**: Watch algorithms compete for the best predictions! 
- 🔍 **Interpretable Results**: Not just predictions - understand WHY they work

---

## 🎮 Quick Start

### Prerequisites

```bash
# You'll need these awesome tools: 
pip install pandas numpy matplotlib seaborn scikit-learn scipy jupyterlab
```

### Running the Analysis

```bash
# Clone this repo
git clone https://github.com/MilanKalajdzic/Machine-learning-I-project.git
cd exam-score-prediction

# Launch Jupyter
jupyter lab exam_score_prediction_improved.ipynb

# Or if you're using the . py file in VS Code, just open and run!  🚀
```

## 🎨 The Dataset

Our data includes **20,000 students** with features like: 

### 📚 Study Habits
- ⏰ **Study Hours**: Time spent hitting the books
- 📖 **Study Method**: Online, offline, or group study
- 🎯 **Class Attendance**: Because showing up matters!

### 😴 Lifestyle Factors
- 🛌 **Sleep Hours**: Beauty sleep = better grades? 
- 💤 **Sleep Quality**: Poor, average, or good
- 🌐 **Internet Access**: The digital divide

### 📝 Demographics & Context
- 👤 **Age & Gender**: Student characteristics
- 📚 **Course**: Different subjects, different challenges
- 🏫 **Facility Rating**: School infrastructure quality
- 📊 **Exam Difficulty**: Easy, moderate, or hard

### 🎯 Target Variable
- 🏆 **Exam Score**: The ultimate metric (0-100)

---

## 🤖 The Model Arena

We trained **7 different models** to see which one reigns supreme:

### 🔵 Team Linear (The Interpreters)

| Model | Special Power | Best For |
|-------|--------------|----------|
| 🟢 **OLS** | Simple & Fast | Understanding relationships |
| 🔵 **Ridge** | L2 Regularization | Handling multicollinearity |
| 🟣 **Lasso** | Feature Selection | Sparse models |
| 🟠 **ElasticNet** | Best of Both Worlds | Balanced approach |

###🔴 Team Non-Linear (The Heavy Hitters)

| Model | Special Power | Best For |
|-------|--------------|----------|
| 🌳 Decision Tree | Rule-Based Splits | Interpretable non-linearity |
| 🌲 Random Forest | Ensemble Power | Robust predictions |
| ⚡ SVR | Kernel Magic | Complex patterns |

---

📊 Key Findings
🏆 The Winner Is...
🎉 [Check the notebook to find out!] 🎉

The best model achieves: 
✅ R² Score: ~0.XX (explains XX% of variance)
✅ RMSE: ~X.XX points
✅ MAE: ~X.XX points

💡 Top Insights
📚 Study Effectiveness = Study Hours × Attendance
The secret sauce:  studying hard + showing up!

😴 Sleep Quality Matters
Well-rested students perform better (shocker!)

📊 Exam Difficulty Has Impact
But good students shine regardless!

🎯 The Best Features
Check the feature importance plots in the notebook!

---
🛠️ Technical Stack
| Category | Tools |
|----------|-------|
| Language | Python 3.8+ 🐍 |
| Data Wrangling | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn |
| Statistics | SciPy |
| Environment | Jupyter Lab / VS Code |

---

📚 Project Workflow
graph LR
    A[📥 Load Data] --> B[🔍 EDA]
    B --> C[🧹 Preprocessing]
    C --> D[✂️ Train/Val/Test Split]
    D --> E[🤖 Train Models]
    E --> F[📊 Evaluate]
    F --> G[🏆 Select Best]
    G --> H[📝 Conclusions]


📥 Data Loading:  Import the student dataset
🔍 Exploratory Data Analysis:  Understand patterns and distributions
🧹 Data Preprocessing: Feature engineering + scaling
✂️ Data Splitting: 70% train / 15% validation / 15% test
🤖 Model Training: Train all 7 models
📊 Evaluation: Compare performance metrics
🏆 Winner Selection: Choose the best model
📝 Insights: Extract actionable conclusions

---

📈 Results Interpretation Guide
🎯 Understanding the Metrics
R² Score: % of variance explained (higher = better)
0.9+ = Excellent 🌟
0.8-0.9 = Very Good ✅
0.7-0.8 = Good 👍
<0.7 = Needs Work 🔧

RMSE: Average prediction error in points
Lower is better!
Compare to exam score standard deviation

MAE: Average absolute error
More interpretable than RMSE
"On average, we're off by X points"

🔍 Overfitting Check
Train R² - Test R² < 0.05  →  ✅ Excellent generalization
Train R² - Test R² < 0.10  →  ⚠️  Moderate overfitting
Train R² - Test R² > 0.10  →  ❌ Significant overfitting


---
