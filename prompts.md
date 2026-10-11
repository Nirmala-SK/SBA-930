# Prompts used in SBA-930

The same prompt and data were given to both Claude and ChatGPT, in a new chat each time, with web search not allowed. Where a prompt shows a bracketed note, the data table (copied from the Google Sheet, 2022-2024 only) was pasted at that point.

## Prompt A: Economic policy and the stock market

```
You are a financial analyst. Below is background data.

S&P 500 monthly change statistics, Jan 2022 to Dec 2024: volatility (standard deviation of monthly change) 3.45%; worst month -7.99% (May 2022); best month +6.31% (August 2022); average monthly change +0.84%.

Federal funds rate: rose from 0.08% in January 2022 to 5.33% in August 2023, stayed at 5.33% until August 2024, then fell to 4.48% by December 2024.

Forecast the potential impact of recent economic policies, such as Federal Reserve interest rate decisions and inflation policy, on the stock market in 2025. Do not use web search.

Answer in a table with these columns: Policy factor, Expected impact on stocks (Positive, Negative or Neutral), Reasoning, Confidence (Low, Medium or High). Then predict the S&P 500's total percent change from December 2024 to December 2025, with a low and high estimate.
```

## Prompt B: Commodity price trends (WTI crude oil)

```
You are a financial analyst. Below is monthly WTI crude oil price data (dollars per barrel) from January 2022 to December 2024.

[Oil data, Jan 2022 to Dec 2024, pasted here]

Analyze the historical trend and predict the average price for each quarter of 2025 (Q1, Q2, Q3, Q4). Do not use web search. Base your forecast on this data and your general knowledge.

Answer in a table with these columns: Quarter, Forecast average price, Low estimate, High estimate. Then list your key assumptions and explain how confident you are.
```

## Prompt C: Inflation and GDP

```
You are a financial analyst. Below are two US economic datasets.

DATASET 1: Monthly CPI inflation rate (percent change from a year ago), January 2022 to December 2024.
[CPI data pasted here]

DATASET 2: Quarterly real GDP growth (percent change from the preceding quarter, seasonally adjusted annual rate), Q1 2022 to Q4 2024.
[GDP data pasted here]

Forecast two things for each quarter of 2025 (Q1, Q2, Q3, Q4): (1) the average CPI inflation rate for the quarter, and (2) real GDP growth for the quarter. Do not use web search. Base your forecast on this data and your general knowledge.

Answer in a table with these columns: Quarter, CPI forecast, CPI low, CPI high, GDP forecast, GDP low, GDP high. Then list your key assumptions and explain how confident you are.
```

## Prompt D: Risk analysis

```
You are a financial risk analyst. Below is US market data from January 2022 to December 2024.

S&P 500 monthly change statistics: volatility (standard deviation of monthly change) 3.45%; worst month -7.99% (May 2022); best month +6.31% (August 2022); average monthly change +0.84%.

Federal funds effective rate (monthly, percent):
[Federal funds data pasted here]

Identify three risks: (1) market volatility risk, (2) credit risk, and (3) liquidity risk. For each one, rate it High, Medium or Low, justify the rating by citing specific numbers from the data above, and suggest two mitigation strategies. Do not use web search. Answer in a table, then add a three-sentence summary.
```

## Prompt E: GDP forecast (optimized)

```
You are a senior macroeconomic analyst with 15 years of experience forecasting US GDP.

Below is quarterly US real GDP growth (percent change from the preceding quarter, seasonally adjusted annual rate), Q1 2022 to Q4 2024.
[GDP data pasted here]

Summary statistics for 2022-2024: average 2.44%, standard deviation 1.51 points, lowest -1.0%, highest 4.5%.

Important: quarterly GDP growth is volatile and often swings by 2 points or more from one quarter to the next. Do not simply forecast a smooth line near the average.

Task: Forecast real GDP growth for each quarter of 2025 (Q1 to Q4). Do not use web search.

Step 1: Briefly describe the pattern in the data, including how much it swings from quarter to quarter.
Step 2: Give a forecast for each quarter that reflects that volatility, with a low and high estimate (use roughly plus or minus 1.5 standard deviations).
Step 3: Present a table with columns: Quarter, GDP forecast, GDP low, GDP high.
Step 4: Review your forecast for errors and say what you are least sure about.
```
