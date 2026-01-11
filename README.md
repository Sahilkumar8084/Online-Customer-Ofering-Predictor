
# 🛒 Customer Purchase Prediction Web App

<p align="center">
  <img src="https://img.shields.io/badge/Python-blue?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?logo=streamlit&logoColor=white" />
  <img src="https://img.shields.io/badge/Machine%20Learning-Classification-success" />
  <img src="https://img.shields.io/badge/Model-Decision%20Tree-orange" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/status-active-success" />
  <img src="https://img.shields.io/badge/deployment-ready-brightgreen" />
  <img src="https://img.shields.io/badge/license-educational-lightgrey" />
</p>

---

## 🧠 Introduction

The **Customer Purchase Prediction Web App** is a **machine learning–powered Streamlit application** that predicts whether a customer is more likely to purchase a **Product** or a **Service** based on demographic, behavioral, and engagement data.

This project demonstrates a **complete end-to-end ML workflow**, from preprocessing and feature engineering to model inference and web deployment.

---

## 📌 Project Overview

Understanding customer purchasing behavior helps businesses:

* 🎯 Improve marketing strategies
* 🧩 Personalize offerings
* 📈 Increase conversion rates

This application allows users to input customer attributes and instantly receive a prediction using a trained **Decision Tree Classifier**.

---

## 🎯 Objective

To build a **user-friendly ML web application** that:

* Collects customer data through an interactive UI
* Applies the **same preprocessing used during model training**
* Predicts purchase type accurately
* Displays results in a clean, professional interface

---

## 🧠 Machine Learning Approach

### 🔹 Problem Type

* **Binary Classification**

  * `0` → Product
  * `1` → Service

### 🔹 Model Used

* 🌳 **Decision Tree Classifier**

  * Interpretable and intuitive
  * Handles mixed feature types well
  * Ideal for beginner–intermediate ML projects

---

## 📊 Features Used

| Feature Name       | Description                     |
| ------------------ | ------------------------------- |
| Age                | Customer age                    |
| Gender             | Male / Female                   |
| Annual_Income      | Yearly income                   |
| Previous_Purchases | Number of past purchases        |
| Spending_Score     | Spending behavior score (0–100) |
| Engagement_Level   | Low / Medium / High             |
| Visit_Frequency    | Low / Medium / High             |
| Discount_Used      | Yes / No                        |
| Promo_Used         | Yes / No                        |
| Offering_Category  | Type of product/service offered |

---

## 🔄 Data Preprocessing

To maintain **training–inference consistency**, the following steps are applied:

### 1️⃣ Binary Encoding

```text
Gender → Male = 1, Female = 0
Offering_Type → Service = 1, Product = 0
Discount_Used → Yes = 1, No = 0
Promo_Used → Yes = 1, No = 0
```

---

### 2️⃣ Manual One-Hot Encoding (Critical)

The model was trained using:

```python
pd.get_dummies(..., drop_first=True)
```

To prevent feature mismatch in Streamlit, **manual one-hot encoding** is implemented:

```text
Offering_Category_Consulting
Offering_Category_Electronics
Offering_Category_Food
Offering_Category_Streaming
```

⚠️ `Subscription` is excluded because it is the **baseline category** due to `drop_first=True`.

✅ Ensures:

* No missing columns
* No scaler mismatch
* Full compatibility with the trained model

---

### 3️⃣ Ordinal Encoding

```text
Low = 1
Medium = 2
High = 3
```

Applied to:

* Engagement_Level
* Visit_Frequency

---

### 4️⃣ Feature Scaling

* **StandardScaler** is used
* Pre-fitted scaler is loaded using `joblib`
* Prevents data leakage and incorrect predictions

---

## 🖥️ Web Application (Streamlit)

### UI Highlights

* 🎨 Clean and responsive layout
* 📋 Organized input sections
* ▶️ Predict button
* 📊 Highlighted output result
* 🔍 Expandable processed-data view

### Prediction Output

* ✅ **Product Purchase**
* 🔵 **Service Purchase**

---

## 📁 Project Structure

```text
Enginow Internship Project/
│
├── models/
│   ├── scaler.pkl
│   └── decision_tree_model.pkl
│
├── p1.py                  # Streamlit application
├── requirements.txt       # Dependencies
├── README.md              # Documentation
└── venv/                  # Virtual environment
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone <repository-url>
cd Enginow-Internship-Project
```

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
```

### 3️⃣ Activate Environment

**Windows**

```bash
venv\Scripts\activate
```

**Linux / macOS**

```bash
source venv/bin/activate
```

### 4️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the Application

```bash
streamlit run p1.py
```

The app will open at:

```
http://localhost:8501
```

---

## 📦 Requirements

Main libraries used:

* `streamlit`
* `pandas`
* `scikit-learn`
* `joblib`

---

## 🧪 Model Inference Flow

```text
User Input
   ↓
Encoding (Binary / One-Hot / Ordinal)
   ↓
Feature Scaling (StandardScaler)
   ↓
Decision Tree Model
   ↓
Prediction (Product / Service)
```

---

## 🚀 Future Improvements

* Add prediction **probability scores**
* Use **Random Forest / XGBoost**
* Implement **Sklearn Pipelines**
* Deploy on **Streamlit Cloud**
* Add **database integration**
* User authentication system

---

## 🏆 Learning Outcomes

This project helped me gain hands-on experience in:

* End-to-end ML pipeline design
* Correct categorical encoding strategies
* Preventing feature mismatch errors
* Deploying ML models using Streamlit
* Writing production-quality ML applications

---

## 👨‍💻 Author

**Sahil Kumar**
Machine Learning Intern
India 🇮🇳

---

## 📜 License

This project is intended for **educational and internship purposes**.
You are free to modify and extend it.

---

⭐ **If you found this project useful, consider giving it a star!**


