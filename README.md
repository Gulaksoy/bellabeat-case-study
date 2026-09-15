# Bellabeat Case Study

**Google Data Analytics Professional Certificate — Capstone Project**

This project analyzes smart device usage data to help Bellabeat, a wellness technology company, better understand consumer behavior. The goal is to identify trends in the data and provide actionable, evidence-backed recommendations for Bellabeat's marketing strategy.

## 📊 Data Source

[FitBit Fitness Tracker Data](https://www.kaggle.com/datasets/arashnic/fitbit) (CC0: Public Domain), shared via Mobius on Kaggle — daily activity and sleep data from 30 consenting Fitbit users (2016).

Files used: `dailyActivity_merged.csv`, `sleepDay_merged.csv`.

## 🛠️ Tools

Python (pandas, NumPy) for data cleaning and analysis; matplotlib and seaborn for visualization. Full code is in [`bellabeat_case_study.ipynb`](bellabeat_case_study.ipynb) — every chart and statistic in this README and in the report is generated directly from that notebook, not typed in by hand.

## 📌 Process (Ask → Prepare → Process → Analyze → Share → Act)

- **ASK:** Defined the business task — identify smart device usage trends and translate them into marketing recommendations for one Bellabeat product.
- **PREPARE:** Assessed the dataset using the ROCCC framework (Reliable, Original, Comprehensive, Current, Cited) and documented its limitations (small sample, no demographic data, 2016 data).
- **PROCESS:** Removed duplicates and zero-activity/zero-sleep rows, standardized date formats, merged the two datasets, and engineered new fields (`TotalActiveMinutes`, `SedentaryPercentage`, `SleepEfficiency`, `DayOfWeek`).
- **ANALYZE:** Explored activity intensity, sedentary time, sleep efficiency, weekday/weekend patterns, and built a simple threshold-based user segmentation.
- **SHARE:** Summarized insights with supporting visualizations (below).
- **ACT:** Translated findings into concrete, prioritized marketing recommendations.

## 🎯 Key Insights

- Users are sedentary for roughly **75% of the tracked day** — this is the single largest behavioral pattern in the data.
- Average daily steps (~8,300) fall below the standard 10,000-step benchmark; only about a third of days reach it.
- Sleep efficiency is strong (~92%), but sleep **duration** is inconsistent and is **not** correlated with daytime activity in this dataset (r ≈ ‑0.19) — an early draft of this analysis claimed the opposite, and that claim was corrected after checking the actual numbers.
- There is **no meaningful weekday/weekend difference** in step counts in this sample (~8,330 vs. ~8,300) — again, corrected from an earlier assumption.
- A simple, transparent threshold-based segmentation (Sedentary / Lightly Active / Moderately Active / Highly Active) reveals meaningfully different behavior across users.

## 🚀 Recommendations

1. Position Bellabeat around **sustainable, low-intensity movement**, not high-intensity workout tracking — that's where users actually spend their active time.
2. Use **micro-movement, routine-based notifications** to convert sedentary minutes into light activity.
3. Market **sleep efficiency** as a genuine strength — but avoid claiming it's driven by daily activity level.
4. Use **segment-specific messaging**, clearly labeled as threshold-based rather than statistically clustered.

## 📄 Project Files

- [`bellabeat_case_study.ipynb`](bellabeat_case_study.ipynb) — full analysis notebook (code + outputs + charts), also published on [Kaggle](https://www.kaggle.com/code/gulayaksoy/bellabeat-google-data-analytics-capstone)
- [`Bellabeat_Case_Study.pdf`](Bellabeat_Case_Study.pdf) — written report with the six-phase breakdown and full recommendations
- `images/` — exported chart images

## ⚠️ Limitations

Small sample (33 users for activity, 24 for sleep after cleaning), unknown demographic representativeness, data collected in 2016, third-party (non-Bellabeat) users. Findings should be validated against Bellabeat's own first-party data before being used in an actual campaign.
