# Assignment 4 – Explainable and Privacy-Aware AI for Cybersecurity

## Overview
This assignment focuses on developing an AI-based login threat detection system using a **Decision Tree Classifier**. The system analyzes login activity, identifies suspicious behavior, explains predictions, protects sensitive information, and generates responsible security alerts.

## Objectives
- Detect suspicious login activities using Machine Learning.
- Generate predictions with confidence scores.
- Identify important features influencing model predictions.
- Perform sensitivity analysis by modifying failed login attempts.
- Protect account IDs and IP addresses using privacy masking.
- Generate security alerts with severity levels and recommended actions.
- Include human review for high-risk activities.

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab / Jupyter Notebook

## Dataset
A sample login activity dataset is created within the notebook.

**Features used:**
- `failed_logins` – Number of failed login attempts.
- `login_hour` – Hour at which the user logged in.
- `new_device` – Indicates whether the login is from a new device.
- `download_mb` – Amount of data downloaded in MB.
- `label` – Login activity category (Normal or Suspicious).

## Machine Learning Algorithm
**Decision Tree Classifier**

The Decision Tree model is trained using login activity features to classify login records as:
- Normal
- Suspicious

The model also generates prediction confidence scores using `predict_proba()`.

## Implementation Steps
1. Import the required Python libraries.
2. Create a sample login activity training dataset.
3. Train a Decision Tree classification model.
4. Generate predictions for five sanitized login records.
5. Calculate prediction confidence scores.
6. Identify the record with the lowest confidence.
7. Calculate and visualize feature importance.
8. Perform a sensitivity test by changing failed login attempts from 2 to 8.
9. Mask account IDs and IP addresses to protect privacy.
10. Generate responsible security alerts.
11. Summarize alerts according to their severity.

## Results

### 1. Login Activity Predictions

The model generated predictions for five sample records:

| Account | Prediction | Confidence |
|---|---|---|
| ACC-1001 | Normal | 1.0 |
| ACC-1002 | Suspicious | 1.0 |
| ACC-1003 | Normal | 1.0 |
| ACC-1004 | Suspicious | 1.0 |
| ACC-1005 | Normal | 1.0 |

### 2. Feature Importance

The feature importance analysis showed:

- Failed Logins: 1.0
- Login Hour: 0.0
- New Device: 0.0
- Download MB: 0.0

In this trained Decision Tree, failed login attempts were the feature used for the model's splits.

### 3. Sensitivity Analysis

The fifth baseline record was tested by changing only its failed login attempts:

- Baseline: 2 failed logins → Normal
- Modified: 8 failed logins → Suspicious

The model's prediction changed after modifying the failed login attempts.

### 4. Privacy Protection

Account IDs and IP addresses were masked before displaying the records.

Example:
- Account ID: `ACC-1001` → `ACC-***01`
- IP Address: `192.168.10.24` → `192.168.xxx.xxx`

### 5. Security Alert Summary

| Alert Category | Total |
|---|---:|
| High Severity | 2 |
| Medium Severity | 0 |
| Low Severity | 3 |
| Human Review Required | 2 |
| Total Records | 5 |

## Privacy and Responsible-Use Rules
- Mask identifiers before displaying or exporting records.
- Use sanitized data in classroom notebooks.
- Restrict access to unmasked records.
- Require human review for high-risk actions.

## Conclusion
In this assignment, we developed an AI-based login threat detection system using a Decision Tree classifier. The system identifies suspicious login activities, generates confidence scores, analyzes feature importance, and performs sensitivity testing.

Privacy masking and responsible security alerts were also implemented to protect sensitive information and support human oversight.

This experiment demonstrates how Explainable and Privacy-Aware AI can improve cybersecurity monitoring while maintaining privacy and responsible decision-making.

## Repository Structure

```text
Assignment-4/
│
├── AI_Cyber_Security_Lab_Assignment_4.ipynb
└── README.md
```
