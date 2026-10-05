# RF Stock Statistical Analysis

I completed this Excel project for QNT 2020 at Baruch College using Regions Financial (RF) stock and financial data. I used statistics to study daily returns, quarterly financial results, and the relationship between earnings per share and stock price.

## What this project is for

The project gave me practice turning source data into calculations, tests, and charts in Excel. The questions were whether stock returns look normally distributed, how samples vary, whether recent financial results differ from history, whether net margins vary by quarter, and how earnings relate to share prices. It is a historical class analysis, not a current company valuation or investment recommendation.

## Open the workbook

Download `1-RF-Stock-Statistical-Analysis.xlsx` and open it in Excel. GitHub does not display an Excel preview. The workbook opens on the `RF` analysis sheet at cell F19, at 85% zoom.

The full long analysis sheet is included. Use Excel's Name Box to jump to a cell:

| Section | Starting cell | What is there |
| --- | --- | --- |
| Chapter 12 | F19 | EPS/price regression and four charts |
| Chapter 11 | F89 | Quarterly net-margin ANOVA and equal-variance check |
| Chapter 9 | F109 | Historical versus recent financial-result tests |
| Chapter 8 | F149 | Sampling and confidence intervals |
| Chapter 7 | F179 | Daily log-return statistics and empirical-rule comparison |
| Daily data calculations | F189 | Price series, returns, and return buckets |
| Financial data calculations | F2959 | Quarterly financial series and growth measures |

There is no Chapter 10 section in my original workbook. The other three tabs contain the price history, quarterly income statements, and dividend history used as reference data. They are not substitutes for the analysis and have been kept unchanged.

## Assignment

In my own words, these were the tasks:

- Chapter 7: Check whether daily log returns resemble a normal distribution. Calculate the mean, standard deviation, skewness, and kurtosis; group returns by distance from the mean and compare their frequencies with the empirical rule.
- Chapter 8: Draw ten samples of ten returns, check for duplicates, and calculate 80% confidence intervals using population-SD and sample-SD assumptions. Compare sample means and intervals with the full-data mean.
- Chapter 9: Compare 2025 Q2-Q3 revenue, net income, and their quarterly growth rates with historical means using two-tailed tests at 90% confidence. Repeat with known- and unknown-SD assumptions, using critical values and p-values. The assignment framed this around tariff timing; this comparison alone cannot establish a tariff effect.
- Chapter 11: Organize 2016-2024 net margins by calendar quarter, calculate descriptive statistics, run one-way ANOVA at the 5% level, and use Hartley's test to check equal variances.
- Chapter 12: Match quarterly closing prices to basic EPS, run a simple linear regression, and examine the scatter, fitted-line, residual, and normal-probability charts.

## Findings

These findings describe the data and results stored in my workbook, not the company's position today.

### Daily returns and risk

Across 2,514 daily log returns, the average was about 0.038% and the standard deviation was about 2.30%. The average return was small compared with daily movement. Skewness was -0.62 and excess kurtosis was 10.19, suggesting a longer downside tail and more extreme moves than a normal distribution. A normal curve is therefore a limited description of this return sample.

### Sampling and confidence intervals

Nine of the ten sample confidence intervals contained the full-data mean at the workbook's 80% confidence level. Each sample had ten observations. This illustrates sampling uncertainty; it is not a forecast or a stock-price prediction interval. The exercise assumes normality even though the return checks give reasons to question that assumption.

### Recent financial results versus history

The workbook reports mean quarterly revenue of $1,910.5 million for 2025 Q2-Q3, compared with $1,601.3 million in the historical control range. Its unknown-SD test gives p = 0.0225, below the assignment's 10% significance level. The net-income, revenue-growth, and net-income-growth tests did not reject their historical-mean nulls (p = 0.292, 0.275, and 0.651).

I read this as a limited signal of higher revenue in the two recent quarters, not proof of lasting improvement. Only two quarters are in the recent period, and the calculations use historical variability. These tests do not show that tariffs caused the difference.

### Net margins by calendar quarter

For 2016-2024, average net margins were 34.05%, 32.01%, 35.16%, and 35.21% for Q1 through Q4. ANOVA gives p = 0.9446, so it does not identify a clear difference between quarter means. However, Hartley's variance ratio is 13.61, above the workbook's critical value of 6.31. The equal-variance assumption fails this check, so I treat the ANOVA conclusion cautiously rather than declaring that margins have no seasonality.

### Earnings and stock price

The fitted regression uses 38 observations and shows a positive association between basic EPS and closing price. R-squared is 0.469, so the model accounts for about 47% of the variation in closing prices within that sample. The fitted slope is about $15.31 of closing price per $1 of EPS, with a 95% interval of $9.80-$20.81.

This does not mean that a $1 increase in EPS causes a $15.31 price increase. More than half of the sample's price variation is outside this one-variable model, and the class exercise does not address other influences or the time-series structure.

### My takeaway

Stronger earnings are associated with higher share prices in this sample, but earnings alone do not explain the whole price pattern. Daily returns have heavy tails, and the short recent-period comparison is too limited for a broad claim that the company is improving.

## Data sources

I kept the three source-data tabs with the workbook:
- Daily price history: the historical-price export used for the assignment, which directed students to Nasdaq.
- Quarterly income statements: the Mergent Market Atlas export accessed through Baruch's library.
- Dividend history: the company investor-relations data collected for the assignment.

These are historical source snapshots, not live feeds. The source tabs were not changed during portfolio cleanup. The assignment instructions are paraphrased above; the course PDFs are not included.

## Revisions after feedback

I revised the workbook after instructor feedback:
- Added references in the expected critical-value cells to my existing correct z and t values.
- Replaced seven fixed values in the empirical-rule section with live formulas. The stored results stayed the same.
- Removed eight charts linked to the example stock, keeping the four RF charts.
- Removed grading marks, checker and expected-answer bands, and external example-workbook links from this portfolio copy.
- Set the opening view to the RF analysis so readers can find the chapter work immediately.

I kept my chapter analysis and the original RF source-data tabs. The cleanup did not turn the workbook into a different analysis or invent corrections for unexplained deductions.
