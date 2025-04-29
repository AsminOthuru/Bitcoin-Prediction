# 📈 Bitcoin Price Prediction using Machine Learning

This project demonstrates how machine learning can be applied to predict Bitcoin price trends using historical data. By engineering relevant features and applying logistic regression, the model aims to predict whether the Bitcoin price will go up or down the next day.

---

## 🔍 Problem Statement

Cryptocurrency markets are highly volatile. Predicting price direction can help reduce risks and enhance trading decisions. This project uses historical Bitcoin data and builds a classification model to predict the **next-day price movement** (Up/Down).

---

## 📁 Dataset

The dataset (`bitcoin_data.csv`) contains the following columns:
- `Date`
- `Price`
- `Open`
- `High`
- `Low`
- `Vol.`
- `Change %`

The dataset includes 1500+ entries of daily Bitcoin trading data.

---

## 🧼 Data Preprocessing

- Handled missing values
- Converted strings with symbols (like `%`, `K`, `M`) to numeric
- Converted `Date` to datetime format
- Capped outliers using the IQR method

---

## 🛠️ Feature Engineering

Created new features such as:
- Day, Month, Year, DayOfWeek
- Price & Volume change percent
- Short-Term and Long-Term EMAs
- Binary target variable `Price_Up` (1 if price goes up next day, else 0)

---

## 📊 Data Visualization

- 📅 Bitcoin price over time
- 📈 Volume vs Price scatter plot
- 🔄 Price Change % distribution
- 🧊 Correlation heatmap with `Price_Up`
- 📉 Price vs EMAs (7-day and 21-day)

---

## 🤖 Model Building

Used **Logistic Regression** to classify price movement:

- Train-test split: 80% / 20%
- Achieved **accuracy of ~98.6%**
- Evaluation: Confusion Matrix & Classification Report

---

## 🔮 User Prediction Tool

After training, the model accepts user input to predict price movement:

```plaintext
Required Inputs:
- Open
- High
- Low
- Volume
- Change %
- Price_Change_Percent
- Short_Term_EMA
- Long_Term_EMA
- DayOfWeek
- Month
