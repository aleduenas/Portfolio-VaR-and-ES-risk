# Value at Risk and Expected Shortfall

This Python script calculates the Value at Risk (VaR) and Expected Shortfall (ES) for a portfolio of stocks using three different methods: Covariance (Var-Covar), Historic, and Monte Carlo simulation. It also visualizes these risk measures and the log returns of the individual stocks in the portfolio.

## Code Usage

This script uses a .csv data file containing stock prices. The required data structure is a .csv file where each column corresponds to a different stock's daily closing price. The order of the stocks is Amazon (AMZN), Toronto-Dominion Bank (TD), Tesla (TSLA), and Alphabet Inc Class A (GOOGL).

The script calculates the VaR and ES for different confidence levels (97%, 95%, and 99%) using a window of 252 trading days. The portfolio is equally weighted across all stocks.

To run the script, simply execute it in a Python environment.

## Required Libraries

The script uses the following libraries:

- `numpy`
- `pandas`
- `scipy.stats`
- `matplotlib.pyplot`

## Code Explanation

The script begins by reading the data from the .csv file and converting it into numpy arrays. Then, it calculates the log returns of the portfolio.

After defining the investment and weights, it defines three functions to calculate VaR and ES:

- `varcovar_method`: Uses the variance-covariance method.
- `historic_method`: Uses historical data.
- `montecarlo_method`: Uses Monte Carlo simulation.

Another function, `rolling_window`, is defined to use a rolling window approach on the data.

The script then applies these functions to calculate VaR and ES for each method over the specified rolling window. These results are then plotted over time, and the plots are displayed.

Finally, the script calculates VaR and ES for different window sizes (6 months and 2 years) and plots the distribution of log returns for each stock.

Note: The lines of code that save the plot images to the local disk are currently commented out. If you wish to save the plots as .png files, you can uncomment those lines of code.

## Disclaimer

This script is for educational purposes only. It should not be used for making real investment decisions. The calculation methods used in the script are simplified and may not fully capture the risk characteristics of a portfolio.
