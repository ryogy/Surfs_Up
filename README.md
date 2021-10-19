# Surfs Up

## Overview of Statistical Analysis
The purpose of this analysis was to look at all the temperature data on Oahu, Hawaii for the months of June and December.  This is to identify what the key differences are between summer and winter in Hawaii.  With this information the client will be able to better predict seasonal sales trends and determine if the business will be profitable year round.

## Results
* The main difference between the datasets for the months of June and December is that the sample size for June is much larger.  The sample count for June being 19,550 and the count for December being 1,517.  This means that the data for June is much more accurate than December.

*  The standard deviation for June is 4.5 with December being only 3.7.  This means that the temperature in December is more 'stable' than in June because the temperature tends to stay closer to the mean.  Even with that being said the average temperatures for December and June are 71 and 73, so it is safe to say that Hawaii has beautiful weather year round.

*  The Lower Quartiles for both datasets are only 1 degree apart, 69 and 70.  With this information we know that even under the worst temperature circumstances for each month, the temperatures are still very warm, definitely warm enough to operate a surf and ice cream shop.

## Summary
The main flaw within the data is the difference in sample sizes between June and December.  It is widely known that Hawaii has very favorable and warm temeratures year round but this discrepancy in sample size gives just enough quantitative doubt to possibly rethink that.  Looking forward to future analysis more data must be collected from other stations to rectify this difference in collection data.

For additional queries...
###### Query #1
annual_2017 = session.query(Measurement.tobs).\
filter(extract('year', Measurement.date)==2017).all()
annual_data.describe()

###### Query #2
precipitation_2017 = session.query(Measurement.date, Measurement.prcp).\
filter(extract('month' , Measurement.date)==6).all()
precipitation_2017.describe()

Both of these querys are just basic examples, but since the above analysis shows an almost nonexistant seasonal temperature difference.  Looking into possible fluctuations in annual termperatures due to larger scale environmental factors.  The other major source of Data that was overlooked in this general analysis was precipitation data.  A rainy year can ruin sales in the outdoor industry just as significantly as temperatures.  Looking into seasonal precipitation rates would be another great way to see if the business will be profitable year round.

Lastly, WAVE DATA!  There must be some analysis into seasonal fluctuations around swells otherwise the above analysis is completely useless.


