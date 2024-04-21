# Finance-Portfolio-Investment

This project exercises different Machine Learning algorithms to challenge the prediction of a stock value. Apple is the stock of choice<br><br>
The stock value is estimated using:

## 1. A **Rolling** method to estimate a stock value using its history 2 days ago, a week, 3 months and 4 years ago<br>

## 2. **LSTM**, a Recurrent Neural Network Deep Learning algorithm, addressing typical Gradient problems using standard RNNs. The model is defined manually, i.e. its number of layers, nodes and loss function<br>

## 3. **GPT2**, another Deep Learning algorithm based on the **Transformers** architecture, without getting bogged by sequential data processing<br>

## 4. **OpenAI**, to exercise another way to extract a GPT2 model<br><br><rb>

<hr style="border:4px solid gray">

## 1. Probability we can guess the trend of a stock at a given date

### Collect stocks of a given stock AAPL <br>

![Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'](./pictures/portfolio01List.png "Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'")<br><br>
![Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'](./pictures/portfolio01AAPL.png "Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'")<br><br>

### Define a Target Variable based on the tomorrow value <br>

Let's drop the columns Dividends and Stock Splits. Stock Splits might be an issue when we backtest the history<br>
We are building a target variable by pulling the actual value of the stock the following day. We are using the **Shift(-1)** to perform this quick operation<br><br>
![Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'](./pictures/portfolio02List.png "Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'")<br><br>

### Run Predictions<br>

We are going to add as predictors, the information regarding the stock value **2 days ago, a week, 3 months and 4 years**<br>
The rolling method is useful calculating moving averages or other rolling window calculations in time series data or any sequential data<br><br>
![Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'](./pictures/portfolio03List.png "Portfolio 'AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA'")<br><br>
For APPL, we improve from 51.9% to 53.8% with a probability of 60% to be correct, by using a backtest using up to several months of resuls<br>

## 2. Predict a stock value at a given date

Using a **LSTM** Neural Network does not provide better results. There is one path to consider, which is to look at the market opened before the USA, like in Japan or London, or the CAC40<br><br>
![Portfolio LSTM 'AAPL'](./pictures/lstm_apple_excerpt.png "Portfolio LSTM 'AAPL'")<br><br>
![Portfolio LSTM 'AAPL'](./pictures/lstm_apple_price_history.png "Portfolio LSTM 'AAPL'")<br><br>
![Portfolio LSTM 'AAPL'](./pictures/lstm_with_predictions.png "Portfolio LSTM 'AAPL'")<br><br>

## 3. Using  a LLM approach bringing up GPT2

For again the AAPL stock, we are going to use a third approach using GPT<br>

* A **GPT-2** tokenizer and pre-trained model are extracted from a **transformers** library<br>
* The historical stocks are used to fine-tune le model<br>
* Eventually this model is used to estimate the future stock prices<br><br><br>
![Portfolio GPT2 'AAPL'](./pictures/GPT_HistoricalvsPredictedStocks.png "Portfolio LSTM 'AAPL'")<br><br>

## 4. Using a LLM approach calling OpenAI
