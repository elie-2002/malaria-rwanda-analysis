# malaria-rwanda-analysis

*Name:* Nshimyumuremyi Elias  
*Student ID:* 27020 
*Course:* Introduction to Big Data

Analysis of malaria incidence trends in Rwanda using Python and Power BI

---

## 📊 Dataset Information

- **Source**: WHO Global Health Observatory
- **File Name**: `RELAY_WHS.csv`
- **Table Used**: `cleaned_malaria_data (4)`
- **Structure**: Structured CSV with yearly malaria rates
- **Key Column**: `RATE_PER_1000_N` = Estimated malaria cases per 1,000 people at risk

---

## 🔍 Python Analysis

Used **Pandas**, **Matplotlib**, and **ARIMA** to:

- Clean and preprocess data
- Plot incidence trends over time
- Forecast future values using time series modeling
- Detect significant trend changes
- <img width="1359" height="722" alt="fexam1" src="https://github.com/user-attachments/assets/488089cc-e817-4fb7-86e0-afae0d9b966f" />
-<img width="1366" height="761" alt="fexam4" src="https://github.com/user-attachments/assets/b8fade6b-f6af-4157-998b-731e58615639" />
-<img width="1353" height="725" alt="fexam5" src="https://github.com/user-attachments/assets/0de599b5-4dc1-4ee0-8b85-289e72e7beac" />


---

## 📈 Power BI Dashboard

Dashboard Highlights:

- 📅 Time series chart of incidence rates
- 📊 Bar chart of annual changes
- 📌 Key metrics cards (max, min, avg rates)
- 🔁 5-Year Moving Average (DAX measure):
- <img width="1361" height="725" alt="dashboard_screenshot" src="https://github.com/user-attachments/assets/ef6ea4b9-800d-4c44-90ff-9da563e5f3f9" />


```DAX
FiveYearMovingAvg =
AVERAGEX(
    DATESINPERIOD(
        'cleaned_malaria_data (4)'[Year],
        MAX('cleaned_malaria_data (4)'[Year]),
        -5,
        YEAR
    ),
    CALCULATE(MAX('cleaned_malaria_data (4)'[RATE_PER_1000_N]))
)
This project demonstrates the importance of analyzing malaria trends to support Rwanda’s health initiatives. By combining Python and Power BI tools, we gained actionable insights into the historical patterns and future projections of malaria incidence, helping inform strategic planning for disease control and prevention.

