name : exponential moving average
tags : 
backlinks : 
source : https://medium.com/analytics-vidhya/understanding-exponential-moving-averages-e3f020d9d13b
https://www.statology.org/excel-exponential-moving-average/
https://www.investopedia.com/ask/answers/122314/what-exponential-moving-average-ema-formula-and-how-ema-calculated.asp

###### Content:
An exponential moving average is a type of moving average which gives more weight to recent observations, allowing it to adapt to trends more quickly. The exponential moving average $\hat{y}_{t+1|t}$ can be evaluated using the following equation:

$$\hat{y}_{t+1|t} = \alpha y_t + (1-\alpha)\hat{y}_{t|t-1}$$
where

$$\hat{y}_{t|t-1} = \alpha(1-\alpha)y_{t-1}+ \alpha(1-\alpha)^2y_{t-2}+...+\alpha(1-\alpha)^ny_{t-n}$$
with $n$ being the number of most recent data points being included in the calculation, and $\alpha$ as the smoothing parameter between 0 and 1. The value for $\alpha$ is calculated using the equation:
$$\alpha = \frac{2}{n+1}$$


###### Properties:
- See medium link above for EMA's use in [[reinforcement learning]] and [[deep neural network]]s (mainly with reference to weight adjustment)
- Used to forecast the price of stock, where $\hat{y}_{t+1|t}$ is the foretasted price of the stock (or $t+1$) given the current price at time $t$

###### Additional Thoughts:
