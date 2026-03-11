# Attention Validation Task - Team Mavericks

**Team Members:**  
- Akhila Anumalla  
- Kritika Joshi  
- S Supraja  

---

## descriptive_statistics.Rmd
- Loads raw **lab** and **phone** CSV data
- Extracts and cleans **Initial Response Time (IRT)** from PsychoPy logs
- Computes descriptive statistics:
  - Mean
  - Median
  - Standard deviation
  - Skewness
  - Kurtosis
- Performs the above analysis for:
  - IRT
  - False alarms
  - Hit rate
- Saves processed dataset as **cleaned_data.rds**

---

## data_visualization.Rmd
- Reads **cleaned_data.rds**
- Generates figures for exploratory data analysis
- Saves figures to the **figures/** directory

**Generated Figures**
- `fig1_irt_histogram.jpeg` — IRT distribution by group
- `fig2_irt_boxplot.jpeg` — IRT spread and outliers
- `fig3_irt_violin.jpeg` — Full IRT distribution by platform and condition
- `fig4_fa_histogram.jpeg` — False alarm distribution (phone)

---

## IRT_Vs_Trial_Visualization.Rmd
- Loads laboratory task CSV files for **single-target** and **multiple-target** conditions
- Extracts **Initial Response Time (IRT)** from the `mouse.time` column in PsychoPy logs
- Cleans the data by removing missing values and extreme outliers
- Assigns **trial numbers** to analyze performance across sequential trials
- Computes **median reaction time per trial** for both task conditions
- Generates a **learning curve plot** showing how median IRT changes across trials
- Helps visualize **practice (learning) effects** or **fatigue trends**

**Output**
- Line plot: **Reaction Time vs Trial Number (Learning Effect)**
- Comparison between:
  - **Single Target**
  - **Multiple Target** conditions

---

## InterTargetTimeVsTrialVisulization.Rmd
- Loads laboratory task CSV files for **single-target** and **multiple-target** conditions
- Extracts timestamp values from the `mouse.time` column in PsychoPy logs
- Converts timestamps to **milliseconds**
- Computes **inter-target time** by calculating the time difference between consecutive responses within each trial
- Aggregates the data to compute **median inter-target time per trial**
- Sets inter-target time to **0 for single-target trials** (since only one target exists)
- Visualizes how the time between locating targets changes across trials

**Output**
- Line plot: **Median Inter-Target Time Across Trials (Lab Task)**
- Comparison between:
  - **Single Target**
  - **Multiple Target** conditions
- Demonstrates how quickly participants locate additional targets across trials

---

## targetColourVsReactionTime.Rmd
- Loads laboratory task CSV files for **single-target** and **multiple-target** conditions
- Extracts **Initial Response Time (IRT)** from the `mouse.time` column in PsychoPy logs
- Converts reaction time from **seconds to milliseconds**
- Cleans the dataset by removing missing values and extreme outliers
- Groups the data by:
  - **Target color**
  - **Task condition**
- Computes **median reaction time for each target color**

**Output**
- Bar chart: **Median Reaction Time by Target Color and Condition**
- Comparison of reaction times across **different target colors**
- Shows detection speed differences between:
  - **Single Target**
  - **Multiple Target** conditions

---


## phone_correlation_hypothesis.rmd
- Contains code used for **Phone Environment Analysis**
- Generates visualizations related to phone-based task performance
- Performs **correlation analysis**
- Includes **hypothesis testing code**
