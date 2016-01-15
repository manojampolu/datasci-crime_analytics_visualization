## Exploratory data analysis of Crime Rate in San Francisco

I have selected San Franscisco crime data for my assignment. I have used IPython to analyse the data and create charts.

A sample code used to generate the bar graphs for the analysis is below.

import pandas as pd
import matplotlib.pyplot as plt 
file_name ='/home/manoj/datasci_course_materials/assignment6/sanfrancisco_incidents_summer_2014.csv'
file_data = pd.read_csv(file_name)
districts = dict(file_data.PdDistrict.value_counts()).keys()
plt.bar(range(len(districts)), district.values())
plt.xticks(range(len(districts)), districts)
plt.title('District-wise crime rate')
plt.show()


I have produced various various charts to understand the data. An initial look at the count of crimes versus other parameters show interesting facts about the crimes.
![Count of Crimes Vs Others](https://github.com/manojampolu/datasci-crime_analytics_visualization/blob/master/pizap.com14528473348223.jpg)

1. I was thinking that no of crimes reported on a weekend would be higher than that of a weekday. But, the crimes do not follow any specific pattern based on day of a week. (graph on top left).
2. Southern District leads for highest number of crimes reported in San Francisco.(graph on top right)
3. Larceny/Theft is the most common crime observed in San Francisco.(graph on bottom left)
4. I was hoping that number of crimes reported on month end would be higher that the number reported on begining of the month. However, the number of crimes reported on day of month do not follow any specific pattern. The peaks are observed on 27th June and 9th Aug. (graph on bottom right)

However, the number of crimes reported is seen to be increasing from June to August.
![Month wise break up of common crimes](https://github.com/manojampolu/datasci-crime_analytics_visualization/blob/master/month_wise_crimes_reported.png)

#A deeper look into the data by analysing the crimes reported on specific time of a day various other factors revealed some interesting facts.

I was thinking that no of crimes reported during night would be higher compared to day time. Surprisingly, the number of crimes reported at night are less compared to day time. The intersting facts being:
![Count of Crimes Vs Others](https://github.com/manojampolu/datasci-crime_analytics_visualization/blob/master/pizap.com14528623847692.jpg)
1. Number of crimes gradually decrease from night and then increase at 12th hour(noon time), then show a slight decrease and reach maximim between 17th hour(5 PM) to 19th hour(7 PM). The same pattern is observed for crime recorded time on any day of week.
2. I think the above pattern is largely due to high number of larceny/theft crimes reported. Also, is the high number of larceny/thefts reported in Southern district. 
![Count of Crimes Vs Others](https://github.com/manojampolu/datasci-crime_analytics_visualization/blob/master/pizap.com14528624690003.jpg)
3. Crimes recroded around 4 AM could be minimum as the city sleeps during that time.
4. While southern district records maximum crimes between 5PM-7PM, the other districts like TENDERLOIN records low number of crimes. This could be due to the fact that Southern District has more offices and TENDERLOIN is housing zone.

I felt that the number of crimes resolved will play an important role in the number of crimes recorded in any district. But I am surprised to see that most of the districts display the same ratio of crimes resolved to unresolved except TENDERLOIN, MISSION and BAYVIEW. ![District wise crimes resolved Vs Unresolved](https://github.com/manojampolu/datasci-crime_analytics_visualization/blob/master/res_vs_unres_districtwise.png)
This may be because of the fact that most of the thefts/burglaries are not resolved in any district.
![Category of crimes resolved Vs Unresolved](https://github.com/manojampolu/datasci-crime_analytics_visualization/blob/master/crimes_%res_vs_%unres.png)


### Conclusion
I think the San Francisco police department and the judicial department have to come up with more innovative steps to curb theft related crimes in all districts. People should also be warned about the timings(between 12PM-1PM and 5PM-7PM) during which most of the crimes take place. If they can reduce the number of crimes during the peak hours, I feel it would show a great difference in number of crimes recorded.
