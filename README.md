# IPL Score Prediction using Deep Learning 🏏📊

This project implements a **Deep Learning–based regression model** to predict the **final score of an IPL (Indian Premier League) match** using real-time match features such as runs, wickets, overs, and recent performance metrics.

The model is trained on **ball-by-ball IPL data** and is capable of making accurate score predictions during an ongoing match.

---

## 🔍 Problem Statement

In T20 cricket, predicting the final score during an ongoing innings is crucial for:
- Match strategy and decision-making
- Live analytics platforms
- Fan engagement and sports analytics applications

Traditional statistical methods struggle with non-linear patterns in match dynamics. This project addresses that challenge using **Deep Neural Networks**.

---

## 📂 Dataset Description

The dataset (`ipl_data.csv`) consists of **ball-by-ball match data** from IPL matches.

### 📊 Dataset Shape
- **Rows:** 76,014
- **Columns:** 15

### 🧾 Key Features Used

| Feature | Description |
|------|-----------|
| `runs` | Total runs scored till the current ball |
| `wickets` | Total wickets fallen |
| `overs` | Current over in the innings |
| `runs_last_5` | Runs scored in the last 5 overs |
| `wickets_last_5` | Wickets lost in the last 5 overs |
| `bat_team` | Batting team |
| `bowl_team` | Bowling team |
| `venue` | Match venue |
| `total` | Final innings score (Target Variable) |

---

## 🛠️ Data Preprocessing & Feature Engineering

The following steps were performed:

- Removal of irrelevant teams and outdated seasons
- One-hot encoding of categorical features (teams & venues)
- Feature selection focusing on real-time match parameters
- Train-test split for model evaluation
- **StandardScaler** used to normalize numerical features

---

## 🧠 Deep Learning Model Architecture

The score prediction model is built using **TensorFlow & Keras**.

### 🧠 Deep Learning Model Architecture

| Layer Type | Details |
|----------|---------|
| Input Layer | Match features |
| Dense Layer | 512 neurons, ReLU |
| Dense Layer | 216 neurons, ReLU |
| Output Layer | 1 neuron, Linear |

### ⚙️ Training Configuration

- **Loss Function:** Huber Loss (robust to outliers)
- **Optimizer:** Adam
- **Callbacks:** Early Stopping (to prevent overfitting)
- **Evaluation Metric:** Mean Absolute Error (MAE)

---

## 📈 Model Performance

- The model shows **strong generalization** on unseen match data
- Early stopping ensures optimal weights are retained
- Handles non-linear relationships between match variables effectively

---
