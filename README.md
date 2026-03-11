# Attention Validation Task - Team Mavericks
Team Members - Akhila Anumalla, Kritika Joshi, S Supraja

## descriptive_statistics.Rmd
- Loads raw lab and phone CSV data
- Extracts and cleans Initial Response Time (IRT) from PsychoPy logs
- Computes descriptive statistics (mean, median, SD, skewness, kurtosis) for IRT, false alarms, and hit rate
- Saves cleaned_data.rds 

### data_visualization.Rmd
- Reads cleaned_data.rds 
- Produces 4 figures saved to figures/:
  - fig1_irt_histogram.jpeg — IRT distribution by group
  - fig2_irt_boxplot.jpeg — IRT spread and outliers
  - fig3_irt_violin.jpeg — Full IRT distribution by platform and condition
  - fig4_fa_histogram.jpeg — False alarm distribution (phone)
  - 
## Files
- phone_correlation_hypothesis.rmd
  - Contains codes that were used to generate visualizations for the Phone Environment Analysis
  - Also has Code for correlation analysis performed
  - Hypothesis testing code is also included in the file
