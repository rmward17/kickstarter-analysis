# An Analysis of Kicksarter Campaigns
Performing analysis on Kickstarter data to uncover trends in order to aid Louise in determining the best way to get her US play campain funded.

## Analysis of the Data
To begin the analysis, I performed the following actions to make the data easier to read:

* Color coded the "outomes" column to quickly visualize the results of each campaign
* Created the "Percentage Funded" category to create a metric to measure the relationship between the goal money amount and pledged money amount
* Created an "Average Donations" column to see how much money, on average, backers were donating to each campagin
* Separated the subcategories from the parent categories to make the data easier to read
* Converted the dates to be readable for analysis

Next, I analyzed the outcomes of all of the theater campaigns in the United States. In the stacked bar chart below, you can see that there are 525 successful campaigns, 349 failed campaigns, 26 canceled campaigns, and 12 live campaigns.

![Parent_Categories_Outcome](https://github.com/rmward17/kickstarter-analysis/blob/main/Parent_Categories_Outcome.jpg?raw=true)

Knowing this, I wanted to take a deeper look at these campaigns. Since the chart above shows the parent categories, I wanted to see what the outcomes of the subcategories were. In the stacked bar chart below, you can see that the "plays" subcategory has the most campaigns in the US. Of those 671 campaigns, 250 have failed and 412 have been successful.

![Subcategory_Outcomes](https://github.com/rmward17/kickstarter-analysis/blob/main/Subcategory_Outcomes.jpg?raw=true)

Now knowing some basic details of the theater and play campaigns,next I used the data to determine aspects of a successful campaign. A possible factor in campaign success is the launch date. Based on the line chart below, you can see that the highest number of successful campaigns were launched in May. After that, the number of successful campaigns decreases in each subsequent month with a slight uptick in October. 

![Outcomes_Based_on_Launch_Date](https://github.com/rmward17/kickstarter-analysis/blob/main/Outcomes_Based_on_Launch_Date.jpg?raw=true)

Another important aspect of the campaign is the goal amount of money and the amount of money pledged. In the US, the successful campaigns in this dataset have a mean of $5,049 and the failed campaigns have a mean goal of $10,554. Meanwhile, the successful campaigns have a mean amount pledged of $5,062 while the failed campaigns have a mean amount pledged of $559. This shows us that the failed campaigns, on average, asked for double the amount of money than the successful campaigns and getting a much smaller amount donated than the successful campaigns. The median for the goal and pledged amounts of the successful campagins are $3,000 and $3,168, respectfully, while the medians for the failed campagins goal and pladged amounts are $5,000 and $103. This further supports the idea that the failed campaigns are asking for too much money which may deter backers from donating to them, resulting in very low pledged amounts.

After finding those statistics, I dug in a little deeper to see what more I could find out about these campaigns. I did so by calculating the Upper Quartile, Lower Quartile, and IQR of the goal and pledged amounts of the successful and failed campaigns. The Upper and Lower Quartiles provide a range of the middle 50% of the data and are key in determining the Inter Quartile Range, IQR for short. The IQR provides the range of the middle 50% of the data and can be used to help determine outliers. The Upper Quartile, Q3, for the successful campaigns' goal amount is $5,000 and the Lower Quartile, Q1, is $1,500. That range can help you determine how much to set you capagin goal to given that the successful pledged amount has a Q3 of $5,602 and a Q1 of $1,717. Those values being so close makes sense given that they are the successful campaigns. Doing the same for the failed campaigns, the goal amounts have a Q3 of $10,000 and a Q1 of $2,000. The failed campaigns' pledged amounts have a Q3 of $501 and a Q1 of $9. The stark difference in those Quartiles warns that when setting a goal, you must think realistically about what potential backers are willing to donate. I know that you are also thinking about a future campaign for a play in the United Kingdom so I created a couple of Box-and-Whisker plots to help visualize the goal and pledged amounts' Quartiles, maxes, mins, and outliers of the UK play campagins to set expecations and provide insight on how much you should be asking for in that campaign as well. 

![UK_Play_BW](https://github.com/rmward17/kickstarter-analysis/blob/main/UK_Play_BW.jpg?raw=true)

## Findings and Reccomendations

Based on this dataset, I have determined some key aspects of the successful and failed play campagins in the US. In general, plays are the most popular type of campagin on Kickstarter which means there are a lot of other campaigns to compete with. The successful campaigns seemed to ask for around $5,000 and launch at the end of Spring. In order to be as successful as possible, I would reccomend asking for an amount around the average goal of successful campaigns and launching the campaign in May. For your future UK play, I reccomend having a lower than average goal because the highest amount pledged is lower than the average goal. The Box-and-Whisker plot shows that 25% of the UK play campaigns weren't funded at all. Just some things to keep in mind for the future. 

Good Luck, I can't wait to see the play!


# Kickstarting with Excel

## Overview of Project

### Purpose

The purpose of this analysis is to compare the outcomes of play campaigns to the campaign launch date to give Louise an idea of how her campaign for "Fever" may go.
This is a continuation of an analysis of Kickstarter data to provide Louise guidance on starting the campaign. Luckily, she got close to her fundraising goal quickly so naturally, she is curious about what that could indicate for the outcome of the campaign.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

Since the goal of this analysis is to determine what the possible outcome of Louise's play will be, I used pivot tables and charts to visualize the outcomes of all theater campaigns based on launch date. The table below shows that the highest number of successful play campaigns launched in May. However, May also has the highest number of failed campaigns. That doesn't mean that May is the worst month to launch a play, we have to consider that May has the higest number of campaign launches for plays so we have to keep in mind the relationship between these numbers.

![Theater_Outcomes_vs_Launch2](https://github.com/rmward17/kickstarter-analysis/blob/main/Theater_Outcomes_vs_Launch2.jpg?raw=true)

### Analysis of Outcomes Based on Goals

In order to get a better understanding of the play campaign outcomes, I created a table that has the number of successful, failed, and canceled play campaigns
by goal amount ranges. The table also includes the percentages of successful, failed, and canceled campaigns for each goal range. I was able to use a COUNTIFS() function in excel that allowed me to filter data within each cell to enure I was getting the correct infromation. For example, this is the function for the cell showing the number of successful play campagins that had a goal amount between $1,000 and $4,999:

=COUNTIFS(Kickstarter!$F:$F,"successful", Kickstarter!$D:$D, ">=1000",Kickstarter!$D:$D, "<=4999",Kickstarter!$R:$R,"plays")

I was able to filter on the outcomes, goals, and subcategories. I was able to filter on the goal column twice to ensure I had both bounds of the goal range for this section of the table. 

![Outcome_vs_Goal_Chart](https://github.com/rmward17/kickstarter-analysis/blob/main/Outcome_vs_Goal_Chart.jpg?raw=true)

Using this table, I was able to create the table below that shows the outcome percentages based on goal range. You can see that none of the play campaigns were canceled and the higher the goal amount, the less likely it was to be successful. Just looking at the line chart, you would think that something odd is happening in the $35,000 to $39,999 and $40,000 to $44,999 range however, looking at the table, there are only 6 campaigns in the $35,000 to $39,999 range and 3 campaigns in the $40,000 to $44,999 range so there aren't very many projects in that fudning level in the first place. Each visualization is good on it's own but with both, you can get the whole story of what is going on.

![Outcomes_vs_Goals2](https://github.com/rmward17/kickstarter-analysis/blob/main/Outcomes_vs_Goals2.jpg?raw=true)

### Challenges and Difficulties Encountered

Luckily, I didn't enouncter many challenges in creating the charts to show exactly what we wanted. However, the percentage table was a little difficult to create because we needed a long bit of code to produce the correct counts in each cell. Other potential challenges could have come from simple, easy to make mistakes such as selecting the pledged amount column instead of the goal amount column and filtering for "theater" on the categories  rather than "plays" pn the subcategories.

## Results

This analysis provides a lot of insight on the success of campaigns based on launch date and goal amount. From the outcomes based on launch date, we can conclude that the most ideal time to launch a campaign is May or June as those have the highest amounts of successful campaigns. We can also conclude that the worst time to launch is October and December. It is possible that with the nicer weather Spring brings, people are spending more time going out for activites rather than staying in during the cooler months of Fall and Winter.

From the outcomes based on goals table and line chart, we can conclude that the lower the goal amount, the higher chance the campaign has on being successful. One thing to note is that at the $15,000 - $19,999 range, the successful and failed outcomes are at 50% each. If the goal amount is equal to or below that range, you have a higher chance of having a succesful campagin than a failed one.

Some limitations of this data set are the years. This data set only goes up to 2017 so there's about 5 more years of data we could be using to refine these results. There are also other fundraising sites. If we had data from those other sites as well, we could do a comparison of the outcomes based on site to see if Kickstarter is the best place for your campaign. However, there are a lot of things we can still do with this dataset. A table that considers the percentage of successful and fialed campagins based on launch date would be very helpful and tell a better story than the counts we have at the moment. A table with the outcomes based on duration of the campapign could help determine the optimal length for your campaign. Another table that would be helpful is one that shows the goal amounts of successful play campagins by average donations and/or number of backers to know how much you need to share the campagin in order to be most succesfful. If the average donation amount is low for most successful campagins, then that most likely correlates to a higher number of backers which means you would need to share the campagin in as many places as possible. 
