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
<img width="1232" height="719" alt="imagem" src="https://github.com/user-attachments/assets/2cde0293-0d3b-44a3-844c-ebc088568735" />
- Logistic Regression
<img width="1411" height="399" alt="imagem" src="https://github.com/user-attachments/assets/3e86d7d2-6dbe-4dcb-8be1-497195b1f36c" />
- Decision Trees
<img width="1415" height="429" alt="imagem" src="https://github.com/user-attachments/assets/0981090a-e121-4209-bb3a-b85610d5d875" />
- Random Forest + Email notification automation
<img width="1438" height="644" alt="imagem" src="https://github.com/user-attachments/assets/30ded3a6-41ca-43e0-9c1c-617e318e6059" />
- Autoencoders (Neural Networks)
<img width="1464" height="534" alt="imagem" src="https://github.com/user-attachments/assets/557b9c51-78f8-4719-a7d7-63960fc90b43" />

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
