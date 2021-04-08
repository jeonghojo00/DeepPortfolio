# DeepPortfolio
This project was inspired by the Video "Deep portfolio: using neural networks for portfolio construction" by Anant Gupta
< https://youtu.be/7LOb9kk6U_M >

## Calculations
Stock Returns: R = (X_t2 - X_t1) / X_t1 \
Rolling Returns: Series of Returns \
Correlations can sometimes be deceiving
Correlations are better than Covariance for making choice decisions

W: Weights of individual stocks in a portfolio
R: Returns of individual stocks in a portfolio
Sigma: Covariance matrix of stocks ina portfolio

Portfolio:
    Returns: This will levaerge X and W matrics, come up with how much gained or loss over a period of time
    Risk: This will leverage Covariance and W matrics, come up with houw much gained or loss over a period of time
    
    Returns vs. Risk graph

Current Portfolio Construction
    Efficient Frontier
    CAPM (Capital Asset Pricing Model)
    Arbitrage Pricing Theory
    
## Step
1. AutoEncoders: Get patterns in a unsupervised manner
    - input -> Latent Features -> Input
2. Stock Selection
    - Find RMSE (Root Mean Squared Error) between original and recreated matrix
    - Output: Top 50 Stocks with Least RMSE
    -         Top 50 Stocks with Most RMSE

3. Portfolio Rejig
    - Find the most optimum actions to undertake to arrive at the optimum portfolio from an existing portfolio
    - Lesser Transactions
    - Lesser number of total stocks
    - Maimize Returns
    - Minimize Risk
    - Loss Function: Loss = tf.reduce_sum(ret) + tf.reduce_sum(devPortfolio) + changeWeight + weightLoss
    - Optimizer: optimizer = tf.train.AdamOptimizer(0.001).minimize(loss)

4. Asset Allocation
    - Get updated weights for each stock
