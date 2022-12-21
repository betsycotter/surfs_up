# Surf’s Up Analysis

## Overview

W. Avy, my investor, and I would like to build a Surf and Shake shop in Hawaii. This shop will serve ice cream and rent surfboards to locals and tourists. W. Avy is a savvy investor and would like to run some analysis before we commit to the idea. W. Avy is most concerned with the weather data in the locations we are researching. We have been asked to run the analytics on the weather data that has been collected in previous years, particularly for June and December. 

## Results

We have been given the [hawaii.sqlite](hawaii.sqlite) database and through our analysis, we have found the following: 
- The average temperature in June is 74.94 degrees, while the average temperature in December is 71.04 degrees. 
- The minimum temperature in June is 64 degrees, while the minimum temperature in December is 56 degrees. 
- The maximum temperature in June is 85 degrees, while the maximum temperature in December is 83 degrees. 

See full details below: 

June Data Summary: 

<img width="142" alt="June_Temps" src="https://user-images.githubusercontent.com/116031639/208977173-6ad97ece-584f-432a-ae54-62f6a9735df9.png">

December Data Summary: 

<img width="172" alt="December_Temps" src="https://user-images.githubusercontent.com/116031639/208977198-c903ffc7-6477-4165-9573-ae0734d3aeef.png">

## Summary

After reviewing the June and December data, we notice that the temperatures vary over the course of the year, however, the fluctuations are not very significant. It would be helpful to run the precipitation data for each of these months to see the seasonal differences. The following queries will be helpful to obtain this data: 

June Precipitation query: 

```
june_prcp = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6)
```

December Precipitation query: 

```
dec_prcp = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 12)
```

NOTE: these queries will be added to the code after all dependencies have been added. Then, the current text: month_temps will need to be updated to month_prcp. This will allow all 4 versions of the query to run properly. 

By gathering this data, we can use it to determine business needs, such as supplies and staffing, due to seasonal changes in demand from our customers. 
