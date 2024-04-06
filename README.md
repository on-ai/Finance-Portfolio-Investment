# Finance-Portfolio-Investment
## Overall trend for several NASDAQ Stocks
![Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'](./pictures/portfolio01GOOG.png "Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'")<br><br>
![Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'](./pictures/portfolio01AMZN.png "Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'")<br><br>
![Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'](./pictures/portfolio01MSFT.png "Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'")<br><br>
![Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'](./pictures/portfolio01TSLA.png "Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'")<br><br>
## Collect stocks of a given stock APPL <br>
![Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'](./pictures/portfolio01List.png "Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'")<br><br>
![Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'](./pictures/portfolio01APPL.png "Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'")<br><br>

## Define a Target Variable based on the tomorrow value <br>
Let's drop the columns Dividends and Stock Splits. Stock Splits might be an issue when we backtest the history<br>
We are building a target variable by pulling the actual value of the stock the following day. We are using the **Shift(-1)** to perform this quick operation<br><br>
![Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'](./pictures/portfolio02List.png "Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'")<br><br>
## Run Predictions<br>
We are going to add as predictors, the information regarding the stock value **2 days ago, a week, 3 months and 4 years**<br>
The rolling method is useful calculating moving averages or other rolling window calculations in time series data or any sequential data<br><br>
![Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'](./pictures/portfolio03List.png "Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'")<br><br>
For APPL, we improve from 51.9% to 53.8% with a probability of 60% to be correct, by using a backtest using up to several months of resuls<br>
Using a LSTM Neural Network does not provide better results. There is one path to consider, which is to look at the market opened before the USA, like in Japan or London, or the CAC40.