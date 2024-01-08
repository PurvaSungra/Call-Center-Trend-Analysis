# Call-Center-Trend-Analysis

![image](https://github.com/PurvaSungra/Call-Center-Trend-Analysis/assets/149881341/8f4e6c44-19ea-48b1-95b7-868f90c1f038)


Link- https://app.powerbi.com/view?r=eyJrIjoiZGFmZTJlZDEtMDYzNC00NjUwLWEwYTctYjgyMTU4ZGIzYzJlIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9

Background


To make sure a company always does well, it's important to regularly look at how it's been doing over time. This analysis helps find any problems, figure out how things are going, and come up with plans to fix any issues. This way, the company can work towards reaching its goals.

This analysis was done to find trends and insights using some visuals and understand the performance of this particular “Call Centre” for the first quarter of the year using some key performance indicators (KPI’s).

Data Collection

I’m currently undergoing a virtual internship by PwC Switzerland and this particular data was provided by the company to enable me take the second task of the internship.

Data Preparation

I had a glance of the dataset using excel and I was able to find out that the data consists of 10 columns and 5001 rows with the column names as Call Id, Agent, Date, Time, Topic, Answered (Y/N), Resolved, Speed of answer in seconds, AvgTalkDuration and Satisfaction rating.

![image](https://github.com/PurvaSungra/Call-Center-Trend-Analysis/assets/149881341/bab181e4-7a28-495a-886c-2d6eaf4fa982)

After taking a glance at the dataset, I moved to Power BI and connected to the dataset then did some cleaning and processing in the power query editor such as:

1. I filled in the null values in some columns with zeros. I picked zero because there were no clear patterns or feedback from stakeholders about why those values were empty. For the "AvgTalkDuration" column, I couldn't use zero because it only accepts time values, not regular numbers.
2.I made it simpler for people to understand by replacing "N" and "Y" in "Answered (Y/N)" and "Resolved" with "No" and "Yes" respectively.
3. I renamed the column from "AvgTalkDuration" to "Avg. Talk Duration." Originally, it had both time and date, but I changed it to only show the time. This is because it's about how long something lasted on a specific day.
4. Similar to the Avg. Talk Duration column, the time column also had both time and date information. I simplified it by changing the data type to show only the time.


Once I finished cleaning and organizing the data, it looked much better and was easier to work with.

After finishing up with the Power Query Editor, I started making some calculations using special functions called DAX functions. These calculations were important because they helped me create the Key Performance Indicators (KPIs) that were needed for the task. Some of the calculations I made are called measures.

 1. Positive Satisfaction Rating which were all ratings from 4 to 5.




![image](https://github.com/PurvaSungra/Call-Center-Trend-Analysis/assets/149881341/724bbc44-0c7c-4d10-9183-7e51ce156a25)


2. Count of Satisfaction Rating which was done in order to individually count all the satisfaction ratings that were provided.


![image](https://github.com/PurvaSungra/Call-Center-Trend-Analysis/assets/149881341/79d35150-9e18-4fb1-9be9-9ee03ce2664f)


3. Overall Customer Satisfaction whose formula is stated below:

 
![image](https://github.com/PurvaSungra/Call-Center-Trend-Analysis/assets/149881341/0eed0545-0ddf-4832-beb0-5acbf33afbce)

Haven known the way this calculation is usually done, I replicated same in Power BI by using the Positive Satisfaction Rating and Count of Satisfaction Rating measures that were already created.
After creating the measure, I converted to percentage by just clicking on the percentage symbol in the formatting section.

4. Total Calls answered which was created using the Answered (Y/N) column in order to view the total amount of calls that were answered.

   
![image](https://github.com/PurvaSungra/Call-Center-Trend-Analysis/assets/149881341/eb541486-e9bf-462d-9469-b1dd34330eb4)


5. Total Calls Unanswered which was also created using the Answered (Y/N) column to view the total amount of calls that were unanswered.

 
![image](https://github.com/PurvaSungra/Call-Center-Trend-Analysis/assets/149881341/03818201-e4c3-4b3b-aa85-ed2b4c1aaab0)


6. Haven known the total answered and unanswered calls, I went ahead to create the total number of calls measures by just adding up total answered and unanswered calls together.

   
![image](https://github.com/PurvaSungra/Call-Center-Trend-Analysis/assets/149881341/ac3533ee-dd24-48ea-a755-e2e7201f9f5e)


7. I have created the day Column and my providing one example like (Friday) the column will automatically take the data for the rest of the rows.

   
![image](https://github.com/PurvaSungra/Call-Center-Trend-Analysis/assets/149881341/663bdedf-5572-4844-aefc-f89b32d87bb5)



![image](https://github.com/PurvaSungra/Call-Center-Trend-Analysis/assets/149881341/8ffda54c-7a9b-424f-aa5b-e039da48248f)





Data Visualization/Analysis


When performing a visualization task, you must build a dashboard that meets the needs of the stakeholders and the goals they want to achieve from the dashboard, but with your experience added in.

The dashboard’s structure included certain cards to display some of the measures (Key Performance Indicators) that were created, as well as slicers to filter the charts to be displayed.
![image](https://github.com/PurvaSungra/Call-Center-Trend-Analysis/assets/149881341/d3bdc8ac-2900-462e-8902-ed3405b2e487)





The dashboard structure was set, thereafter analysis using visuals were done to make sense of the data at hand.

For the sake of this analysis, four visuals were made to understand some trends in the Call Centre and some of the visuals created were:

1) Stacked Bar Chart to show the Total Satisfaction Rating for each Agent which can be further filtered using the slicers available on the dashboard and from the visual, Jim has the highest rating whichever number it is between 1 & 5. Also, this visual was formatted to show some color variation on the bars from the highest value to the lowest.


![image](https://github.com/PurvaSungra/Call-Center-Trend-Analysis/assets/149881341/b036e20b-85b1-47b0-bb25-fb91e78c9669)
Stacked Bar Chart

2)Line Chart to give an insight as to which Agent has the Total Speed of answer. This chart shows the total speed of agent in responding to calls and it’s obvious that Stewart who had the least satisfaction rate because he was slow in response to calls.


![image](https://github.com/PurvaSungra/Call-Center-Trend-Analysis/assets/149881341/e3f37466-ab7c-4fa8-b35a-e29253113df6)
Line Chart

3) Pie Chart to show the Total Number of Calls based on the Topic. This chart clearly shows that people had more issues with streaming hence making it have the highest number of calls.


![image](https://github.com/PurvaSungra/Call-Center-Trend-Analysis/assets/149881341/6e7497d2-cf83-4d6a-9021-50a0e5aab4b7)
Pie Chart

4) Matrix Chart to show each agent’s Performance Quadrant. This chart is just to show how much work each agent has done i.e. their individual performance.


![image](https://github.com/PurvaSungra/Call-Center-Trend-Analysis/assets/149881341/7f9145d6-f274-4e53-99a1-b8f9c7ba6ce5)
Matrix Chart

Conclusion

All the visuals created sum up to a dashboard to further draw more insights and a full picture of the dashboard created is shown below.
![image](https://github.com/PurvaSungra/Call-Center-Trend-Analysis/assets/149881341/a374e93e-3948-4709-8ef1-9dcf28032617)



Call Centre Dashboard

Note: All the analysis was done with Power BI.
We can also connect through http://www.linkedin.com/in/purvasungra

All Formulas

positive satisfaction rating = CALCULATE(COUNT('Sheet1'[Satisfaction rating]), FILTER('Sheet1','Sheet1'[Satisfaction rating] IN {4,5}))

Satisfaction rating' = COUNT('Sheet1'[Satisfaction rating])

Overall Customer Satisfaction = DIVIDE([positive satisfaction rating],[Satisfaction rating'],0)

Calls answered = COUNTX(FILTER('Sheet1','Sheet1'[Answered (Y/N)]="Yes"),'Sheet1'[Answered (Y/N)])

Calls Unanswered = COUNTX(FILTER('Sheet1','Sheet1'[Answered (Y/N)]="No"),'Sheet1'[Answered (Y/N)])

Total Calls = CALCULATE('Sheet1'[Calls answered]+'Sheet1'[Calls Unanswered])

Resolved Calls = COUNTX(FILTER('Sheet1','Sheet1'[Resolved]="yes"),'Sheet1'[Resolved])

Unresolved Calls = COUNTX(FILTER('Sheet1','Sheet1'[Resolved]="No"),'Sheet1'[Resolved])

average td = AVERAGE(Sheet1[AvgTalkDuration.time])


