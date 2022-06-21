# Reproductive Health and Climate Change

## Abstract

Many don’t realize it, but contraceptives and family planning have a giant impact on reducing our planet's carbon emissions, 20 times more of an impact than things like recycling or driving an efficient car, because...well... humans are responsible for most carbon emissions. Using worldwide contraceptive data, I'm creating an interactive map to pinpoint areas that are lacking contraceptive care and hope to find out why those areas are struggling more than others.   

## Context

### The problem
One of our world's largest problems right now is climate change. The huge amount of carbon humans are currently pumping into our atmosphere is having catastrophic effects. Floods, massive fires, extreme weather/storms, and higher temperatures than ever seen before (to name a few). Our society is also having major issues respecting women's bodily autonomy and need for reproductive healthcare, the biggest event to note is the overturning of Roe v Wade. We need to identify what areas need the most help and see how the choices they're making will affect their future.

### Why is this important to solve?
One climate solution that can have a huge impact is not having as many children. This is in no way a request for people to no longer have kids, but if you don't want children right now, you shouldn't be having them. Scientists predict that family planning (non-having babies if you don’t want to) and the education of girls (which can lead to delayed onset of marriage, and delayed childbearing -Project Drawdown) could prevent the release of 119.2 gigatons of carbon into the atmosphere. This won't only help the planet but is also a crucial step in women journey towards respect and equity. Better access to contraception and education will provide families (but specifically women) better agency over their lives and bodies and can help save the planet too. 

## Proposal 

## Specific question I'm trying to answer
Right now, we know family planning would have a huge effect on climate change but don’t have a way to get the ball rolling. What areas need resources in the first place? Pinpointing specific areas that need care and exposing the relationship these areas have with our society’s systems (like racism, classism…) will help me create a resource for people to learn and donate to the cause.

### How I will answer it
I hope to use a mix of R Studio and Tableau to make an interactive resource (currently planning on a shiny app) that uses color to indicate a certain region's family planning resources. Viewers will be able to see what areas are lacking support (as well as the demographic make-up of those spaces) and the app will provide them with information and easy ways to fund better reproductive health care resources.

### What I expect/hope to find
It's hard to say exactly what states will have more issues than others, but I can already see a relationship between people’s access to contraceptive care and their state’s political affiliations. I hope that this project will help me illuminate the relationship of who has the biggest issues accessing contraceptive resources and how those folks are disproportionately affected by climate change. I think this final argument will help tie the whole project together.

## Conclusion

### Summary
Our world's carbon emissions are getting out of control and many are left feeling like there isn't much they can do to stop it. Many environmentally friendly choices (like composting or purchasing eco-friendly products) aren't accessible to all and do not meaningfully impact carbon emissions. In contrast, better family planning and allocation of educational resources is something individuals can fund right now that actually makes a measurable impact. An interactive heatmap will give people a way to find out what US states (and what people in those states) need the most support giving their residents proper reproductive health care.

### How my solution could be important beyond this specific context
This app set up could be applied to country-based data. You could, for example, see if there’s a relationship between countries with better healthcare plans and contraceptive access or how political relations have an effect on access. This topic could also be narrowed to include county data in each state.

### Limitations and potential future directions
The biggest issue with this topic is that its data is interesting but pretty fuzzy. There's no clean data set that displays how each child born directly relates to an increase in carbon emissions. This project will have to be theory based and mainly focused on identifying areas that need support. It will also be difficult to find ways to support different regions. I expect the final version of this project to be clean and polished, however, I'm not opposed to having this app be a launching point for further resources and research on how to help the planet with family planning and education. 

## Data Description, Origins, Limitations, Features (amongst other things)

Data related to population was sourced from:
https://dilemma-x.net/2016/12/21/u-s-state-populations-2016-most-populous-states/

Political affiliation data was coded by hand (it's surprisingly hard to get a simple data set on final results from this year). The information was based off: https://en.wikipedia.org/wiki/2016_United_States_elections

The main data set was sourced from the Guttmacher Institute : https://data.guttmacher.org/states/table?state=AL+AK+AZ+AR+CA+CO+CT+DE+DC+FL+GA+HI+ID+IL+IN+IA+KS+KY+LA+ME+MD+MA+MI+MN+MS+MO+MT+NE+NV+NH+NJ+NM+NY+NC+ND+OH+OK+OR+PA+RI+SC+SD+TN+TX+UT+VT+VA+WA+WV+WI+WY&dataset=data&topics=143+146+262+145

This main data source allows you to pick what states and what topics you want to view in a table. I tried to stick to simple results related to contraceptive care so in case this project needs to expand, I can narrow down to individual county data and show similar results. I grouped the information by race and poverty level and took a look at women who needed care and were uninsured.

There are sometimes multiple sources for Guttmacher data downloaded from this website but the main source for my downloaded data was: https://www.guttmacher.org/report/publicly-supported-FP-services-US-2016

Here is the main methodology for how values were calculated:

"Estimates were produced by combining 2016 population data from the U.S. Census Bureau with information on income level and marital status from the 2014–2016 ACS and characteristics of women from the 2011–2015 NSFG. We calculated the proportion of women in various population groups who met the specified criteria (detailed above in Key Definitions) indicating their potential to seek contraceptive services and supplies during the year using the 2011–2015 NSFG, a nationally representative cross-sectional survey of 11,300 women aged 15–44 conducted by the U.S. National Center for Health Statistics. The proportion of women with the potential to seek contraceptive services in population groups defined by each age by marital status by income level by race and ethnicity group were then applied to county-level estimates of the number of women in each of these population groups. Estimates were made at the county level and then summed to obtain state and national estimates. For further explanation of this methodology, see the Methodological Appendix."

## EDA results 
This EDA was done through tableau rather than R. Images render best within tableau, but I have attempted to export and include them anyways. (Update: I was not successful).

The first thing I looked at was the number of uninsured women were likely in need of contraceptives and supplies. I looked at a map of the US and colored the different states depending on the number of women who needed care.

![Image1]("Image1.png")

I noticed from this map, the number of people was highly reliant on the population of that state. Since this data was sourced from 2016, I found a data set that contained the state populations from that year and connected the two tables based on state. Then I made a new variable that found the percent of people in each state who were uninsured and in need of resources.

![Image2]("Image2.png")

This map shows that the percentage only ranges from 4-8 percent. We can now see which states need support because they have a large number of people (our first image) and which states have a larger percentage of women needing support (our second image). It appears that many states in the south and traditionally republican states don't appear to have as good contraceptive care resources for their residents. To show this difference in political parties, I decided to show states political affliction for that year.

![Image2]("Image3.png")

This new graph told a much better story. I was originally worried this data was completely based off of census data (they used surveys to calculate information as well but they don't elaborate what fields surveys helped calculate and what just uses census data) we and the population data I found was just different enough from their calculations that it appeared there was some random difference between states. However, the difference in contraceptive access for Republican and Democratic states shows that this isn't a completely random calculation. There is a clear correlation between a state's political leanings and the percentage of women who are in need of publicly funded contraceptive care and resources. 

Now we can see that, in general, Republican states have much higher percentages of women who are uninsured and in need of contraceptive care/resources while Democratic states are much lower. I couldn't get the y axis to be more helpful but I think the separation and color coding make up for it. I'm looking forward to continuing this exploration of data and moving towards studying the racial make ups of women in need.


