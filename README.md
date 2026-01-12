

# 🛒 Customer Purchase Prediction Web App

<p align="center">
  <img src="https://img.shields.io/badge/Python-blue?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?logo=streamlit&logoColor=white" />
  <img src="https://img.shields.io/badge/Machine%20Learning-Classification-success" />
  <img src="https://img.shields.io/badge/Model-Decision%20Tree-orange" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/status-live-success" />
  <img src="https://img.shields.io/badge/deployed-Streamlit%20Cloud-brightgreen" />
  <img src="https://img.shields.io/badge/license-educational-lightgrey" />
</p>

---

## 🌐 Live Application

🚀 **Deployed App**:
👉 [https://online-customer-ofering-predictor.streamlit.app/](https://online-customer-ofering-predictor.streamlit.app/)

---

## 🧠 Introduction

The **Customer Purchase Prediction Web App** is a **machine learning–powered Streamlit application** that predicts whether a customer is more likely to purchase a **Product** or a **Service** based on demographic, behavioral, and engagement data.

This project showcases a **complete end-to-end ML workflow**, including preprocessing, feature encoding, scaling, model inference, and cloud deployment.

---

## 📌 Project Overview

Businesses use customer behavior analysis to:

* 🎯 Improve marketing strategies
* 🧩 Personalize product offerings
* 📈 Increase conversion rates

This application enables instant predictions using a trained **Decision Tree Classifier**.

---

## 🎯 Objective

To build a **user-friendly ML web app** that:

* Collects customer data through an interactive UI
* Applies **training-consistent preprocessing**
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

  * Interpretable and efficient
  * Handles mixed data types
  * Ideal for internship-ready ML projects

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
| Offering_Category  | Type of offering                |

---

## 🔄 Data Preprocessing

### 1️⃣ Binary Encoding

```text
Gender → Male = 1, Female = 0
Offering_Type → Service = 1, Product = 0
Discount_Used → Yes = 1, No = 0
Promo_Used → Yes = 1, No = 0
```

---

### 2️⃣ Manual One-Hot Encoding (Critical)

```text
Offering_Category_Consulting
Offering_Category_Electronics
Offering_Category_Food
Offering_Category_Streaming
```

⚠️ `Subscription` is the baseline category (`drop_first=True`).

---

### 3️⃣ Ordinal Encoding

```text
Low = 1
Medium = 2
High = 3
```

---

### 4️⃣ Feature Scaling

* **StandardScaler**
* Pre-fitted scaler loaded via `joblib`
* Ensures correct inference

---

## 🖥️ Web Application (Streamlit)

### UI Highlights

* Clean, responsive layout
* Organized input fields
* Predict button
* Clear prediction output
* Expandable processed-data section

---

## 📁 Project Structure

```text
Enginow Internship Project/
│
├── models/
│   ├── scaler.pkl
│   └── decision_tree_model.pkl
│
├── p1.py
├── requirements.txt
├── README.md
└── venv/
```

---

## ⚙️ Installation & Setup

```bash
git clone <repository-url>
cd Enginow-Internship-Project
pip install -r requirements.txt
streamlit run p1.py
```

---

## 📦 Requirements

* streamlit
* pandas
* scikit-learn
* joblib

---

## 🧪 Model Inference Flow

```text
User Input
   ↓
Preprocessing
   ↓
Scaling
   ↓
Decision Tree Model
   ↓
Prediction
```

---

## 🚀 Future Improvements

* Prediction probability scores
* Advanced models (Random Forest, XGBoost)
* ML Pipelines
* Database integration
* User authentication

---

## 🏆 Learning Outcomes

* End-to-end ML deployment
* Feature engineering consistency
* Model inference in production
* Streamlit cloud deployment

---

## 👨‍💻 Author

**Sahil Kumar**
Machine Learning Intern
India 🇮🇳

---

## 📜 License

Educational & internship use.

---

⭐ **Live project deployed and production-ready!**

Just say the word 👍
