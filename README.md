# berkeley-kickstarter-analysis
Week 1 Excel Analysis on Plays

### Challenge
  #### Background
  _What question(s) are we trying to answer?_
  - *How many other Kickstarter campaigns were able to come close to their fundraising goal in a short amount of time?*
  - *Does length of a campaign contribute to its ultimate success or failure?*
  
  ##### Results
  Based only on the findings from the two new analyses (outcomes based on goals and outcomes based on launch date), I found it difficult to answer the above questions. By only looking at when successful plays took place throughout the year and how many plays were successful by Goal amount, I was unable to conclude whether the `length of a campaign contributes to its success or failure.` However, we can use these as a jumping off point for additional analysis to drill in further.
   ##### Seasonality Trends
  Let's start by attempting to identify a seasonal trend for theatre campaigns (chart below):
   ![Outcomes based on Launch Date](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/Outcomes%20based%20on%20Launch%20Date.png)

 - While the data does indicate that the majority of "Successful" theatre campaigns take place in the first half of the year, it does not necessarily tell us whether those months were more successful than others, *just that there was a higher volume of successful campaigns.*
 - It's also important to consider that this chart is looking at _all_ theatre campaigns, not just plays, which could cause misleading conclusions.
 
To better understand the reason behind why there are more "Successful" campaigns in the beginning of the year, we should first test whether it could be due to overall volume.
If we add a filter for the "Plays" subcategory and remove the "Outcome" field from our chart, we can see that total volume of plays does indeed follow the same trend as "Successful" plays in the above chart:
 ![Plays based on Launch Date](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/Plays%20by%20Launch%20Date.png)
  
 - *This supports the above hypothesis that the reason behind more "Successful" campaigns occuring in the first half of the year may only be due to having more total plays*.
 
To test this theory, we should look into whether the `% of total Successful campaigns` varies by month:
![Outcome percentage based on Launch Date](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/Outcome%20%25%20Based%20on%20Launch%20Date.png)

- Based on the chart above, we can see that there is actually little variance between months when it comes to the % of Successful plays. Most months vary between a 65%-70% success rate, with the exception of December (I'm not considering March due to the ~15% that are still live.).
- *This would lead me to conclude that a play's success is not determined by the month it takes place, but that there are other factors to consider when measuring success.*
 
   ##### Goal Setting
  Seeing as the success of a campaign is ultimately decided by the Goal, we should dive in to how Goal setting can influence the overall success rate.
  
  Below, we are looking at Outcomes based on Goal ranges (consolidated groupings to `>30,000` to account for low volume in higher goal ranges):
  ![Outcome percentage based on Goals](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/Outcomes%20Based%20on%20Goals%20Consolidated.png)
  
  - There is a clear inverse relationship (negative correlation) between a Play's Success rate & Goal amount, while there is a positive correlation between Failure Rate and Goal amount. 
  - This makes sense seeing as the "Success" of a play is defined by whether it has hit its goal or not and an inflated goal would make it more difficult for plays to succeed by those standards.
  - General takeaway here would be: *Choose a realistic financial Goal*
  
  ##### Campaign Length
  Now that we know that there aren't any seasonal trends we need to consider when it comes to success and that we should choose a realistic goal if we want our play to be deemed a success, we should now look at whether the length of our campaigns has an effect on success.
  
  I first started by calculating the length of each campaign in days and then grouped them into three brackets (all in days):
  
1. "1-20"
2. "21-40"
3. "40+"

Now that we have our groups, let's take a look at the success rate broken out between them:
![Outcome by Length of Campaign](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/Outcome%20by%20Length%20of%20Campaign.png)

- Based on this chart, I'd be inclined to conclude that shorter campaigns (i.e. <40 days) are more successful than longer campaigns. However, due to our findings with Goal setting, we Should first see if there is any difference in average goals within each grouping:

![Avg Goal for Successful Plays](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/Avg%20Goals%20for%20Successful%20Plays.png)

![Avg Goal for Failed Plays](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/Avg%20Goals%20for%20Failed%20Plays.png)

- It's apparent that Successful campaigns have an average goal that is signifcantly less than Failed campaigns
- That being said, it does appear that campaign length **does** contribute to the success of campaigns. We can see this as the avg goal for successful campaigns only differs by 8% between 21-40 day campaigns and 40+ day campaigns, yet the difference between their success rate is 62% (42% for "40+" campaigns and 68% for "21-40").
- We can conclude that campaigns with both shorter campaign lengths and a smaller goal are more successful.



##### Limitations
- How long did it take for each campaign to hit its goal
- Live data can skew results
- 
