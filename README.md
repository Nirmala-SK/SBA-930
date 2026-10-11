# SBA-930: Evaluating LLMs for Financial Forecasting and Risk Analysis

This project tests how well two large language models (LLMs), **Claude** and **ChatGPT**, can support financial forecasting and risk analysis. Both models received the same prompts and the same data (2022-2024) and were asked to forecast 2025. Their forecasts were then compared with the actual 2025 values.

> This is a class exercise. It is not investment advice.

## Repository contents

| File | Description |
|---|---|
| `Nirmala_SBA_930_Report.docx` | Full project report (Per Scholas template) |
| `SBA930 Results.xlsx` | Google Sheets workbook exported to Excel: prompt log, scores, forecast vs actual tables, and source data |
| `prompts.md` | The five prompts used with both LLMs |
| `README.md` | This file |

## Data

All data come from [FRED](https://fred.stlouisfed.org) (Federal Reserve Bank of St. Louis), downloaded in October 2026.

| Dataset | FRED series |
|---|---|
| Historical stock prices | S&P 500 (`SP500`), monthly |
| Economic indicators | CPI inflation, % change from a year ago (`CPIAUCSL`) |
| Economic indicators | Real GDP growth, annualized (`A191RL1Q225SBEA`) |
| Economic indicators | Federal funds effective rate (`FEDFUNDS`) |
| Economic indicators | WTI crude oil price (`DCOILWTICO`) |

The LLMs saw data through December 2024 only. The 2025 values were kept hidden and used as the answer key.

## Method

1. Downloaded the datasets from FRED and loaded them into Google Sheets.
2. Wrote five prompts: stock market and policy (A), oil prices (B), inflation and GDP (C), risk analysis (D), and an optimized GDP forecast (E).
3. Ran each prompt in a new chat on Claude and ChatGPT, with web search not allowed.
4. Compared forecasts with actual 2025 values (absolute error, percent error, and whether the actual value fell inside the low-high range).
5. Scored every response from 1 to 5 for accuracy, relevance and reliability.
6. Improved the GDP prompt (role, context, volatility warning, step-by-step structure, self-check) and re-tested it.

## Key results

| Test | Claude | ChatGPT |
|---|---|---|
| Oil price, average error (dollars per barrel) | 5.33 | 9.04 |
| Inflation (CPI), average error (percentage points) | 0.20 | 0.27 |
| GDP growth, original prompt, average error (points) | 1.93 | 1.85 |
| GDP growth, optimized prompt, average error (points) | 1.35 | 1.65 |
| S&P 500 change Dec 2024 to Dec 2025: forecast vs actual (+14.0%) | +8% | +9% |
| Average scores (accuracy / relevance / reliability) | 3.8 / 5.0 / 4.8 | 3.4 / 4.8 / 3.4 |

**Main findings**

- Claude was closer to the actual values in three of the five numeric tests, and ChatGPT in two.
- Both models handled slow-moving data (inflation) well but missed sudden changes (the fall in oil prices and the swings in GDP growth).
- Prompt optimization reduced the GDP forecast error by about 30% for Claude and 11% for ChatGPT.

## Limitations

- Each test used four quarterly forecasts and one run per model, so differences may partly be chance.
- The S&P 500 and oil values are monthly averages, so the S&P 500 change is approximate.
- 2025 has already happened, so the models may know the real outcomes.
- The 1-5 scores are subjective, and the free model versions may differ from paid ones.

## Disclaimer

This project is for educational purposes only and is not financial advice.
