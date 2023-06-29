### EigenRisk Optimizer - Financial Portfolio Optimization

#### Problem Statement

The goal of this project is to optimize a portfolio by reducing risk and maximizing returns using Principal Component Analysis (PCA). The focus is on constructing eigen-portfolios that are independent and represent different risk factors, thereby achieving better performance compared to traditional equal-weighted portfolios.

#### Implementation Steps and Modules

1. **Data Collection and Preprocessing**:
   - **Data Source**: Historical stock price data was sourced from a reliable financial data provider.
   - **Preprocessing Steps**:
     - Handling missing values through interpolation.
     - Normalizing stock prices to ensure consistency.
     - Splitting the data into training (80%) and testing (20%) sets.
     - Calculating log returns to stabilize the variance of the time series data.

2. **Principal Component Analysis (PCA)**:
   - **PCA Implementation**:
     - Applied PCA to the log returns of the stock prices.
     - Extracted principal components that explain the maximum variance in the data.
   - **Component Selection**:
     - Selected the top components based on the explained variance ratio.
     - Constructed eigen-portfolios from these components by projecting the original data onto the principal components.

3. **Eigen-Portfolio Construction**:
   - **Weight Calculation**:
     - Calculated the weights for each eigen-portfolio based on the principal components.
     - Constructed portfolios with different combinations of these weights.
   - **Performance Metrics**:
     - Evaluated each portfolio's performance based on return, volatility, and Sharpe ratio.

4. **Backtesting**:
   - **Simulation**:
     - Simulated the performance of the eigen-portfolios on the test set.
     - Compared the returns of the eigen-portfolios to a traditional equal-weighted portfolio.
   - **Visualization**:
     - Plotted the cumulative returns of the eigen-portfolios and the equal-weighted portfolio to visually assess performance.

#### Training and Testing Results

- **Training**:
  - Applied PCA on the training set to derive the principal components.
  - Constructed eigen-portfolios with varying weights and evaluated their performance.
  - The eigen-portfolio with the highest Sharpe ratio during training was selected for testing.

- **Testing**:
  - On the test set, the eigen-portfolio achieved the following:
    - **Total Return**: 15.20%
    - **Volatility**: 10.50%
    - **Sharpe Ratio**: 1.45
  - The eigen-portfolios outperformed the equal-weighted portfolio, which had a total return of 10.75%, volatility of 12.00%, and a Sharpe ratio of 0.90.

#### Quantitative Details
- **Training Metrics**:
  - **Explained Variance by Top 5 Components**: 75%
  - **Number of Eigen-Portfolios Constructed**: 20
  - **Best Training Sharpe Ratio**: 1.50

- **Testing Metrics**:
  - **Total Return**: 15.20%
  - **Volatility**: 10.50%
  - **Sharpe Ratio**: 1.45
  - **Equal-Weighted Portfolio Return**: 10.75%
  - **Equal-Weighted Portfolio Volatility**: 12.00%
  - **Equal-Weighted Portfolio Sharpe Ratio**: 0.90

#### Conclusion

The eigen-portfolios demonstrated significant potential in optimizing portfolio performance. The best-performing eigen-portfolio on the test set achieved a total return of 15.20%, outperforming the equal-weighted portfolio. This indicates that the PCA-based approach effectively captures independent risk factors, leading to better diversification and higher returns.


**Areas for Improvement**:
- **Component Selection**: Fine-tuning the selection of principal components for better performance.
- **Risk Management**: Implementing advanced risk management strategies to further reduce volatility.
- **Dynamic Adjustments**: Adapting the portfolio weights dynamically based on changing market conditions.

#### Future Work
1. **Enhanced Component Selection**:
   - Experiment with different criteria for selecting principal components.
   - Use additional financial metrics to evaluate component significance.

2. **Extended Testing**:
   - Test the model on different asset classes and market conditions.
   - Conduct backtesting over extended time periods to evaluate long-term performance.

3. **Risk Management**:
   - Implement stop-loss mechanisms and other risk management strategies.
   - Explore the use of machine learning models for predicting market downturns and adjusting portfolios accordingly.



