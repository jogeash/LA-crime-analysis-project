# 📊 Los Angeles Crime Analysis & Forecasting

## 📆 Project Details
📅 **Date:** September 2025  
👩‍💻 **Authors:** Jogeashwini Srinivasan Ramesh, Anika Mamidwar, Sanya Kaluarachchi 
🏛️ **Institution:** Northeastern University  


## 🖥️ Tech Stack
* **Programming Language:** Python 🐍
* **Libraries:** Pandas, Matplotlib, Seaborn, NumPy
* **Machine Learning:** Facebook Prophet (Time-Series Forecasting)
* **Data Source:** [LA Crime Dataset via Data.gov](https://data.gov) (2020–2024, 900K+ records)

## 📌 Project Overview
This project explores crime trends in Los Angeles from 2020 to 2024 using data analytics, visualization, and predictive modeling. We analyze crime patterns across time, locations, and demographics — examining the impact of COVID-19, socioeconomic factors, and LAPD's reporting system changes on crime rates, and using Prophet for forecasting future trends.

### 🔍 Key Insights:
* Crime steadily increased post-2020, **peaking in 2022**, coinciding with the lifting of pandemic restrictions and broader socioeconomic turmoil.
* **Burglary/Theft From Vehicle (BTFV)** is the most prevalent crime category.
* **77th Street and Central** divisions consistently report the highest crime counts.
* A sharp drop in 2024 data is largely attributed to **LAPD's migration to a new FBI-compliant record management system**.
* Property crimes peak on **Fridays**, violent crimes peak on **Sundays**.
* Prophet forecasting predicts a **continued downward trend** into 2024–2025.

## 📂 Project Structure

```
📁 LA_Crime_Analysis
 ├── 📊 data/                # Raw and cleaned datasets
 ├── 📈 notebooks/           # Jupyter notebooks with analysis
 ├── 🔍 figures/             # Saved visualizations
 ├── 📄 report/              # Final project report (PDF)
 └── 📜 README.md
```

## 📊 Data Processing & Methodology

### 📥 1. Data Acquisition
* Dataset obtained from Los Angeles crime reports (2020–2024) via [Data.gov](https://data.gov).
* ~900,000+ records loaded using `pandas` into a structured DataFrame.

### 🔍 2. Data Inspection
* Reviewed 28 variables maintained by the LAPD including crime codes, victim demographics, geographic areas, timestamps, and location coordinates.
* Checked data types, missing values, and inconsistencies.

### 🧹 3. Data Cleaning
* **Gender standardization:** M/F entries kept as-is; all other entries (X, `-`, H) standardized to X.
* **Date conversion:** Converted "Date Reported" and "Date Occurred" columns to datetime format for temporal extraction (day, month, year).
* **Column removal:** Dropped Weapon Description, Weapon Used Code, Mocodes, and Cross Street.
* **Filtered partial data:** Removed 2025 entries (only recorded through March) to avoid skewing yearly comparisons.

## 📈 Exploratory Data Analysis (EDA)

### 📊 Overall Crime Trends
* Crime peaked in **2022** before declining in 2023 & 2024.
* The 2024 drop is largely a reporting artifact due to LAPD's new record management system adopted in March 2024.

### 📅 Seasonal & Temporal Patterns
* Crime is highest during **summer months (June–August)** and lowest in **February**.
* Most crimes occur during **afternoon and evening hours** (12 PM–11 PM).
* A clear weekly cycle: higher crime on weekends, building through the weekdays.

### 🔎 Crime Type Analysis
* **Top categories:**
   1. Burglary/Theft From Vehicle (BTFV)
   2. Other Theft (shoplifting, monetary theft)
   3. Motor Vehicle Theft
   4. Domestic Violence
   5. Simple Assault
* Homicides represent a very small fraction of total incidents.

### 📍 Regional Crime Analysis
* **Highest crime areas:** 77th Street, Central
* Crime stays fairly consistent across most of LA County's 21 LAPD geographic divisions, with those two as notable exceptions.

### 📊 Violent vs. Property Crime Patterns
* Violent crimes (homicide, rape, robbery, aggravated assault, domestic violence, simple assault) **peak on Sundays**.
* Property crimes (burglary, motor vehicle theft, BTFV, personal theft, other theft) **peak on Fridays**.

### 👤 Victim Demographics
* Males represent the largest proportion of crime victims across all years.
* In 2024, the proportion of "Unknown" sex victims increased significantly — likely tied to the reporting system migration.

## 🤖 Predictive Modeling (Prophet Forecasting)
* Trained on **monthly crime data from 2020–2023** using Facebook Prophet.
* Forecasted 2024–2025 crime trends show a **continued downward trajectory**.
* The model captures seasonality but does **not account for political, legal, or socioeconomic reforms**.
* Confidence intervals widen over time, reflecting increasing uncertainty.

## 🚀 Future Improvements
* Incorporate **socioeconomic and environmental factors** into forecasting models.
* Cross-reference with other public records to address **underreporting** (especially domestic violence and sexual assault).
* Account for LAPD's **reporting system migration** when analyzing 2024+ data.
* Integrate legal and political reform variables for more robust predictions.

## ⚠️ Limitations
* Underreporting bias, particularly for domestic violence and sexual assault.
* 2024 data is incomplete due to the LAPD system transition mid-year.
* Prophet model relies solely on historical trends without external regressors.

## 📜 Full Report
📄 Read the full Los Angeles Crime Analysis Report [here](report/).

## ⭐ Contribute & Connect
💡 If you find this useful, star ⭐ this repo!

📩 For questions, feel free to reach out! 🚀

