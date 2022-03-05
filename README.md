# Crowdfunding-Analysis

---

---

    An analysis of Kickstarter campaigns

---

---

## Overview

---
    In this analysis we utilized Excel to examine a Kickstarter dataset of many fundraising campaigns in order to make recommendations to best ensure the success of Louise's campaign for the production of her play, Fever.
---

---

## Analysis and Challenges

---
    Our analysis began by importing an excel file from our module containing data on many Kickstarter campaigns for a variety of projects across the world.  We began by color coding the various outcome options and using a color gradient for the percentage of a project's funding goal received in order to make the results of a Kickstarter campaign easier to visually identify and interpret.  Additionally, we converted a single column of categorical information into a parent and subcategory to be more able to effectively filter the data for our purposes.  We converted the given Unix timestamps for campaign start and end dates algebraically with the DATE formula in order to display convential dates.  We then filtered the data to only include those in the parent category of theater.  This allowed us to examine a pivot table only containing theater campaigns to view their resulting successes, failures, and cancellations against their month of origin.  From the pivot table we are able to visualize the data with a line graph.  The graph displays a sharp spike of successes in May with with its lowest point of successes in December.
---

![Outcomes by Starting Month](/Resources/Theater_Outcomes_vs_Launch.PNG)

---
    We continued by grouping our data by their goal amount for their campaign.  This allowed us to use the COUNTIFS and SUM functions in order to view the totals and proportions of outcomes for plays for each goal range.  Taking those proportions, we are able to build another line graph, but one that displays outcomes against desired goal amount.  It happened to be that no play campaigns were cancelled, leaving successes and failures summing to 100% across the graph.  As the goal amount goes up, the likelihood of success drops.  The trend appears to reverse in the $35,000-$44,999 sections, but these are less than ten data points in a set of over one thousand plays.
---

![Outcomes by Goal Amount](/Resources/Outcomes_vs_Goals.PNG)

---
    The main challenge of this exercise was the use of proper syntax.  I am inexperienced with Excel and was frequently getting a reference error by mistyping or not having appropriate quotation marks within the COUNTIFS function.  I also have never used markdown before and when compiling the rough draft of this README in lesson 1.6 I struggled heavily attempting to display images hosted in the same repository.  Adjusting to using the relative path provided by Visual Studio Code is helping but I am still a little unclear.  My last updates before starting this challenge still only displayed my images in the VSC preview while reading on GitHub as hyperlinks to a 404.  Additionally, the process of editing chart colors in Excel seems counterintuitive. Most of the base palettes defaulted either my "successful" line to a shade of red or my "failed" line to a shade of blue or green, which is undesirable as it could be misleading.  I changed the color of the line, marker, and marker border of each of the lines on the graph to more intuitive colors, but this process seemed unnecessarily time consuming.  I remember we discussed a bit of chart design in class so I will look for that when I review the video from last week.

---

## Results

---

### Theater Outcomes by Launch Date

    It is clear that theater campaigns are most successful with start dates in May, followed by June.  This is a traditional timing of spring theater productions and is probably also related to these months being the start of predictably pleasant weather in many areas of the US, where the majority of these campaigns are conducted, especially greatly assisting the success of any outdoor programs.  As Louise's production will be in the US we strongly suggest that she begin her campaign in May.  We also strongly suggest avoiding the winter months.  Most notably, December has almost equal numbers of successes and failures with less campaigns beginning overall.  We can use the COUNTIFS function with the country column to see that the dataset is almost entirely from extremely Christian, English-speaking countries.  Individuals in these countries are far more likely to spend large portions of and sometimes amounts greater than their disposable income in November and December, leading to increased scarcity of donation funds for Kickstarter projects.  At this point campaign organizers understand both of these effects and others, as we see both a far higher total number of projects launched in the summer months and a much higher rate of success.
---

### Play Outcomes by Goal Amount

    Our other graph of outcome proportion plotted against desired goal amount shows a strong negative relationship between dollars desired and likelihood of success.  The trend is a consistent negative assosciation interrupted by an apparent spike in the two-group range of $35,000 to $44,999.  This spike represents only six successful and three failed plays out of a set of one thousand and forty-seven total plays.  It is to be ignored for Louise's purposes for that reason, especially considering that her goal is to raise $12,000.  $12,000 falls within the band $10,000 to $14,999, for which we have an observed probability of success of 54%.  We are not able to predict much about Louise's potential success or failure based on her goal amount.  It is worth noting that for the preceding band of $5,000 to $9,999 and following band of $15,000 to $19,999, the respective observed likehoods of success are 55% and 50%, both very close to the number of her band at 54%.  This shows that any reasonable alterations in spending are unlikely to strongly influence Louise's likehood of success.  Unless she plans on cutting over 60% of her budget or almost doubling it, she will remain within these three goal bands containing observed likehoods of success all between 50% and 55%.  This allows us to suggest to Louise that she organize the play and its budget almost exactly to her tastes, since small changes to the budget do not seem likely to significantly harm or improve her chances.
---

### Limitations and Possible Recommendations

    The first and most apparent limitation of this dataset is that it only contains data from Kickstarter.  While Kickstarter is very popular, it is possible that there are aspects or conditions of the site that can affect likehood of success for different campaigns in unforseen ways.  It would be preferable if there was a dataset containing information about campaigns across a variety of fundraising sites, and even better if we had data for fundraisers conducted offline as well.  With that data, we could potentially plot successes and failures for each option and recommend an optimal platform for Louise's fundraiser.  One other limitation is that there is little to no detail about how each campaign was conducted.  While we have the beginnning and ending points of each campaign, if there were additional data such as dollars allocated to advertising, years of organizer industry experience, or perhaps economic indicators of the location of the project, we would be able to generate further and deeper insights.  Variables like these could allow us to view likehood of success as a function of advertising expenditures, experience working in the industry, or the location of the project.  Raising $10,000 for a performing arts project in Los Angeles or New York is much different than doing so in Dayton or Athens in Ohio.  Comparing to another country would be even more complicated.  It would be very useful if specifically the play project data (or projects than involve any gathering of people) detailled whether it was intended for an outdoor or indoor theater.  If Fever is meant to be held outdoors, then it is imperative for her to begin her fundraiser in the warmer months.  If it is meant to be held indoors, it is possible that the starting month is less significant.  To determine this we would isolate both indoor and outdoor play projects and compare their success rates by starting month.  If success rate differentials between the indoor and outdoor groups across starting months are statistically significant, it can be concluded that the overall changes in success rate by month can be largely explained by the changing seasons and their accompanying effects on behavior.  Depending on Louise's plans for Fever this could change our recommendation.
