# Call-Center-Trend-Analysis




Background

For firms to always thrive, it’s critical to do analysis of it’s business performance over a period of time. What such analysis does is to basically help finding out issues if there’s any, help understand trends/performances and put up strategies to address such issues to help such firm to reach it’s goal.

This analysis was done to find trends and insights using some visuals and understand the performance of this particular “Call Centre” for the first quarter of the year using some key performance indicators (KPI’s).

Data Collection

I’m currently undergoing a virtual internship by PwC Switzerland and this particular data was provided by the company to enable me take the second task of the internship.

Data Preparation

I had a glance of the dataset using excel and I was able to find out that the data consists of 10 columns and 5001 rows with the column names as Call Id, Agent, Date, Time, Topic, Answered (Y/N), Resolved, Speed of answer in seconds, AvgTalkDuration and Satisfaction rating.


Image by author
After taking a glance at the dataset, I moved to Power BI and connected to the dataset then did some cleaning and processing in the power query editor such as:

Replacing the null values in some columns with 0. Replacing null with 0 isn’t the only way to treat null values but I chose to replace with 0 because there were no trends in those columns to say I want to follow existing trends neither do I have access to the stakeholders to give me an insights as to why those cells had null values hence, resolving to 0. I couldn’t replace the AvgTalkDuration with 0 because it can’t take any value that isn’t in the time format.

Image by author: Columns with null values

Image by author: Replacing process
2. Changed the N and Y in Answered (Y/N) and Resolved to Yes and No which people could easily relate with.


Image by author: Before Changing the texts

Image by author: After changing the text
3. The “AvgTalkDuration” column name was changed to “Avg. Talk Duration” and initially, the column consisted of both time and date but i changed the data type to only time since it was talking about duration and it was on a particular day.


Image by author

Image by author: Changing Process

Image by author: After Changing
4. Just like the Avg. Talk Duration column, the time column also consisted of both time and date so i basically changed the data type to reflect the time only.


Image by author: Before Changing Data Type

Image by author: After Changing Data Type
After doing those cleaning and processing, the data looked cleaner to work with.


Image by author: Glance of the cleaned and processed data
After closing the power query editor, I went ahead to create some measures with the aid if some DAX functions which was going to enable me create the KPI’s that were requested in the task and some of the measures created were:

Positive Satisfaction Rating which were all ratings from 4 to 5.

Image by author
2. Count of Satisfaction Rating which was done in order to individually count all the satisfaction ratings that were provided.


Image by author
3. Overall Customer Satisfaction whose formula is stated below:


Image from MonkeyLearn
Haven known the way this calculation is usually done, I replicated same in Power BI by using the Positive Satisfaction Rating and Count of Satisfaction Rating measures that were already created.


Image by author
After creating the measure, I converted to percentage by just clicking on the percentage symbol in the formatting section as seen below:


Image by author
4. Total Calls answered which was created using the Answered (Y/N) column in order to view the total amount of calls that were answered.


Image by author
5. Total Calls Unanswered which was also created using the Answered (Y/N) column to view the total amount of calls that were unanswered.


Image by author
6. Haven known the total answered and unanswered calls, I went ahead to create the total number of calls measures by just adding up total answered and unanswered calls together.


Image by author
7. I also created the weekday measure to only contain weekdays (Sunday — Saturday).


Image by author
Data Visualization/Analysis

After creating all the measures, I needed them to be together to make sure the tables contain the right set of data.


Image by author
When performing a visualization task, you must build a dashboard that meets the needs of the stakeholders and the goals they want to achieve from the dashboard, but with your experience added in.

The dashboard’s structure included certain cards to display some of the measures (Key Performance Indicators) that were created, as well as slicers to filter the charts to be displayed.


Image by author
![image](https://github.com/PurvaSungra/Call-Center-Trend-Analysis/assets/149881341/26b964f8-32a2-4fdc-9574-4978731fd4b3)

The dashboard structure was set, thereafter analysis using visuals were done to make sense of the data at hand.

For the sake of this analysis, four visuals were made to understand some trends in the Call Centre and some of the visuals created were:

Stacked Bar Chart to show the Total Satisfaction Rating for each Agent which can be further filtered using the slicers available on the dashboard and from the visual, Jim has the highest rating whichever number it is between 1 & 5. Also, this visual was formatted to show some color variation on the bars from the highest value to the lowest.

Image by author: Stacked Bar Chart
Line Chart to give an insight as to which Agent has the Total Speed of answer. This chart shows the total speed of agent in responding to calls and it’s obvious that Stewart who had the least satisfaction rate because he was slow in response to calls.

Image by author: Line Chart
Stacked Bar Chart to show the Total Number of Calls based on the Topic. This chart clearly shows that people had more issues with streaming hence making it have the highest number of calls.

Image by author
Matrix Chart to show each agent’s Performance Quadrant. This chart is just to show how much work each agent has done i.e. their individual performance.

Image by author: Matrix Chart
Conclusion

All the visuals created sum up to a dashboard to further draw more insights and a full picture of the dashboard created is shown below.


Image by author: Call Centre Dashboard
Note: All the analysis was done with Power BI.
