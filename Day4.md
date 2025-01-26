# Class Notes on Statistics

## Introduction to Statistics
Statistics is the science of decision-making. It involves collecting, analyzing, interpreting, and presenting data to aid in decision-making. Statistics can be broadly categorized into two types:

1. **Descriptive Statistics**: Summarizes and describes the main features of a dataset.
2. **Inferential Statistics**: Draws conclusions and makes predictions about a population based on sample data.

---

## Measures of Central Tendency
Central tendency measures summarize a dataset with a single value that represents the center or typical value of the data.

### 1. Mean (Average):
- Represents the sum of all data points divided by the number of data points.
- Best used when the data distribution is symmetric.
- Sensitive to extreme values (outliers).

### 2. Median:
- The 50th percentile of the data.
- Half of the data points lie above the median, and half lie below.
- Useful when the data distribution is skewed or has outliers.

### 3. Mode:
- The value that appears most frequently in the dataset.
- Can be used for both numerical and categorical data.

### 4. Percentiles:
- Percentiles divide the dataset into 100 equal parts.
- **75th Percentile (Q3)**: Represents the value below which 75% of the data falls.
- **25th Percentile (Q1)**: Represents the value below which 25% of the data falls.
- Importance:
  - Help in understanding data spread and identifying outliers.
  - Used to calculate the Interquartile Range (IQR).

---

## Measures of Dispersion
Dispersion measures describe the spread or variability of the data.

### 1. Range:
- Difference between the maximum and minimum values.

### 2. Standard Deviation:
- Indicates how much the data deviates from the mean on average.

### 3. Quartiles:
- Divide the data into four equal parts.
  - **Q1 (25th Percentile)**: Lower quartile.
  - **Q2 (50th Percentile)**: Median.
  - **Q3 (75th Percentile)**: Upper quartile.
- **Outliers**:
  - Identified using the following bounds:
    - **Lower Bound**: Q1 – 1.5 × IQR
    - **Upper Bound**: Q3 + 1.5 × IQR

---

## Correlation
Correlation measures the relationship between two variables.

### 1. Pearson Correlation Coefficient:
- Measures the linear relationship between two variables.
- Ranges from –1 (perfect negative correlation) to +1 (perfect positive correlation).

### 2. Spearman Rank Correlation Coefficient:
- Measures the strength and direction of the monotonic relationship between two variables.

### 3. Scatter Plot:
- Visualizes the relationship between two variables.
- Helps identify patterns or correlations.

---

## Histogram and Probability Density Function
Histograms represent the distribution of a dataset using bars.

### 1. Bell Curve (Normal Distribution):
- Symmetrical distribution where:
  - 68% of the data lies within one standard deviation of the mean.
  - 98% of the data lies within two standard deviations of the mean.

### 2. Bimodal Distribution:
- A distribution with two distinct peaks.

### 3. Cumulative Density Function (CDF):
- Represents the cumulative sum of histogram bars.

---

## Scaling
Scaling is essential to normalize data for comparisons and model training.

### 1. Z-Score:
- Measures how many standard deviations a data point is from the mean.

### 2. Min-Max Scaling:
- Scales the data to a fixed range, typically [0, 1].

---

## Types of Distributions

### Skewed Distribution:
- **Positive Skew**: Tail is longer on the right.
- **Negative Skew**: Tail is longer on the left.

---

## Why Do We Need Both Variance and Standard Deviation?
- **Variance**: Measures the average squared deviation from the mean. Useful in theoretical contexts.
- **Standard Deviation**: Provides a measure of spread in the same units as the data, making it more interpretable in practical scenarios.

