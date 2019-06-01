# Ford GoBike User Analysis
## by Elizabeth Blank


## Dataset

The data here contains 1,863,721 survey responses regarding 16 trip attributes. Variables of interest include member gender (categorical), start time (object), member birth year (integer), user type (member or customer, categorical), and Bike Share for All membership status (categorical). The initial 1,863,721 observations was cut down to 1,670,060 after cleaning.

This dataset and its feature documentation can be found at https://www.fordgobike.com/system-data. 

A post from stack overflow that helped me to learn how to search through subfolders so I could iterate over the many individual files: https://stackoverflow.com/questions/2186525/how-to-use-glob-to-find-files-recursively.


## Summary of Findings

During my exploration I found that high ride frequency was largely characterized by four variables: membership status, time of day (hour), gender, and day of the week. My variables of interest were membership status, day of the week, and age. It turned out that membership status was a clear indicator of frequent riders. Members accounted for almost 90% of rides and were riding with way more consistency than regular customers. Day of the week was also a big factor in ride frequency. We saw ride rates decrease some on weekends, yet they stayed high, consistently, on weekdays. The age variable was highly skewed to the right, but once plotted on a log scale it looked fairly normal. What I learned from age was that it had little variability-- over 75% of users fell between 18 and 40. This variable did not vary much across genders, hour of the day, or membership status, thus age, in the context I examined it, did not seem to carry much weight in terms of predicting ride frequency.

As for variables that weren't of primary interest, I found that gender was a huge factor in ride frequency. Men are three times more likely than women to subscribe and to ride. Hour of day was another variable I didn't expect to have such an impact on ride frequency. It turns out that our most frequent riders follow a clear pattern-- they ride on weekdays around 8am and 5pm. We can expect to see significant drops before, after, and between those hours. Lastly, the month variable. This should have been a no-brainer. Both subscribers and customers alike are most likely to ride during the warmest months (~April-September). This variable's effect was less pronounced among subscribers, but still evident. Lastly, I found an interesting relationship between bike share for all membership status and gender. This relationship didn't matter much in terms of identifying ride frequency, but since it was intriguing, I put it in the presentation. It showed that those who identify as "other" are about 40% more likely to participate in the Bike Share for All program than either other gender. I thought it should be mentioned since recent studies have shown those with non-conventional gender types are more likely to face wage discrimination, and have much more trouble finding jobs in general. This graph seems to do a good job of depicting their marginalized status, and considering our current climate, it seems very relevant.



## Key Insights for Presentation

In my presentation I focus mostly on the four variables mentioned above: membership status, time of day, gender, and day of the week. 
I first examined the user type variable, then hour, followed by gender. These variables' respective effects on ride frequency were most obvious when plotted alone. Next, I examined some other variables in pairs, specifically: daily distribution by user type and bike share for all membership across genders. I found the clearest way to present these was through count plots. Last, I looked at the effect of user type on hourly and daily usage, and finally bike share membership on hourly and daily usage. These interactions were best delineated with heat maps.








