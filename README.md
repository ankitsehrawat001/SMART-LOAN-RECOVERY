# Smart Loan Recovery

A single-page Streamlit risk-prediction interface built around the trained
Random Forest model. The app opens directly to the borrower form and includes
an interactive model-importance chart, risk gauge, and 3D profile view after
prediction.

## Run locally

```powershell
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m streamlit run app.py
```

Keep `loan_rf_model.joblib` and `loan_scaler.joblib` beside `app.py`. The form
uses the model's ten expected inputs: age, monthly income, loan amount, loan
tenure, interest rate, collateral value, outstanding loan amount, monthly EMI,
missed payments, and days past due.

Suggested recovery actions follow the model score: above 75% prioritises direct
review and recovery outreach; from 50% through 75% suggests settlement and
repayment-plan review; below 50% suggests routine reminders and monitoring.
Predictions are decision-support guidance and require human review.
