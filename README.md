# TeslaSentimentalAnalysis-

##
This project will be a testing demo for our own quantitative trading strategy. If it succeeds,
hopefully we can find a potential investor of our trading strategy:).
The main idea of our strategy is we firmly believe that daily news will definitely affect the
thinking of stockholders of a certain stock (for example, we will focus on Tesla in this project).
Analyzing the sentiment conveyed by every news would help us to predict the attitude of market
towards a stock.
##
According to the efficient market hypothesis (EMH), the market can't be beaten because all
information that could predict performance is already built into the stock price. While many
successful trading algorithms have shown that our market weren’t efficient as though before.
The reason is that investors need time to consume the information in related news about a stock.
Therefore, there will be a time lag between investors taking a corresponding action and stock
price demonstrating the sentiment of investors. If we could predict the impact of news
automatically and efficiently, it will give us a first-move advantage.

##
We also assume that information coming from the macroscopic level and microscopic level will
have different effects on the sentiment with respect to a certain stock. For instance, positive news
about technology will probably generate a positive sentiment on all stocks in technology while
negative news about politics may also have a negative sentiment on all stocks. Meanwhile,
negative analysis of a specific stock will give a negative sentiment on this stock. Thus to analyze
the comprehensive sentiment w.r.t a specified stock, we should consider the news in those two
levels.
##
Therefore, this project will be divided in four parts:
• Classify a general news by text classification algorithm (NLP). It could be business,
entertainment, politics, sport and tech. This classification model will be trained by the
data(News_Category_Dataset_v2.json) containing around 200k news headlines from the
year 2012 to 2018 obtained from HuffPost. We will mainly use news from business,
entertainment, politics, health, tech&science. (news in 2018 will be the test set).This
dataset is posted by a user named Rishabh Misra on
Kaggle( https://www.kaggle.com/rmisra/news-category-dataset ).

• Do the sentimental analysis of macro news in test set and micro analysis about tesla.
Micro analysis about tesla is collected from
https://seekingalpha.com/symbol/TSLA?s=tsla . (Please see the steps to get csv data in
appendix) We have collected analysis about tesla on this website as steps in appendix and
turn it into a csv file: tesla_analysis.csv . Those news range from 1/11/ 2018 to
12/6/2018. We will adjust our testing period in future work.
• Calculate the comprehensive sentimental scores of tesla every day, predict the movement
of stock price of tesla and use this as a guidance of our trading strategy. In this case we
will develop our own formula which would consider the effects (This formula will be
developed in project 3)
• Backtest our strategy and do some visualizations. (Historical stock price data of Tesla
would be our additional data for backtesting, we can use the dataset on Kaggle:
https://www.kaggle.com/timoboz/tesla-stock-data-from-2010-to-2020 )

Now, we can think about some tasks/questions by referring our four parts.
1. Getting familiar with data and data clean (Basic info such as # of news in each category ,
plot of tesla historical price, # of analysis about tesla in 2018,clean analysis of tesla)
2. Find most correlated words(top 5) in each category, this would be used as features in
further analysis
3. Try PCA to reduce dimension of features in 2 and do some interesting plot of projected
components
4. Classification (try different models and do some tunings of parameters on training set and
validation set then select the best one for prediction on test set, we can also do some
performance analysis such as confusion matrix)
5. Classify macro news in test set and do sentimental analysis of macro news and micro
analysis
6. (Open end) Try to figure out a robust way to calculate
comprehensive sentimental scores of tesla every day and then predict the movement of
stock price of tesla
7. Backtest by utilizing results in 6. Show essential performance indicators. (e.g Sharp ratio,
return rate)
8. (Open end) Can we adjust some parameters or even methodology in 6 to get better
results?
9. (Bonus :) probably) Visualization of backtest results. This could be developed further as
an app. (If some one would like to invest us)

## Back test visualization

![backtest](https://github.com/BBojack/TeslaSentimentalAnalysis-/assets/42468209/451a69ce-343f-45bb-898a-89791cb84043)


