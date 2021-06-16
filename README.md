## citibike-challenge

### contains
- analysis.md: contains summary analysis of visualisations within a Tableau Story
- [Citibike Analysis](https://public.tableau.com/profile/sarah.dalleyhood#!/vizhome/CitiBikeAnalysis_16185073442630/citibikeanalysis?publish=yes): a Tableau Story with associated dashboards and worksheets analysing the Citibike station use dataset
- bike_preprocessing.ipynb: contains the code for preprocessing the Citibike dataset

### description

The goal of this analysis was to uncover two trends within the Citibike dataset over 2018-2021: usage by gender, to determine whether outreach to women has been successful, and identifying bikes potentially in need of servicing. To that end, charts and graphs of people using Citibike by gender and trip length and quantity were created. A graph of usage of start and end station locations was also created. 

![Bar Usage By Gender](/images/genderBreakdown.png)
![Trip Duration Horizontal Bar](/images/tripDuration.png)
![Station Location Map](/images/stationLocation.png)

### challenges

The dataset required several steps of pre-processing. First, each month's dataset was concatenated into one file, then the user year of birth column was searched for suspicious values, and all rows with birth years before 1931 were removed. Finally, the index was copied into a column to act as a unique 'trip ID' for each row in Tableau. 

![Suspicious Birth Dates](/images/suspiciousDOBedited.png)
*A review of values in the Birth Year column revealed unrealistic birth dates such as 1888.*

Another challenge was finding the percentages of users by gender. At first using a calculated field was attempted, but it proved difficult to combine the multiple columns within it. Then the 'Percentages Of' option under the Analysis tab was used, in combination with sets, to create visualisations illustrating the percentages of female usage. 

![Gender Usage Table](/images/gender%Table.png)
*The table upon which the gender usage pie charts were based, created using the 'Percentages Of' Analysis option.*

Finally, combining two latitude/longitude pairs into one map proved difficult. It was not possible to have two latitudes/longitudes as rows and columns on a map, so using a Dual Axis and the other latitude/longitude was used as Details. 

![Use of Dual Axis](/images/dualAxis.png)