# Air-Quality-Index-Pred-AQI-
In this Project I have followed each and every step of a Data_Science lifecycle.

#### Data Collection
In Data Collection i extracted the all the data required for the AQI prediction by a website https://en.tutiempo.net/
particularly for New Delhi.

##### Variable Interpretation

* T	Average Temperature (°C)
* TM	Maximum temperature (°C)
* Tm	Minimum temperature (°C)
* SLP	Atmospheric pressure at sea level (hPa)
* H	Average relative humidity (%)
* PP	Total rainfall and / or snowmelt (mm)
* VV	Average visibility (Km)
* V	Average wind speed (Km/h)
* VM	Maximum sustained wind speed (Km/h)
* VG	Maximum speed of wind (Km/h)
* RA	Indicate if there was rain or drizzle (In the monthly average, total days it rained)
* SN	Snow indicator (In the monthly average, total days that snowed)
* TS	Indicates whether there storm (In the monthly average, Total days with thunderstorm)
* FG	Indicates whether there was fog (In the monthly average, Total days with fog)

We also need PM 2.5 value, PM 2.5 values are collected from paid API, which will act as a dependent variable and all the others as independent variables.

Executing the code in [AQI_perDay.py](https://github.com/anubhav6864/Air-Quality-Index-Pred-AQI-/blob/main/AQI_perDay.py) we get PM 2.5 per day values for each year,We get a dependent feature
Now we need to extract independent features from the Html, for thati have used Beautifulsoup to parse the Html data into a CSV file  which can be seen in [ScrapingTableAndCombining.py](https://github.com/anubhav6864/Air-Quality-Index-Pred-AQI-/blob/main/ScrapingTableAndCombining.py) file.
After doing the above i added the PM 2.5 value to the CSV files and then combined all the years data into a single CSV so that we can get our final data which is to be used in the prediction.


