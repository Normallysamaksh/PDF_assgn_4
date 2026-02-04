# 📊 Probability Density Function Estimation using Maximum Likelihood Estimation (MLE)

This project demonstrates how a probability density function (PDF) can be learned directly from real-world data using **data cleaning, statistical estimation, and Maximum Likelihood Estimation (MLE)**.

The goal is to estimate the parameters of a Gaussian distribution that best fits the observed data.

---

## 🔗 Dataset
- **File Used:** `data.csv`
- **Data Type:** Real-valued numerical measurements  
- **Source:** Provided dataset for the assignment  
- **Usage:** The first column of the CSV is used for PDF estimation  

---

## 🧠 Objective
The objective of this assignment is to:
- Load and clean real-world numerical data  
- Handle encoding and non-numeric values robustly  
- Estimate the mean and standard deviation of the underlying distribution  
- Construct the probability density function using MLE  
- Visualize and analyze the learned PDF  

---

## ⚙️ Workflow Overview

1. Load CSV data using safe encoding  
2. Convert values to numeric form  
3. Remove invalid and missing entries  
4. Estimate distribution parameters  
5. Plot histogram and fitted PDF  
6. Evaluate log-likelihood  

---

## 🪜 Methodology

### 1️⃣ Data Loading & Cleaning
The dataset is loaded using Latin-1 compatible encoding to avoid Unicode errors.  
Non-numeric values are automatically converted to NaN and removed before analysis.

This ensures only valid numerical observations are used for modeling.

---

### 2️⃣ Exploratory Data Analysis
A histogram is plotted to visualize the empirical distribution of the cleaned data.  
This helps understand the shape, spread, and density of the observations before fitting a model.

---

### 3️⃣ Probability Density Function Model
We assume the data follows a **normal (Gaussian) distribution**, whose PDF is:

\[
p(x) = \frac{1}{\sigma \sqrt{2\pi}} \; e^{-\frac{(x-\mu)^2}{2\sigma^2}}
\]

where:
- \( \mu \) is the mean  
- \( \sigma \) is the standard deviation  

---

### 4️⃣ Parameter Estimation using MLE
Using Maximum Likelihood Estimation:

\[
\mu = \frac{1}{n}\sum_{i=1}^{n} x_i
\]

\[
\sigma = \sqrt{\frac{1}{n}\sum_{i=1}^{n}(x_i - \mu)^2}
\]

These values maximize the likelihood of observing the given data under a Gaussian model.

---

## 📈 Results

### 🔢 Estimated Distribution Parameters

| Parameter | Description |
|----------|-------------|
| \( \mu \) | Mean of the observed data |
| \( \sigma \) | Standard deviation of the observed data |

(Exact values are computed dynamically from `data.csv` inside the notebook.)

---

### 📊 Visual Analysis
The notebook generates:
- Histogram of the cleaned dataset  
- Fitted Gaussian PDF overlaid on the histogram  

The close alignment between the histogram and the fitted curve confirms that the estimated PDF models the data effectively.

---

## 🧾 Final Output
The notebook also computes the **log-likelihood**, which quantitatively measures how well the estimated PDF explains the observed data.

---

## 👤 Student Details
**Roll Number:** 102316049  

---
