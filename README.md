# **Twitch Streamer Performance Analysis**

## ***Overview***

This project analyzes performance data from the top 1,000 Twitch streamers to understand what drives follower growth on the platform. Using exploratory data analysis, hypothesis testing, and predictive modeling, the project identifies key factors associated with streamer success and builds a regression model to quantify their impact.

The goal is not just to describe Twitch metrics, but to translate them into actionable insights about audience growth and engagement.

## ***Dataset***

Source: Twitch Streamers Data

Size: 1,000 channels × 11 variables

Data Types:

- Engagement Metrics: Watch time, stream time, peak viewers, average viewers, followers, followers gained, views gained

- Channel Attributes: Partnered status, mature content flag, broadcast language

## ***Data Quality***

The dataset required no preprocessing:

- ✅ No missing values

- ✅ No duplicate records

- ✅ All variables well-defined and analysis-ready

## ***Exploratory Data Analysis (EDA)***

Key observations from the exploratory phase:

- Highly skewed engagement metrics: A small number of streamers capture the majority of viewers and watch time.

- Wide variation in stream duration: Some channels stream far longer than average, suggesting differing growth strategies.

- Peak vs. average viewers: Many channels experience occasional spikes that significantly exceed their typical audience size.

These patterns highlight a “winner-takes-most” dynamic common in large content platforms.

## ***Hypothesis Testing***

Question: Does broadcast language affect follower growth?

- Method: Welch Two-Sample t-test

- Groups: English vs. non-English channels

- Result: No statistically significant difference in followers gained (p = 0.84)

Conclusion: Language alone does not meaningfully influence follower growth among top Twitch streamers.

## ***Predictive Modeling***

A multiple linear regression model was built to predict followers gained.

***Model Selection***

Initial predictors were refined using forward and backward stepwise regression (AIC-based). Both methods converged on the same final model:

***Final predictors:***

- Existing followers

- Watch time (minutes)

- Stream time (minutes)

- Partnered status

***Key Insights***

- Existing followers strongly predict future growth, indicating momentum effects.

- Watch time has a positive impact on follower gains.

- Longer stream times are associated with diminishing returns when controlling for other factors.

- Partnered channels tend to grow more slowly once maturity is accounted for.

***Model Performance***

- Adjusted R²: ~0.60

- Model diagnostics confirmed acceptable linear regression assumptions.

