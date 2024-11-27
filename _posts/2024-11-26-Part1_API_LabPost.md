---
layout: post
title: "API-Lab Lab Post"
subtitle: November 26th, 2024
tags: [Lab]
comments: true
mathjax: true
author: "Alisa Buitenhuis"
---

The extra query parameters that I chose to use were:
 1. Adolescent fertility rate (births per 1,000 women ages 15-19); ID = SP.ADO.TFRT
 2. Literacy rate, adult total (% ages 15+); ID = SE.ADT.LITR.ZS
 3. Proportion of seats held by women in national parliaments (%); ID = SG.GEN.PARL.ZS
 4. contraception prevalence (in percent) (15 + age); ID = SP.DYN.CONU.ZS
 5. Proportion of time spent on unpaid domestic and care work, male (% of 24 hour day); ID = SG.TIM.UWRK.MA
 6. Literacy rate, youth total (% ages 15-24); ID = SE.ADT.1524.LT.ZS

I tried to stick in the gender category, and I'm curious to see how these different parameters corrolate with one another. 
Firstly, I think that somethign like the proportion of seats held by women in national parilment is a pretty clear reflection of the gender nroms of the country 
because its highly unlikely that a super mysoginistic country would have a high number of women in its governement and (vice versa). Then, presumably, if a country 
treats men and women relatively equally, the proportion of time that men would spend on unpaid domestic work would increase (to level out with that of women). This is an example of
one of the hypotheseses that I wanted to confirm with the data. Another example could be the following. 
One thing I don't neccesarily have a hypothesis for but am curious about is whether having a higher time 
spent by men on domestic labour is corrolated with icnreased youth literacy or not. Depending on whether its a causal relationship or not 
(or whether there is any relationship at all with a significant P value), this could potentially suggest whether 
children are more educationally stimulated (measured by the literacy rates) under their fathers or their mothers care. 

I didn't purposely filter any countries out, but I did select a subset of countries, instead of just chosing them all. the way my code was setup, 
I need to have a list of countries prior to querying the API so I just decidede to randomely choose some countries that I was familiar with from this link : 
[COUNTRYISO3](https://www.iban.com/country-codes). For the years that I analyzed, I also randomely chose a few years. I tried to choose years within the range of years 
that data was gathered for the indicators hat I chose. 

MY P VALUES ARE COMING IN PART TWO OF THE LAB... STAY TUNED
