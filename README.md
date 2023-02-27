# Basket Asian Relative Performance Option Valuation

A pricing model for basket Asian relative performance options (RPO) is proposed by using Monte Carlo simulation. In a basket Asian RPO, payoff is determined by the difference between the performance of a reference stock and that of a basket of stocks, where performance is defined as the ratio of (weighted) average of two sets of averaging dates.

Let   be a reference stock and   be N stocks in a given basket,   be the price process of the jth stock and  .  Let   be an “initial” set of reset dates and   a “final” set of reset dates, and assume  .  The price of each stock is recorded on these reset dates to obtain price arithmetic averages of   and   corresponding to the initial set of reset dates and the final set of reset dates, respectively.  Weighted averages of   and   are then defined as
				 ,
where   are the weights for the stocks in the basket.

Let   be a payoff settlement date or maturity.  The basket Asian RPO is a European style derivative security whose matured payoff at the settlement date T is given by
					 

where the functional   specifies how many shares of   should be rewarded as a function of the relative performance, ( ).  It should be noted here that stock dividends are assumed reinvested at the market price when the dividends are paid, so that the model simply assumes that the stocks do not pay dividends.

Let t be the current value date, then the current value of this derivative security can be written as
				 

where   is the discount factor at the value date (see https://finpricing.com/lib/FxForwardCurve.html). The above formulae are in a world that is forward risk-neutral with respect to a specific currency  .  If an underlying asset j is measured in another currency  , the governing price dynamics of this underlying asset in the risk-neutral world of   should be written as

			 

where   is the short rate of  ,   is the correlation coefficient between the asset price and the cross-currency exchange rate,   is the volatility of the asset price,   is the volatility of the exchange price, and   is the Wiener process.  Asset prices are correlated with   where  ’s are constant correlation coefficients between the logarithmic asset prices.  All these parameters are assumed deterministic.

Monte Carlo simulation associated with stratified sampling variance deduction is employed to evaluate the option.  In the first sample transaction, there are six stocks, one as a reference, and the other five in a basket with equal weight.  These underling stocks and the option are all measured in CAD.

