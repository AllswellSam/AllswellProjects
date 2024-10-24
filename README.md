Overview:
-
Apple Stocks( 1999 -2024) is an R script with codes that analyze Apple's stock data (AAPL_stock_price.csv). It cleanses the dataset, provides descriptive statistics, plots graphs, performs correlation analysis, etc.
The Apple stocks dataset (AAPL_stock_price.csv) was downloaded from Kaggle (https://www.kaggle.com/datasets/prathamjyotsingh/apple-stocks ) and saved into my local drive or directory.
This data set contains variables such as Apple's stock close price, high price, volume, etc which provides some 
information on the Stock's trend, volatility, and market performance (1990 to 2024).

Objectives:​
-
- Analyze trends in Apple’s stock price.​
- Evaluate daily returns and volatility.​
- Identify key insights from trading volume and stock movements​

Research Questions:​ 
-
- How has Apple’s stock price evolved over time?​
- What is the typical range of daily returns?​
- Are there any correlations between trading volume and stock price movement?​

How to Run the Code:
-
 - Run the codes in an R terminal.
 - Some packages like tidyverse, lubridate and pacman may need to be installed before loaded if you have not already done so
 - The dataset may need to be saved in the same folder directory as the that of your R project.

Results and Conclusion:
-
Apple's stocks showed the following characteristics between the years 1990 and 2024:
- Consistent Long-Term Growth:​ The mean daily return of 0.08% indicates steady long-term growth in Apple's stock price. Over time, the stock tends to appreciate, though daily changes are often small.​

- Significant Daily Volatility:​ With a standard deviation of 2.97%, Apple's stock shows considerable daily volatility. Although the mean return is small, there are frequent fluctuations, with potential for both gains and losses.​
The minimum return of -85.49% and maximum return of 13.90% highlight some extreme days, likely driven by market-wide events or company-specific developments (Bodie et al., 2021).​

- High Trading Volume:​ Apple’s stock sees robust investor interest, with an average daily trading volume of 33.1 million shares. This high trading activity indicates strong liquidity and consistent market engagement (Fama, 1970).​

- Large Variations in Trading Volume:​ The standard deviation of 30.6 million shares in trading volume shows that while trading is generally high, it can spike dramatically on certain days, likely in response to earnings reports, product launches, or macroeconomic factors (Sharpe et al., 1999).​

- Volume Spikes Align with Significant Events:​ The maximum trading volume of 332.6 million shares indicates major trading spikes, often seen during critical events like product releases or financial announcements, when investor activity surges (Hull, 2017).​

- Weak Negative Correlation Between Price and Volume:​ The correlation coefficient of -0.041 suggests a weak negative relationship between closing price and trading volume, meaning that higher prices may slightly correspond with lower trading volumes (Malkiel, 2019).​

References:
-
- Singh, P. (2024). Apple stocks [Data set]. Kaggle. Link​
- Bodie, Z., Kane, A., & Marcus, A. J. (2021). Investments (12th ed.). McGraw-Hill Education.​
- Fama, E. F. (1970). Efficient capital markets: A review of theory and empirical work. The Journal of Finance, 25(2), 383–417. 
- Hull, J. C. (2017). Options, futures, and other derivatives (10th ed.). Pearson.​
- Sharpe, W. F., Alexander, G. J., & Bailey, J. V. (1999). Investments (6th ed.). Prentice Hall.​
- Malkiel, B. G. (2019). A random walk down Wall Street (12th ed.). W.W. Norton & Company.​
