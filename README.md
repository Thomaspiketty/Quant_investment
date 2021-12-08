# Quant_investment S&P 500 listed companies from 2018 until NOV 2021

## 1. summary

To invest in stock market is not so easy. Especially if you have a job, you can not always spend time to see display and  have a response for the buying point and selling point.
Many people ignore financial reports of companies. But I do believe that financial reports are very important for the valuation stock price. Therefore I made a investment method based on the financial reports. This is not new. The method called 'Qauant investment' exists already. I wanted to check, how would be the profit rate of the 'Quant investment' over the past 4 years in history of stock trading

## 2. Parsing and getting the ratios

In python there is a library called 'yfinance'.
Through 'yfinance' I can get the histories of stock trading, Balance sheets, Cash-Flow, annual/quarterly financial status.
I parsed the list of S&P 500 companies in Wikipedia and saved data

PE ratio, PB ratio, PC ratio, PS ratio

EPS = Net Income / the number of shares issued
PE(Price to Earning) ratio = Stock price / EPS
PB(Price to Book value) ratio = Stock price / (Total Asset - Total Liability - Intangible Asset(optinal))
PC(Price to Cash-Flow) ratio = Stock price / Cash-flow
PS ratio = Stock price / Total Sale

## 3. Strategies 

1. I put data from the last 20 years of the S&P 500 into a computer and made predictions for the next 5 days from the last day of the data.
   I used for that a Time Series analysis with ARIMA and fbprophet
   The result is as you can see not good. 
   Both ARIMA and prophet did not even match the trend of the index.


2. Long term strategies(Trading only per year or 2 years or 4years)
  1-1. PE Ratio
    I get the rank of PE Ratio, and buy the 10 stocks from the lowest number.

  1-2. PE Ratio + PB Ratio
    I get the rank of PE Ratio and PB ratio, add them up, and buy the 10 stocks from the lowest number.
    
  1-3. PER + PBR + PCR
    I get the rank of each ratios, add them up, and buy the 10 stocks from the lowest number.
    
3. Automation strategies

  2-1. PE Ratio + PB Ratio
    I get the rank of PE Ratio and PB ratio, add them up, and buy the 10 stocks from the lowest number.
    After that, when a certain rate of return or a certain loss rate occurs, the stock is sold and the index is re-ranked to invest steadily in 10 stocks.

  2-2. PE Ratio + PB Ratio + PC Ratio
    I get the rank of each ratios, add them up, and buy the 10 stocks from the lowest number.
    After that, when a certain rate of return or a certain loss rate occurs, the stock is sold and the index is re-ranked to invest steadily in 10 stocks.
    
## 4. Conclusion
My Skill to apply time series forecasting to the stock market is not enough.
But many theses has proved that it is difficult to find a certain pattern in the market trend, trend, and seasonality.
The PE Ratio, PB Ratio, PC Ratio combination strategy is successful for the investment S&P500 listed companies in last 4 years
