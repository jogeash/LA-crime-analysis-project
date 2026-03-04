# 📊 Los Angeles Crime Analysis & Forecasting

## 📆 Project Details
📅 **Date:** 2024  
👩‍💻 **Authors:** Anika Mamidwar, Sanya Kaluarachchi, Jogeashwini  
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
 📁 Los_Angeles_Crime_Analysis
 ├── 📊 Data Preprocessing
 ├── 📈 Exploratory Data Analysis (EDA)
 ├── 🔍 Crime Trends & Visualization
 ├── 🤖 Predictive Modeling (Facebook Prophet Forecasting)
 ├── 📄 Report & Findings
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

---

## 📈 Exploratory Data Analysis (EDA)

### 📊 Overall Crime Trends

Crime steadily increased from ~200,000 incidents in 2020 to a peak of ~236,000 in 2022, before declining in 2023. The sharp drop in 2024 is largely a reporting artifact due to LAPD adopting a new FBI-compliant record management system in March 2024.

![Total Number of Crimes per Year](figures/total_crimes_per_year.png)

---

### 📅 Monthly Crime Counts by Year

Breaking down crime counts by month for each year reveals that 2022 and 2023 consistently had the highest monthly counts, while 2024 shows a dramatic decline starting mid-year as the old reporting system was phased out.

![Monthly Crime Counts by Year](figures/monthly_crime_counts_by_year.png)

---

### 🌡️ Seasonal Crime Patterns

Average monthly crime data shows a dip from January through April, followed by a summer surge peaking in June–July. Crime dips again in September before a sharp spike in December.

![Average Monthly Crimes](figures/avg_monthly_crimes.png)

---

### 🕐 Crime Frequency by Day of Week and Hour

The heatmap reveals that crime peaks around **12 PM (noon)** across all days, with the highest concentration on weekdays (Monday–Wednesday). Late-night and early-morning hours consistently show the lowest crime frequency.

![Crime Frequency by Day of Week and Hour](figures/crime_heatmap_day_hour.png)

---

### 📊 Violent vs. Property Crime Patterns

**Violent crimes** (homicide, rape, robbery, aggravated assault, domestic violence, simple assault) trend upward through the week and **peak on Sundays**. In contrast, **property crimes** (burglary, motor vehicle theft, BTFV, personal theft, other theft) build through the weekdays and **peak on Fridays**.

![Violent and Property Crimes by Day of Week](figures/violent_property_crimes_by_day.png)

---

### 📍 Regional Crime Analysis

The heatmap of crime counts by LAPD area and year shows that **77th Street and Central** consistently have the highest crime counts across all years. Most other areas remain relatively consistent, with 2022 being the peak year across nearly all regions.

![Crime Count by Area and Year](figures/crime_count_area_year_heatmap.png)

---

### 👤 Victim Demographics

Males represent the largest proportion of crime victims (~42%), followed by females (~37%), with the remainder classified as unknown (X). This distribution remains fairly consistent across the dataset.

![Proportion of Crimes by Victim Sex](figures/crimes_by_victim_sex.png)

---

## 🤖 Predictive Modeling (Prophet Forecasting)

Using Facebook Prophet trained on **monthly crime data from 2020–2023**, forecasted 2024–2025 crime trends show a continued downward trajectory. The model captures seasonality but does **not account for political, legal, or socioeconomic reforms**. The observed 2024 data (blue) diverges sharply from the forecast (red), largely due to the reporting system change. Confidence intervals widen over time, reflecting increasing uncertainty.

![Prophet Crime Forecast](figures/prophet_forecast.png)

---

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
📄 Read the full Los Angeles Crime Analysis Report [here]([report/](https://github.com/jogeash/LA-crime-analysis-project/blob/main/IE%206400%20Project%201%20Report.pdf)).

## ⭐ Contribute & Connect
💡 If you find this useful, star ⭐ this repo!

📩 For questions, feel free to reach out! 🚀
