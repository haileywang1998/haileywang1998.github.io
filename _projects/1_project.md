---
layout: page
title: An analysis of factors affecting support for President Tsai 
description: a regression model with R language
img: assets/img/publication_preview/reelect.jpeg
importance: 3
category: 2019
related_publications: 
---

As the 2020 presidential election loomed, people were curious about the factors that influenced their assessment of a president's performance and their decision to re-elect them.

In my research, Tsai Ing-wen was Taiwan's president at that time, preparing for her second term. To understand what factors swayed voters, I analyzed data from a 2019 survey on Tsai's governance satisfaction conducted by the Taiwan Election and Democratization Study. 2,298 individuals participated in the poll. I selected nine specific factors from the poll and constructed a regression model with R language to examine their correlation with support for Tsai.

I analyzed nine factors in this research. I will briefly introduce each of them:
1. *Voters’ gender*
2. *Voters’ education level*
3. *Trust in China*
Tsai was the leader of the pro-independence ruling Democratic Progressive Party, so voters' attitude toward China might affect their support for Tsai.
4. *Preference for Ko Wen-je*
5. *Preference for Chu Li-lun*
6. *Preference for Han Kuo-yu*
These three people are competitors from Tsai’s rival parties.
8. *Preference for Lai Ching-te*
 Lai is in the same party as Tsai. They were debating on who to run the next turn at that time.
10. *Satisfaction with Tsai’s leadership*
Participants rated Tsai’s governance performance in the poll based on her first turn.
12. *Trust in Tsai.* 
In the poll, participants rated whether they trusted Tsai.

The multiple regression equation is:

$$Y = β_0 + β_1X_{ko} + β_2X_{lai} + β_3X_{chu} + β_4X_{han} + β_5X_{trut} + β_6X_{truc} + β_7X_{lead} + β_8X_{sex} + β_9X_{educ} + u_i$$

In this equation: 

$$Y$$ represents "overall satisfaction with President Tsai Ing-wen's governance"

$$X_{ko}$$ represents "preference for Ko Wen-je" 

$$X_{lai}$$ represents "preference for Lai Ching-te" 

$$X_{chu}$$ represents "preference for Chu Li-lun" 

$$X_{han}$$ represents "preference for Han Kuo-yu" 

$$X_{trut}$$ represents "trust in Tsai Ing-wen" 

$$X_{truc}$$ represents "trust in China" 

$$X_{lead}$$ represents "satisfaction with Tsai Ing-wen's leadership" 

$$X_{sex}$$ represents the "gender"

$$X_{educ}$$ represents the "education level"

$$u_{i}$$ represents the error or residual term in the equation

Here is the result!

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/publication_preview/reelect.jpeg" title="factors affecting re-election" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    T-value of factors affecting support for Tsai.
</div>

For each factor, if the absolute value of the t-value is larger than 1.96, it means that the factor is statistically significant under 95% confidence level. Here, we see “Preference for Ko,” “Preference for Han,” “Satisfaction with Tsai’s leadership,” and “Trust in Tsai” are the factors that statistically affect voters’ support for Tsai. Other factors have no significance.

🌸 **Findings:** 🌸

The results revealed that "Preference for Ko," "Preference for Han," "Satisfaction with Tsai's leadership," and "Trust in Tsai" significantly influenced support for Tsai. Other factors didn't show statistical significance.

Interestingly, mainstream media in Taiwan suggested that Tsai's female identity would attract more female voters. However, my findings contradicted this perception, as there was no statistical correlation between gender and support for Tsai.

The Democratic Progressive Party (DPP), to which Tsai Ing-wen belonged, had two internal groups, one supporting Lai Ching-te for the presidency and the other backing Tsai for running for another term. Despite media expectations that people who support Lai were less likely to support Tsai, there was no statistically significant relationship between the two factors. 

When we delve into the reasons for support, "Satisfaction with Tsai's leadership" and "Trust in Tsai" stood out. These two indicators directly reflected participants' views on her performance during her first term. It appeared that voters were more influenced by performance rather than their own identity factors like gender and education level.

"Preference for Ko" and "Preference for Han" demonstrated that political affiliations played a role in candidate support. Ko Wen-Je, although an independent candidate, aligned closely with the DPP's values, and his supporters were more likely to support Tsai. Conversely, Han Kuo-yu, Tsai's toughest rival, came from a different party, and his supporters were less likely to back Tsai.

In conclusion, this research provided valuable insights into the factors affecting support for Tsai, challenging some popular assumptions. Gender and loyalty to another candidate in Tsai's party, for instance, were found to have no impact on voters' support for the President.
