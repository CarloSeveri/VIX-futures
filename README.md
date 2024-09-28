The "Model Implied VIX" code models and estimates VIX using an adjusted GARCH model. 
It retrieves S&P 500 and VIX data, calculates the time series of conditional volatility (ht) and pricing errors. 
An optimization procedure (differential evolution) minimizes the log-likelihood function based on VIX and model-implied VIX.
The final estimated parameters are used to compute and plot the model-implied VIX against the actual VIX data. Finally, it evaluates key statistics, such as long-run variance and gamma.
It is noted that for the creation of the code the "VIX-Only approach" found in Wang (2016) was used.

The second part of the code calculates the price of VIX futures using an iterative GARCH-based model. It defines functions H_iterative and C_iterative to compute key model terms, and the f_iterative and integrand functions to handle the integration required for pricing. The vix_futures_price function integrates these elements to estimate VIX futures prices based on given parameters and VIX levels. Parameters are then applied to compute an example futures price, which is printed.

The last part, "VIX FUTURES CURVE", calculates VIX futures prices based on the Heston-Nandi GARCH model using the model's parameters. It defines the functions for iterative calculations of  H  and  C , followed by the VIX futures price calculation via numerical integration. VIX data is fetched from Yahoo Finance, and futures prices are computed for each date using the defined parameters. The results are then plotted to compare the actual VIX with the calculated VIX futures prices over time. Finally, the plot displays these two data series on the same graph for visualization. One should have an external source with VIX futures prices. 



