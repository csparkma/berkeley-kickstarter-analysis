# berkeley-kickstarter-analysis
Week 1 Excel Analysis on Plays

### Challenge
  #### Background
  _What question(s) are we trying to answer?_
  - *How many other Kickstarter campaigns were able to come close to their fundraising goal in a short amount of time?*
  - *Does length of a campaign contribute to its ultimate success or failure?*
  
  ##### Results
  Based only on the findings from the new analyses: *Outcomes based on Goals* and *Outcomes based on launch date*, I found it difficult to definitively answer the above questions. By only looking at when successful plays took place throughout the year and how many plays were successful by Goal amount, I was unable to conclude whether the `length of a campaign contributes to its success or failure.` However, we can use these as jumping off points for additional analysis to drill in further.
   ##### Seasonal Trends
  Let's start by attempting to identify a seasonal trend for theatre campaigns (chart below):
   ![Outcomes based on Launch Date](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/Outcomes%20based%20on%20Launch%20Date.png)

 - While the data does indicate that the majority of "Successful" theatre campaigns take place in the first half of the year, it does not necessarily tell us whether those months were more successful than others, *just that there was a higher volume of successful campaigns.*
 - It's also important to consider that this chart is looking at _all_ theatre campaigns, not just plays, which could cause misleading conclusions.
 
To better understand the reason behind why there are more "Successful" campaigns in the beginning of the year, we should first test whether it could be due to overall volume.
If we add a filter for the "Plays" subcategory and remove the "Outcome" field from our chart, we can see that total volume of plays does indeed follow the same trend as "Successful" plays in the above chart:
 ![Plays based on Launch Date](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/Plays%20by%20Launch%20Date.png)
  
 - *This supports the above hypothesis that the reason behind more "Successful" campaigns occuring in the first half of the year may only be due to having more total plays*.
 
To test this theory, we should look into whether the `% of total Successful campaigns` varies by month:
![Outcome percentage based on Launch Month](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/outcome_pct_based_on_launch_month.png)

- Based on the chart above, we can see that there is actually little variance between months when it comes to the % of Successful plays. All months vary between a 65%-70% success rate, with the exception of December.
- *This would lead me to conclude that a play's success is not determined by the month it takes place, but that there are other factors to consider when measuring success.*
 
   ##### Goal Setting
  Seeing as the success of a campaign is ultimately decided by whether it achieves its Goal, we should dive in to how Goal setting can influence the overall success rate.
  
  Below, we are looking at Outcomes based on Goal ranges (I have consolidated groupings with a goal higher than `30,000` into one cohort to account for low volume above 30k):
  ![Outcome percentage based on Goals](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/Outcomes%20Based%20on%20Goals%20Consolidated.png)
  
  - There appears to be an inverse relationship (negative correlation) between a Play's Success rate & Goal amount, while there is a positive correlation between Failure Rate and Goal amount. 
  - This makes sense seeing as the "Success" of a play is defined by whether it achieves its set Goal and an inflated goal would make it more difficult for plays to succeed by those standards.
  - General takeaway here would be: *Choose a realistic financial Goal*
  
  ##### Campaign Length
  Now that we have data to support that there aren't any seasonal trends we need to consider and that we should choose a realistic goal if we want our play to be deemed a success, we can now look at whether the length of our campaigns affects our success rate.
  
  I first started by calculating the length of each "Play" campaign and then grouped them into three brackets (measured in **days**):
  
1. "1-20"
2. "21-40"
3. "40+"

With all of the plays broken out into groups, I then calculated the success rate broken out between them:
![Outcome by Length of Campaign](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/Outcome%20by%20Length%20of%20Campaign.png)

- Based on this chart, I'd be inclined to conclude that shorter campaigns (i.e. <40 days) have a higher success rate compared to longer campaigns. However, due to our findings with Goal setting, we Should first determine whether there is any difference in Goal amount within each grouping:
![Avg Goal for All Plays](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/Average%20Goals%20for%20Plays.png)

![Avg Goal for Successful Plays](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/Avg%20Goals%20for%20Successful%20Plays.png)

![Avg Goal for Failed Plays](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/Avg%20Goals%20for%20Failed%20Plays.png)

- It's apparent that Successful campaigns have an average goal that is signifcantly lower than Failed campaigns. The **highest** average Goal for Successful plays is still **4.5% lower than the lowest average Goal for Failed plays.** But I do not think we can conclude that *Average goal* is the only influencing factor.
- Looking at the chart for Total Plays, we can see the *Average goal* between the "1-20" group and the "21-40" group **increases by 95% with little change in the Success rate**.
- However, the *Average Goal* between the "21-40" group and the "40+" group **increases by less than half of that** yet the *Success Rate* drops signficantly (42% for "40+" campaigns from 68% for "21-40")!
- Meaning, **there appears to be a significant dropoff in Success rate for campaigns that run longer than 40 days, especially if they have an inflated Goal.**

##### Conclusion
- Given the above analysis, I believe there is sufficient evidence to suggest that both the *Goal Amount* and the *Length of the campaign* **do** contribute to its overall succcess. However, without additional data on *how long it took for each campaign to hit its goal* (rather than just how long the campaign ran), it would be difficult to quantify by how much.
- Additional analysis should also be done on whether `backer_count` and `geographic region` influence overall success rate. While we can draw some conclusions from the above analysis, it would be inadvisable to use it to conclude that it is **only** *Goal amount* and the *Length of the campaign* that lead to success. 
