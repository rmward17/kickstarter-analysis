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


