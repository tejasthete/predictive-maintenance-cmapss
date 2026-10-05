# Predictive Maintenance using NASA C-MAPSS

A machine learning project for **predictive maintenance of turbofan engines** using the NASA C-MAPSS (Commercial Modular Aero-Propulsion System Simulation) dataset.

The goal of this project is to analyze engine sensor data, estimate **Remaining Useful Life (RUL)**, and eventually build a machine learning model that can predict when an engine is approaching failure.

---

## 📌 Project Overview

Predictive maintenance uses historical sensor data to identify signs of equipment degradation and predict potential failures before they occur.

In this project, the **NASA C-MAPSS FD001 turbofan dataset** is used to study the degradation of simulated aircraft engines.

The project will follow a complete machine learning workflow:

```text
Raw C-MAPSS Dataset
        ↓
Data Understanding
        ↓
Exploratory Data Analysis
        ↓
Feature Engineering
        ↓
Model Development
        ↓
Model Evaluation
        ↓
RUL Prediction
```

---

## 🎯 Objectives

* Understand the NASA C-MAPSS turbofan dataset.
* Analyze engine operating cycles and sensor measurements.
* Calculate Remaining Useful Life (RUL) for training data.
* Identify useful sensor measurements and degradation patterns.
* Perform feature engineering on time-series sensor data.
* Train machine learning models for RUL prediction.
* Evaluate model performance.
* Develop a predictive maintenance pipeline.

---

## 📂 Project Structure

```text
predictive-maintenance-cmapss/
│
├── data/
│   ├── train_FD001.txt
│   ├── test_FD001.txt
│   └── RUL_FD001.txt
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_feature_engineering.ipynb
│   └── 04_modeling.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── feature_engineering.py
│   └── prediction.py
│
├── models/
│
├── reports/
│
├── requirements.txt
│
└── README.md
```

---

## 📊 Dataset

This project uses the **NASA C-MAPSS FD001 turbofan engine dataset**.

The dataset contains simulated run-to-failure data from multiple turbofan engines.

Each observation contains:

* Engine ID
* Operating cycle
* 3 operating settings
* 21 sensor measurements

### Dataset Files

| File              | Description                                           |
| ----------------- | ----------------------------------------------------- |
| `train_FD001.txt` | Training data containing engine degradation histories |
| `test_FD001.txt`  | Test data containing partial engine histories         |
| `RUL_FD001.txt`   | True RUL values for the test engines                  |

For the FD001 dataset, there are **100 engines** in the training set and **100 engines** in the test set.

---

## 🔍 Current Progress

### Phase 1 — Data Understanding

**Completed**

The first notebook:

```text
notebooks/01_data_understanding.ipynb
```

covers:

* Loading the C-MAPSS dataset
* Adding column names
* Understanding dataset dimensions
* Inspecting training and test data
* Checking engine IDs
* Analyzing engine operating cycles
* Checking missing values
* Checking duplicate records
* Examining sensor statistics
* Examining sensor variability
* Understanding sensor correlations
* Visualizing engine lifetime

### Phase 2 — Exploratory Data Analysis

**In Progress**

```text
notebooks/02_eda.ipynb
```

Planned analysis includes:

* RUL distribution
* RUL vs operating cycle
* Engine degradation patterns
* Sensor behavior over time
* Sensor-to-RUL correlation
* Sensor correlation analysis
* Early-life vs late-life behavior

### Phase 3 — Feature Engineering

**Planned**

```text
notebooks/03_feature_engineering.ipynb
```

This phase will prepare the time-series data for machine learning.

### Phase 4 — Modeling

**Planned**

```text
notebooks/04_modeling.ipynb
```

Machine learning models will be trained and evaluated for RUL prediction.

---

## 🧠 Remaining Useful Life (RUL)

Remaining Useful Life represents the estimated number of operating cycles an engine has before failure.

For the training data, RUL is calculated using:

```text
RUL = Maximum cycle of the engine - Current cycle
```

For example, if an engine fails at cycle 200:

```text
Cycle 1   → RUL = 199
Cycle 2   → RUL = 198
...
Cycle 199 → RUL = 1
Cycle 200 → RUL = 0
```

This creates the target variable that will later be used for machine learning.

---

## 🛠️ Technologies Used

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

Additional machine learning libraries may be added during the modeling stage.

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/predictive-maintenance-cmapss.git
```

### 2. Navigate to the project

```bash
cd predictive-maintenance-cmapss
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Open Jupyter Notebook

```bash
jupyter notebook
```

Then open:

```text
notebooks/01_data_understanding.ipynb
```

---

## 📈 Project Goal

The final objective is to build a machine learning system capable of estimating the **Remaining Useful Life of turbofan engines** from historical sensor data.

The completed project will demonstrate a complete predictive-maintenance workflow from raw data analysis to machine learning-based RUL prediction.

---

## 📚 Dataset Reference

NASA C-MAPSS (Commercial Modular Aero-Propulsion System Simulation) turbofan engine degradation dataset.

---

## 👨‍💻 Author

**Prajwal Thete**

B.Tech — Artificial Intelligence & Data Science

---

## ⭐ Project Status

🚧 **Currently under development**

The project is being developed step-by-step, starting with data understanding and exploratory data analysis.
