# Kickstarter-Analysis
Analysis on Kickstarter data to uncover trends

Analysis of Outcomes Based on Goals 
See associated PNG in the resource folder for Graph Charts. 

Outcomes Based on Goals was populated by using the COUNTIFS function to pull 'successful', 'failed', and 'canceled' plays within predefined goal counts.  Counts were segregated into specific goal ranges.   Under the headings ‘successful’, ‘failed’, and ‘canceled’,  total values were identified within each specific goal range group.  For example the formula below counts each instance from Kickstarter (column D) where the goal was between 1000 and 4999  AND the campaign (plays) was successful (Column R)
 =COUNTIFS(Kickstarter!$D:$D,">=1000",Kickstarter!$F:$F,"successful",Kickstarter!$R:$R, "plays",Kickstarter!$D:$D,"<=4999")
 
This information was then used to sum up totals for each header as well as provide the percentage successful, percentage failed, and percentage canceled.  The data shows that goals set at 1000 or less had the highest successful percentage and lowest percentage failed.  The number of total projects however is second to goals set between the range of 1000 to 4999.  This category has the 2nd highest successful percentage and 2nd lowest percentage failed for the group.  Total projects for this category were 534.  Higher dollar value goals coupled with low project counts were shown to be less successful than other categories.  For goals between 45000 and 49999, there were no projects completed successfully and one project in total.  Based on the data pulled we can also say that there were no cancellations for campaigns for plays.  

**Challenges**
Issues filling in the code in an “efficient manner” was unsuccessful at first.  You could  not simply just use the fill function to populate  in the information once you scripted the first formula. There were several typos due to manually trying to fill in the data.  Eventually I copy and pasted within the headers and adjusted the data for the goals range.  

**Analysis of Theater Outcomes Based on Launch Date**
See associated PNG in the resource folder for Graph Charts. 
Theater Outcomes Based on Launch Date inserted a pivot table in from the Kickstarter data.  The data was filtered using Parent Categories and Years.  Outcomes were placed in the Columns field and under Values and the variable for rows were divided by months.  Once the chart was generated, the Parent Category was filtered to ‘theater’.  A line graph was populated to represent the data as well.

Based on the data we can say that the most theater campaigns were running through the months of May to July.  166 campaigns were running in May, 153 campaigns were running in June, and 138 theater campaigns were running in July.  However, campaigns ran between May and July had the highest number of failed campaigns but still maintained the highest percentage of successful campaigns over other months.  The month of December shows to have the fewest campaigns AND the highest failure percentage with 75 completed projects, 37 successful projects, 35 failed projects, and 3 canceled projects.  We can say that theater campaigns are the most successful in May and June months.  

**Challenges**
Filtering the row labels down to individual months proved to be a bit difficult as well as filtering the Parent Category to ‘theater’.  In my mind I didn’t think that you could used a variable more than once. (I have no idea where this came from). I kept moving the ‘outcomes’ variable around  in the pivot table fields but I wouldn’t use it twice.  

**What are two conclusions you can draw about the Theater Outcomes by Launch Date?**
Two conclusions drawn is that the top three months for total theater projects AND most successful theater projects were completed in the months of May, June, July, and August.  The least successful month is in December. 

**What can you conclude about the Outcomes based on Goals?**
Based on the data populated, goals within the range of 0 to 999 and 1000 to 4999, and 5000 to 9999 were shown to be the most active than other goal categories.  Goal categories between 0 and 4999 were also shown the have the highest percentage successful and lowest percentage failed despite having the top two highest total projects completed. 

**What are some limitations of this dataset?**
The dataset only provides a summary total for each goal set.  You are not able to see any additional information about the types of projects, number of backers, or when the projects were completed.  We know from the ‘Theater Outcomes by Launch Date’ dataset that the most successful months were between May and July.  This information is not available within the Outcomes Based on Goals dataset.  

**What are some other possible tables and/or graphs that we could create?**
For the dataset ‘Outcomes Based on Goals’  categories, 35000 to 40000, and 40000 to 45000 have a ‘Percentage Successful’ rate of 67 percent.  These two goal categories appear to be outliers as the total number of projects completed for the year were 6 and 3.  Seeing the total number of backers could explain these numbers and provide a clearer picture. 
