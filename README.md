The "Model Implied VIX" code models and estimates VIX using an adjusted GARCH model. 
It retrieves S&P 500 and VIX data, calculates the time series of conditional volatility (ht) and pricing errors. 
An optimization procedure (differential evolution) minimizes the log-likelihood function based on VIX and model-implied VIX.
The final estimated parameters are used to compute and plot the model-implied VIX against the actual VIX data. Finally, it evaluates key statistics, such as long-run variance and gamma.
It is noted that for the creation of the code the "VIX-Only approach" found in Wang (2016) was used.

The second part of the code calculates VIX futures prices based on the Heston-Nandi GARCH model using parameters estimated in "Model-Implied VIX". It defines functions for iterative calculations of  H  and  C , followed by the VIX futures price calculation via numerical integration. VIX data is fetched from Yahoo Finance, and futures prices are computed for each date using the defined parameters. 
The results are then plotted to show results

