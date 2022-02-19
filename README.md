# An Analysis of Kicksarter Campaigns
Performing analysis on Kickstarter data to uncover trends in order to aid Louise in determining the best way to get her US play campain funded.

## Analysis of the Data
To being the analysis, I did the following actions to make the data easier to read:
*Color coded the "outomes" column to quickly visualize the results of each campaign
*Created the "Percentage Funded" category to determine a relationship between the "goal" column and "pledged" column
*Created an "Average Donations" column to see how much backers were donating to each campagin
*Separated the subcategories from the parent categories to make the data easier to manipulate
*Converted the dates to be readable for analysis

Next, I analyzed the outcomes of all of the theater campagins in the United States. In the stacked bar chart below, you can see that there are 525 successful campagins, 349 failed campagins, 26 canceled campaigns, and 12 live campagins

![Parent Categories Outcome](C:\Users\wardr\OneDrive\Desktop\Data Analytics Bootcamp\Analysis Projects\Crowd Funding Analysis\Parent Categories Outcome.png)

Knowing this, I wanted to take a look deeper at these camapgins. Since that chart shows the parent category, I wanted to see what each of the subcategories looked like. In the stacked bar chart below, you can see that the "plays" subcategory has the most campains in the US. Of those 671 campaigns, 250 have failed and 412 have been successful.

![Subcategory Outcomes](C:\Users\wardr\OneDrive\Desktop\Data Analytics Bootcamp\Analysis Projects\Crowd Funding Analysis\Subcategory Outcomes.png)

Now knowing some basic details of the theater and play campagins, the next step was to use the data to help you determine steps to take in order to have a successful campaign. An important thing to decide is when to launch the campaign. Based on the line chart below, you can see that the highest number of successful campagins were launched in May. After that, the number of successful campagins decreases steadily in each subsequent month with a slight uptick in October. 

![Outcomes Based on Launch Date](C:\Users\wardr\OneDrive\Desktop\Data Analytics Bootcamp\Analysis Projects\Crowd Funding Analysis\Outcomes Based on Launch Date.png)

Another important aspect to the campagin is the goal amount of money and the money pledged. In the US, the successful campaigns in this dataset have a mean of $5,049 and the failed campaigns have a mean goal of $10,554. Meanwhile, the successful campaigns have a mean amount pledged of $5,062 while the failed campaigns have a mean amount pledged of $559. This tell us that those failed campagins, on average, were asking for double the amount of money than the successful campaigns and getting a much smaller amount pledged. The medaian for the goal and pledged amounts for the successful campagins are $3,000 and $3,168, respectfully, while the medians for the failed campagins goal and pladged amounts are $5,000 and $103. This further supports the idea that the failed campagins are asking for too much money which may deter backers from donating to them which results in very low pledged amounts.

After finding those statistics, I dug in a little deeper to get a better handle on what the data is telling us. I did this by fidning the Upper Quartile, Lower Quartile, and IQR of the data. The Upper and Lower Quartiles provide a range of the middle 50% of the data and are key in determining the Inter Quartile Range, IQR for short. he IQR can be used to help determine outliers in the data. I know that you are also tthinking about a future campagin for a UK play so I cerated some box and whisker plots to help you see the goal and pledged amounts of those campagins to prvide insight on how much you should be askign for in your campaign.

![UK Play BW](C:\Users\wardr\OneDrive\Desktop\Data Analytics Bootcamp\Analysis Projects\Crowd Funding Analysis\UK Play BW.png)

## Findings and Reccomendations

Based on this dataset, I have determined some key aspects of the successful and failed play campagins in the US. In general, plays are the most popular type of campagin on Kickstarter. The successful campaigns tended to ask for less money than the failed campagins and launch at the end of Spring. In order to be as successful as possible, I would reccomend asking for an amount around the average goal of successful campaigns and launching the campaign in May. For your future UK play, I would reccomend having a lower than average goal becuase the highest amount plesged is lower than the average goal. Just some things to keep in mind for the future. 

Good Luck, I can't wait to see the play!


