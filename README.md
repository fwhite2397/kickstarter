# Kickstarting with Excel

## Overview of Project
We are provided our customer, Louise, analysis that will help her determine the likelyhood of success for her play.
She now seeks additional information on how different campaigns fared in relation to their launch dates and funding goals.
This project is to provide Louise the information that she requested.

### Purpose
Provide charts and data of different campaigns successfullness based upon their launch dates and funding goals.
These reports should provide guidance to Louise on the likelihood of her play being a success.

## Analysis and Challenges
Using the data in the KickStarter worksheet, of the KickStarter_Challenge workbook, I filtered the data for only look at play, to gather information on similar projects.
<img width="1291" alt="2021-12-17 (1)" src="https://user-images.githubusercontent.com/95976771/146601690-4f5b66bc-6f19-4d5c-8b81-a70254593353.png">

### Analysis of Outcomes Based on Launch Date
Since customer wanted to see the results by year, we needed to derive the year from the "DateCreatedConversion" column and record the results in a new column called Year. 
To obtain the year, we used the Year() function on the data in "DateCreatedConversion" column and saved the results in the corresponding row in the "Year" column. 
ex. =YEAR(T598)
Once the KickStarter spreadsheet had the data we needed, we used it to create a pivot table, showing the number of outcomes by month for a theater projects, overall years.
We then created a line graph detailing the results of the pivot table, to display the results in an easier to read format. 
<img width="1291" alt="2021-12-17 (2)" src="https://user-images.githubusercontent.com/95976771/146602693-4fe99288-31cb-4590-8f6d-72d5399f7e82.png">


### Analysis of Outcomes Based on Goals
We wanted to show the customer, the percentages of outcomes based upon funding goal amount of only projects associated to the "plays" category.
This was accomplished by creating a new spreadsheet and using the countifs() and data from the KickStarter spreadsheet, to calculate the number of outcomes for each goal range. 
ex. =COUNTIFS(KickStarter!$F:$F, "successful", KickStarter!$D:$D, ">=30000", KickStarter!$D:$D, "<= 34999", KickStarter!$R:$R, "plays")
Then summing the outcomes for each range to the total number of projects. 
ex. =SUM(B4:D4)
Lastly, calculating the percentage of each outcome, per range:
ex. =IFERROR(ROUND(B4/E4,2),0)
Finally, generated a line graph detailing the result of the percentages for th ranges, so the customer can clearly see the outsomes
<img width="1291" alt="2021-12-17 (4)" src="https://user-images.githubusercontent.com/95976771/146607520-4fc6a942-2bce-4c9f-a22e-a3d4b581f8d6.png">


### Challenges and Difficulties Encountered
Encountered challenges generating the pivot table for Outcomes Based on Launch Date. This was challenging in understanding the column/row set up needed to produce the correct pivot table layout and how the set up needs to be done. After more practive, it will get clearer on how to set up a pivot table faster.
Encountered difficulties generating the Outcomes Based on Goals using the CountIfs() function. This was all manually intensive writing the function for all the ranges and wish I could have done it programmatically. I incorrectly formatted several cells and had to triple check the coding in each cell to ensure that it was performing the appropriate action to display the correct results.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?
