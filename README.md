# Fraud-Analytics-with-KNIME

🎉 **1st Place – Identifying Fraud Challenge (Spring 2025)** 🎉  

This project was developed as part of the *Big Data Analytical Methods* course at ISCTE Business School, in collaboration with KNIME.  
It focuses on detecting fraudulent transactions using a combination of statistical techniques, machine learning models, and deployment workflows.

<a href="https://www.credly.com/badges/634b8637-bd87-459b-b8d0-e6694d357735/linked_in_profile">
  <img src="https://github.com/user-attachments/assets/60c4878a-c4ce-4e80-b2b2-686e28c458fe" alt="Credly Badge" width="140"/>
</a>

## Project Overview

With the rapid growth of e-commerce, fraud detection has become a critical challenge for organizations.  
This project aims to identify suspicious transactions by combining multiple analytical approaches into a robust and scalable solution.

The solution was built using **KNIME Analytics Platform**, leveraging its low-code capabilities to design, train, and deploy fraud detection models.

## Dataset

- ~1.47 million transactions (2024)
- 16 variables describing transaction behavior  
- Target variable: `Is Fraudulent`  

Key features include:
- Transaction Amount  
- Customer Information (Age, Location)  
- Device and IP data  
- Payment Method  
- Transaction Time  

The dataset is **highly imbalanced**, with only ~5.28% fraudulent transactions. This is a common characteristic in fraud detection problems, where the objective is to identify rare events. As a result, this imbalance requires specific decisions during both model training and evaluation, with a stronger focus on correctly detecting fraudulent transactions (minority class) rather than overall accuracy.

## ⚙️ Methodology

The project follows the **CRISP-DM framework**, ensuring a structured analytical approach.

### Techniques Applied

- Outlier Detection (IQR / Quartiles)
- Logistic Regression
- Decision Trees
- Random Forest + Email notification automation
- Autoencoders (Neural Networks)

Each model was implemented with a tailored preprocessing pipeline to ensure fair evaluation.

## 🧹 Data Preparation

- No missing values detected  
- Outliers were **intentionally preserved** (potential fraud indicators)  
- Negative values (e.g., age) kept as anomaly signals  
- Z-score normalization applied where needed  
- Removal of non-informative variables (IDs)  

### Feature Engineering

- `day_period` → time of day category  
- `amount_per_hour` → captures unusual transaction patterns  
- `device_location_match` → detects location inconsistencies  

These features helped improve anomaly detection performance. 

## Model Performance & Insights

Key findings:

- **Decision Trees** and **Autoencoder + PCA**
  - High recall → effective for early fraud detection  

- **Quartile-based model**
  - Best overall balance  
  - Highest accuracy (~93.63%)  
  - Strong interpretability  

- **Random Forest & Logistic Regression**
  - Lower performance due to poor precision
  
## Final Architecture

A **3-layer hybrid fraud detection system** was proposed:

1. **Autoencoder (+ PCA)** → Early anomaly detection  
2. **Decision Tree** → Main classification layer  
3. **Quartile Model** → Simple validation layer

Benefits:
- High coverage of fraud cases  
- Real-time applicability  
- Strong interpretability  
- Scalable for e-commerce environments

## Deployment

A real-world simulation was implemented:

- Random Forest model deployed for live scoring  
- Suspicious transactions filtered automatically  
- Email alerts triggered for fraud cases  
- Near real-time monitoring achieved using KNIME workflows  

This demonstrates practical applicability in **high-volume environments (e-commerce / fintech)**
<img width="1435" height="640" alt="imagem" src="https://github.com/user-attachments/assets/a188d2b7-a8bb-4492-9a3f-24bd0fdec5c4" />

## 🔗 Portfolio

Check more projects here:  
https://github.com/JoaoSaraiva99

## 📎 Project Presentation

Full project presentation available [here](https://github.com/JoaoSaraiva99/Fraud-Analytics-with-KNIME/blob/main/Fraud%20Analytics%20Project.pdf).

