## Business Problem Framing

An investment company, XYZ Inc. is planning to make a substantial investment in Coca-Cola (KO) stock. The team need to understand quantitative returns and risk associated with the stock and overall market. 

The team believes that higher trade volume relative to previous trading period tends to reduce the returns of S&P500 and need a scientific approach to their belief.

## Analytic problem framing

Returns and risks can be measured over different period. This analysis consists of daily, weekly, monthly and quarter period.

1) Analyze returns - Returns in its simplest terms means, how much money has being made?  
Arithmetic average or log returns are two of the preferred method. Others being trimmed mean, harmonic mean etc.

2) Analyze market risk - Market risk, is the uncertainty inherent to the entire market. Examples include interest rates, recession and wars.  
Beta is a numeric value that measures the fluctuations of a stock to changes in entire market.

3) Hypothesis testing - Higher trade volume relative to previous trading period tends to reduce the returns of S&P500.  
Ha = If there is an increase in volume from previous period, on average the returns of S&P500 decreases.   
Ho = If there is an decrease in volume from previous period, on average the returns of S&P500 increases.  
We will use the Welch t-test statistic for testing our hypothesis.  

## Data

Two flat files are available - historical records for S&P500 and Coca-Cola (KO).  

As OHLC figures prior to 1961 are same, they are removed.  

Preprocessing steps such as adjustment for split and bonus, missing values, duplicate records and outlier has been validated.   

## Analysis

### Returns

As discussed, the common approach for stock returns are arithmetic mean or log returns. The calculation are as follows:

Arithmetic mean =  sell price - buy price / buy price  
Log return = Natural log of (sell price / buy price)  

In the following table we notice that arithmetic returns are biased towards positive, hence we use log returns.

Table:- 

| Sr no | Buy Price | Sell price | Arithmetic return  | Log return |
|-------|-----------|------------|--------------------|------------|
| 1     | 200       | 100        | -100%              | -30%       |
| 2     | 100       | 200        |  50%               |  30%       | 
