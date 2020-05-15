# berkeley-kickstarter-analysis
Week 1 Excel Analysis on Plays

### Challenge
  #### Background
  _What question(s) are we trying to answer?_
  - *How many other Kickstarter campaigns were able to come close to their fundraising goal in a short amount of time?*
  - *Does length of a campaign contribute to its ultimate success or failure?*
  
  ##### Results
  Based only on the findings from the two new analyses (outcomes based on goals and outcomes based on launch date), I found it difficult to answer the above questions. By only looking at when successful plays took place throughout the year and how many plays were successful by Goal amount, I was unable to conclude whether the `length of a campaign contributes to its success or failure.` However, we can use these as a jumping off point for additional analysis to drill in further.
   
  Let's start by attempting to identify a seasonal trend for theatre campaigns (chart below):
   ![Outcomes based on Launch Date](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/Outcomes%20based%20on%20Launch%20Date.png)
 
 - An important consideration in this chart is that it is looking at _all_ theatre campaigns, not just plays, which can be misleading.
 - While the data does indicate that the majority of successful theatre campaigns take place in the first half of the year, it does not necessarily tell us whether those months were more successful than others, *just that there was a higher volume of successful campaigns.*
 - It's also important to consider that this is looking at _all_ theatre campaigns, not just plays, which could cause misleading conclusions.
 
If we add a filter for "Plays" subcategory and remove the "Outcome" field from our chart, we can see that total volume follows the exact same trend as "Successful" campaigns:
 ![Plays based on Launch Date](https://github.com/csparkma/berkeley-kickstarter-analysis/blob/master/Plays%20by%20Launch%20Date.png)
  
 - *This supports the above hypothesis that the result of more "Successful" campaigns in the first half of the year may only be due to having more total plays*.
 
