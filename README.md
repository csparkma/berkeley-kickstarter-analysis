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
  
 - *This supports the above hypothesis that the result of more "Successful" campaigns in the first half of the year may only be due to having more total plays*.
 
To back this up, we should also look into whether the `% of total Successful campaigns` varies by each month:
![Outcome percentage based on Launch Date](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/Outcome%20%25%20Based%20on%20Launch%20Date.png)

- We can see that there is actually little variance between months when it comes to the percentage of Successful plays. Most months only vary between a 65%-75% rate, with the exception of December.
- *This would lead me to conclude that success is not determined by when your play is hosted throughout the year, but that there are other factors to consider when considering success.*
 
 
