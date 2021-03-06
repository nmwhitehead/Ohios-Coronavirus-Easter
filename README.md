# Ohio's COVID-19 Spread Caused by Easter Sunday


Last week I wrote a blog post looking at the effects of Easter on the spread of [Coronavirus cases caused by Easter Sunday](https://medium.com/@ins0mnicat/did-socially-distant-easter-services-prevented-a-post-easter-spike-16379e98b0b6). While I was expecting to see major spikes in new cases, I ended up finding that the country did very well, with many states like Alabama seeing major dips in new cases in the week following.

During the research for this blog post, which was done using [free data from the NYT's Github](https://github.com/nytimes/covid-19-data), I did find a few states that had the major spikes I expected. And Ohio's was bad enough that I wanted to do a little more with it.



## Ohio's Easter Spike


<img src="Images/Ohio's Easter.png">


The graph above shows the daily change in cases in the state of Ohio. The solid yellow line indicates Easter Sunday and the dashed yellow line indicated the following Sunday. The week delay is to account for the incubation period of the disease. While most [become symptomatic in 5 days](https://annals.org/aim/fullarticle/2762808/incubation-period-coronavirus-disease-2019-covid-19-from-publicly-reported), not 7, I made it a full week to account for the additional time until someone is tested and confirmed positive. The spike peaking exactly on the dotted line is purely coincidence.

Coincidence aside, the spike following Easter is clear. Prior to Easter, the daily increases in COVID-19 cases in the state was drifting at a comfortable 400ish every day, but following Easter there was a spiked peaking at around 1400 in a single day. The question I wanted to answer was how many cases were caused by Easter events. And the way I wanted to check was a simple linear regression model.



## Linear Regression Predictions


<img src='Images/Ohio Regression.png'>


This predictor expected a higher rise than the state saw in the days before and right after Easter because of the very low number in the beginning of the spread, which made it an efficient low end predictor for the number of cases that Easter was to blame for.

<img src='Images/Ohio Predictor.png'>


This regression model predicted that Easter was to blame for 2,759 cases, or about 18% of Ohio's 15,169 cases, as of April 24th.

In order to account for the more flat data in late March and early April leading up to Easter Day, I made a second regression model that didn't start it's training data until March 27th.


<img src='Images/Ohio Recent Regressor.png'>


This model, which likely predicts too low will provide a much higher prediction for how many cases Easter is to blame for.


<img src='Images/Ohio Recent Predictor.png'>


This regression model predicted that Easter was to blame for 3,396 cases, or about 22% of Ohio's 15,169 cases, as of April 24th.



# Conclusion


While it is impossible to predict the exact number of cases that were caused by Easter, the low and high estimators of 2,759 and 3,396 cases gives us a good estimation of about 3,000 cases, and a large part of the growth of total cases from 6,604 cases on Easter Sunday to 15,169 cases on April 24th, 12 days later.

This doesn't tell us much that we shouldn't already know, but it does tell us that having gatherings is a bad idea, and we should continue to listen to stay at home orders, even if some states think we're ready to open back up.