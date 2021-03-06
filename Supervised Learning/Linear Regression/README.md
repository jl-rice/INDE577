# Linear Regression: Time Series (Autoregressive) Model for Financial Data

### Autoregressive(p) model:

An autoregressive (![](https://latex.codecogs.com/svg.latex?AR)) model predicts future behavior based on past behavior. It’s used for forecasting when there is some correlation between values in a time series and the values that precede and succeed them. An ![](https://latex.codecogs.com/svg.latex?AR%28p%29) model is an autoregressive model where specific lagged values of ![](https://latex.codecogs.com/svg.latex?y_t) are used as predictor variables. Lags are where results from one time period affect following periods.

<img src="https://otexts.com/fpp2/fpp_files/figure-html/arp-1.png" width="630"/>

For example, an ![](https://latex.codecogs.com/svg.latex?AR%281%29) would be a “first order autoregressive process.” The outcome variable in a first order ![](https://latex.codecogs.com/svg.latex?AR) process at some point in time ![](https://latex.codecogs.com/svg.latex?t) is related only to time periods that are one period apart (i.e. the value of the variable at ![](https://latex.codecogs.com/svg.latex?t%20-%201)). An ![](https://latex.codecogs.com/svg.latex?AR%28p%29) model can be denoted as below.

![](https://latex.codecogs.com/svg.latex?X_t%20%3D%20c%20&plus;%20%5Csum_%7Bi%20%3D%201%7D%5E%7Bp%7D%5Cdisplaystyle%20%5Cvarphi%20_%7Bi%7D%20X_%7Bt%20-%20i%7D%20&plus;%20%5Cepsilon_t)

Here, ![](https://latex.codecogs.com/svg.latex?%5Cdisplaystyle%20%5Cvarphi%20_%7B1%7D), ..., ![](https://latex.codecogs.com/svg.latex?%5Cdisplaystyle%20%5Cvarphi%20_%7Bp%7D) are the parameters of the model, ![](https://latex.codecogs.com/svg.latex?c) is a constant, and ![](https://latex.codecogs.com/svg.latex?%5Cepsilon_t) is white noise. 

### Linear regression model:
A linear regression model is a linear approach for modelling the relationship between a scalar response and one or more explanatory variables. It can be written as ![](https://latex.codecogs.com/svg.latex?%7B%5Cdisplaystyle%20%7By%7D%20%3D%20X%7B%7B%5Cbeta%20%7D%7D&plus;%7B%7B%5Cvarepsilon%20%7D%7D%7D), where ![](https://latex.codecogs.com/svg.latex?y) is a vector of observed values ![](https://latex.codecogs.com/svg.latex?%5Cdisplaystyle%20y_%7Bi%7D). ![](https://latex.codecogs.com/svg.latex?X) is a matrix of row-vectors ![](https://latex.codecogs.com/svg.latex?%5Cdisplaystyle%20%7Bx%7D_%7Bi%7D). ![](https://latex.codecogs.com/svg.latex?%5Cbeta) is a ![](https://latex.codecogs.com/svg.latex?%7B%5Cdisplaystyle%20%28p&plus;1%29%7D) dimensional parameter vector, where ![](https://latex.codecogs.com/svg.latex?%7B%5Cdisplaystyle%20%5Cbeta%20_%7B0%7D%7D) is the intercept term. ![](https://latex.codecogs.com/svg.latex?%7B%5Cdisplaystyle%20%7B%7B%5Cvarepsilon%20%7D%7D%7D) is a vector of values ![](https://latex.codecogs.com/svg.latex?%7B%5Cdisplaystyle%20%5Cvarepsilon%20_%7Bi%7D%7D).

In statistics, ordinary least squares (OLS) chooses the parameters of a linear function of a set of explanatory variables by the principle of least squares: minimizing the sum of the squares of the differences between the observed dependent variable (values of the variable being observed) in the given dataset and those predicted by the linear function of the independent variable. Using OLS, ![](https://latex.codecogs.com/svg.latex?%5Chat%7B%7B%5Cbeta%7D%7D) is obtained through the formula ![](https://latex.codecogs.com/svg.latex?%5Chat%7B%7B%5Cbeta%7D%7D%3D%5Cleft%28%7BX%7D%5E%7B%5Ctop%7D%7BX%7D%5Cright%29%5E%7B-1%7D%20%7BX%7D%5E%7B%5Ctop%7D%7By%7D). Accordingly, ![](https://latex.codecogs.com/svg.latex?%5Chat%7By%7D%20%3D%20X%5Chat%7B%5Cbeta%7D).

# References

Autoregressive model: definition & the AR process. Statistics How To. https://www.statisticshowto.com/

Autoregressive model. Wikipedia. https://en.wikipedia.org/wiki/Autoregressive_model

Linear regression. Wikipedia. https://en.wikipedia.org/wiki/Linear_regression
