# datasci-crime_analytics_visualization
## Southern District in San Francisco leads for largest number of crimes reported

I have selected San Franscisco crime data for my assignment. I used IPython to analyse the data and create charts.

I have python pandas and matplotlib.pyplot modules from python. I have used the following code to to generate the graphs below.

import pandas as pd
import matplotlib.pyplot as plt 
file_name ='/home/manoj/datasci_course_materials/assignment6/sanfrancisco_incidents_summer_2014.csv'
file_data = pd.read_csv(file_name)
districts = dict(file_data.PdDistrict.value_counts()).keys()
plt.bar(range(len(districts)), district.values())
plt.xticks(range(len(districts)), districts)
plt.title('District-wise crime rate')
plt.show()


My conlusions from the visualisations produced are:

1. Larceny/Theft is the most common crime observed in San Francisco.
![Types of Crimes Vs Counts](https://github.com/manojampolu/datasci-crime_analytics_visualization/blob/master/crimes_counts.png)

2. Southern District leads for highest number of crimes reported in San Francisco.(Not at all safe to park your vehicle outside in Southern District)
![District wise crime rate](https://github.com/manojampolu/datasci-crime_analytics_visualization/blob/master/crime_rate_on_district.png)
Out of the majority of crimes reported, Larceny/Theft is most common in any district.
![Top Crime Counts District wise](https://github.com/manojampolu/datasci-crime_analytics_visualization/blob/master/common_crmes_district.png)

3. The crimes do not follow any specific pattern based on day of a week or day of a month. 
![Crimes Rates on a day of month](https://github.com/manojampolu/datasci-crime_analytics_visualization/blob/master/crime_rate_on_day_of_month.png)
![Day of a week wise crime counts](https://github.com/manojampolu/datasci-crime_analytics_visualization/blob/master/crime_rate_day_of_week.png)
But the number of thefts reported on a Saturday seem to be higher.
![Day wise break up of common crimes](https://github.com/manojampolu/datasci-crime_analytics_visualization/blob/master/common_crmes_dayofweek.png)
But the crimes reported seems to be increasing from June to August 2014.
![Month wise break up of common crimes](https://github.com/manojampolu/datasci-crime_analytics_visualization/blob/master/month_wise_crimes_reported.png)

4. However, the number of crimes reported between 5PM - 7PM are high.
![Hourly breakup of crimes reported](https://github.com/manojampolu/datasci-crime_analytics_visualization/blob/master/crime_rate_hourly_basis.png)

5. I think the number crimes resolved in an area plays a very important role in curbing the number of crimes in an area. Low crimes are reported in areas where the crimes resolved are high in number.
![Crimes Resolved Vs not Resolved](https://github.com/manojampolu/datasci-crime_analytics_visualization/blob/master/crime_rate_vs_resoultion.png)

### Conclusion
If you are staying in San Francisco, then Southern district is not the place to be. Number of crimes reported are high between 5PM - 7 PM are high. So shop keepers or house owners or vehicle owners should better beaware about your property.
