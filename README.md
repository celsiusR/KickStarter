# Kickstarting with Excel

## Overview of Project
The project requires the analysis of a data set that contains information related to the outcomes of running a campaign across many countries. Time periods, Locations, Outcomes, Goals and pledges are some of the data points that are included in the dataset.

The analysis is contained within Kickstarter_Challenge.xlsx
Two images of graphs the are derived from the anlysis are:
1. Outcomes_vs_Goals.PNG in the Resources folder. This one corressponds to - TAB - Outcomes based on Goals
2. Theater_Outcomes_vs_Launch.png (corressponds to 
TAB - Theater Outcomes by Launch Date) using the Parent Category filter = "Theater"

### Purpose
Analyze the outcomes of the various campaigns run.
This data set provides satistics on the outcomes of campaigns run. Campaigns consist of different categories including "film & Video", television, theater etc.. as documented in column N of the Kickstarter_challenge.xlsx spreadsheet (Sheet1).  Fine grained data is avaiable to slice and dice the campaign. It provides the user the ability to for analyze the success (or failure) of a campaign. The spreedshet tabs  - Theater Outcomes by Launch Date contain a pivot table that summarizes outcomes of success, failure and cancelations by launch monts. There is a filter that can further fine grain data to show per year and per category. A pull-down of the Parent Caetgory will depict the values and details of the campaign.

## Analysis and Challenges

The Analysis provides data for the user to determine Outcomes 
for a campaign on a launch date. It provides statistics on the success or failure of the campaign based on the amount of funds received versus the goal set for that campaign. 
From a campaign design perspective the categories are too diverse to be in one data sheet. One can ask the question as to - What is the correlation between music and photography as an example. Are these two categories appropriate to be in the same setting. 

### Analysis of Outcomes Based on Launch Date
Outcomes based on launch date are easily derived with the corelation between outcome values (successful, canceled, or failed). A fine grained analysis is made possible by including the month of the year that the campaign was launched. A pivot table has been created for this purpose in Tab "Theater Outcomes by Launch Date". One can dig deeper using filters for the year and the category of the campaign"

### Analysis of Outcomes Based on Goals)

TAB - "Outcomes based on Goals" provides a view in determining the number and percentage of outcomes based on the pledge amount v/s the goal. It provides opportunities for that ardent marketeer to provide feedback upstream to enhance the marketing effort as well as outreach activities.

### Challenges and Difficulties Encountered

These centered around the understanding and implementation of technical artifacts in excel such as pivot tables, vlookup formulas. The date fields in columns "I" and "J" are in unix timestamp formats. So there was a little googling and experimenting involved in order to derive the "YEAR" and "MONTH" values. There was a little deliberation is working the COUNTIFS statement. I encountered one missing data point; namely why is 50,000 not included in the categories for analysis. It states > 50,000. Writing the values across the cells in the Outcomes based on goals was tedious, and I went with a drag the formula cross the cells. However after stumbling a bit realized I had to anchor "&" the coordinate pair. It worked out well. The shortcut F4 was a good ally in this regard.
I think these are easily surmountable through a theretical remebering of the formulas. Not 'Rocket Science'.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

1. Campaigns have a higher success rate in the month of May.See tab - "Theater Outcomes by Launch Date". Even if one removes the filter to use "All" the success rate is high. Probably symptomatic of the onset of Spring.

2. In the months of December for all years the success rate is low.


- What can you conclude about the Outcomes based on Goals?

Firstly, from the range requirements provided in the excercise for example, "1000 to 5000", it is not not clear where the boundary numbers are to be inlcuded. I have prepared the sheet using ">=" and "<=" where applicable so boundary elements are included in the formualtion. Based on my formulas and the chart rendering the following can be observed:

1. Overall success of the combined campaigns is highest at below the goal of 1000. Failure at this point is 20%. Possibly implying that the campaigns should have lower goals.

2. Campaign success and failure rates kind of even out between 15,000 and 40,000. There is a spread of about 10 percentage points.

3. From 45000 to greater than 50,000 the rate of failure rises and  corresspondingly the rate of success drops.



- What are some limitations of this dataset?

1. From the outcomes based on goals derivation it is difficult to tell the genre of campaigns. So one cannot figure out if the music category failed or had less appeal as opposed to the other categories - Theater, Food etc... So we do not know if the census group were foodies or artsies (:-))
2. This data set should provide informtion to analyze the Outcomes during a time period. This could provide more focus on the time of the year for outreach.

3. From the big data set (Sheet1), there is no segmentation of the sexes or perhaps with age. These are important considerations in developing an effective campaign and targeting potential advocates.

4. From the big data set (Sheet1), there is not cultural information. Since these are socially relevant statistics, the ethnicity of the census group should be provided.

- What are some other possible tables and/or graphs that we could create?

1. For one, we could correlate the outcomes based on Category v/s Outcome in a graph
From this graph, we could infer the popular genre where people are inclinde to pledge morefreely.

2. Snother possible table graph could be Category v/s geography (Column G, Tab - Sheet1) 
