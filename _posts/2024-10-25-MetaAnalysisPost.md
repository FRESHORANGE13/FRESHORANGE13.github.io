---
layout: post
title: "Meta Analysis Post"
subtitle: October 25th, 2024
tags: [Lab]
comments: true
mathjax: true
author: "Alisa Buitenhuis"
---

## Background Information: 
The title of the research paper is "Association between adding salt in food and dementia in European descent: A Mendelian randomization study". You can read the article [here](https://research-ebsco-com.horacemann.idm.oclc.org/c/qideok/viewer/pdf/od3wz6rtdj) - as long as you are on your Horace Mann Account I think. It's main authors and contributors were Ren Zhou and Hong Jiang. 

The main goal of this paper was to show causality between high salt intake and increased risk of dementia. Prior research had already been done that suggested a correlation between these two variables, so this paper wanted to build upon that prior research to show there is in fact a causal relationship between the two variables. The study tested various different types of dementia: Alzheimer's disease, undefined dementia, etc. It also tested the relationship between high salt intake and general cognitive performance/decline. In this paper, the null hypothesis was that salt intake is not causally related with increased risk for dementia. The alternative hypothesis was that salt intake is causally related to increased risk for dementia. 

## Why are they interested in the data they used + how did they use it?
They based their study on a type of study design known as Mendelian Randomization (MR). MR is used to estimate the causal effects of certain risk factors for diseases using known genetic variants (also known as SNPs, in this study) as instrumental variables (IVs). In the authors' own words, "MR leverages naturally occurring genetic variations associated with modifiable risk factors to provide insights in topotential causal links while minimizing the confounding and reversecausation issues that commonly affect observational studies." In my understanding, the data this study used provided the different SNPs and exposure factors that are associated with salt intake as well as those associated with different dementias. Then, they used various statistical analysis methods (IVW methods, MR-Egger, MR-PRESSO,and WM analysis) to try and determine whether the relationships between the IVs and the risk factors were causal and how strong those relationships were. 

In order to assess causality in a rigorous way, they elimated all SNPs of genes that were associated with multiple traits. They also deleted all SNPs that could contribute to confounding factors. Then, after all that, they calculated the F-statistic (described on page 4 of their paper) in order to insure the IVs were strongly corrolated with the exposure factors that they wanted to assess the impact of. 

Here is a photo of the part of their paper that describes this, because it is a bit more clear in their words: 
![photo of IVs section](/assets/img/IVs.png)

## What datasets does this study reference or use? Are these datasets available to the public?

This study used data obtained  from GWAS, which stands for Genome-wide association studies (GWAS). These types of studies look at small genetic variations within a huge pool of people in order to associate specific changes in nucleotides within genes to specific traits. These small variations in nucleotides are referred to as single nucleotide polymorphisms (SNPs). 

The data on the genetic variation of added salt to food was taken from the UK Biobank. The dataset identifier was “ukb-b-8-12”. You can access the UK Biobank through [this link](https://www.ukbiobank.ac.uk/.) 
but, after that, when I clicked on "participant login" I got this page:

![BioBankLoginScreenshot](/assets/img/BioBankScreenShot.png) 

Without an ID, you cant really go much further so I wasn't able to access this data 😔. However, if a researcher wanted to replicate this study and access this data, they could probably find a way to register and get and ID to access the UK bio bank. 


To access the GWAS data for dementia, the authors of the study went through the IEUOpenGWASdatabase. To access the GWAS data for dementia, the authors of the study went through the [IEUOpenGWASdatabase](https://gwas.mrcieu.ac.uk/). The ID they used to search for the dementia data is “finn-b-F5_DEMENTIA”. After searching for this ID in the database, I got to [this page](https://gwas.mrcieu.ac.uk/datasets/finn-b-F5_DEMENTIA/), which showed this: 

![SCREENSHOT OF DEMENTIA DATA](/assets/img/DEMENTIADATA.png)


As you can see, there aren’t any download buttons. To try and download the data, I looked through the about page which said to run the command “wget https://gwas.mrcieu.ac.uk/files/ukb-b-19953/ukb-b-19953.vcf.gz”. This uses "ukb-b-19953" as an example dataset ID. Before even running the terminal command, I looked for the dataset that corresponded to the ukb-b-19953 ID on the website and found this: 

![BMI dataset photo](/assets/img/BMIDatasetScreenShot.png)

Here there is a download button! So its a little werid that there isn't one for the dataset used in the study...🤨🤨 Anyways, I still wanted to try the terminal command. I replaced the example ID with "finn-b-F5_DEMENTIA” and for macs, the equivalent to the "wget" command is “curl”, so I ran "curl https://gwas.mrcieu.ac.uk/files/ukb-b-19953/ukb-b-19953.vcf.gz". 

When I ran the terminal command with the example datatset from the about page, I got a downloadable file: 

![terminal command example](/assets/img/exampleTerminalFile.png)

On the other hand, when I tried to run the terminal command with the ID of the dataset used in this study, I got this instead:

![terminal command no download](/assets/img/NoDownload.png)

To sum this up, I was not able to access the data from the IEUOpenGWASdatabase 😔😔. 


To access GWAS data for general cognitive performance, they went through Lee’s study and cited one of their references. The dataset ID was ebi-a-GC5T006572. I followed their works cited to find "Lee's Study" and found this a study titled : "Gene discovery and polygenetic prediction from a genome-wide association study of educational attainment in 1.1 million individuals" by Lee.J.J., Wedow R., et. al. You can find this study [here](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6393768/). I'm not gonna lie, this study seemed pretty good (when it came to being transparent with data) and they even have a whole section dedicated to all the software they used and the links to access the software as well as their databses online. HOWEVER... when I followed the [link to their database]( www.thessgac.org/data), I got a page not found error. Lee's study does link the contacts of some of their researchers to allow readers to contact them if they have any questions on the data, so if someone was desperate enough to get the data, maybe they could contact them to gain access. Anyways, I wasn't able to find or access this data, so the general public probably wouldn't be able to either 😢. 

The GWAS summary data on different types of dementia was obtained from the Finngen database. For Vascular Dementia (VaD), the dataset identifier is “finn-b-F5 VASCDEM, for Alzheimer's Disease (AD) the dataset identifier was “finn-b-F5-ALZHDEMENT” and for undefined dementia, the dataset identifier was “finn-b-F5_Dementia_U”. To try and access this data, I searched up Finngen database which brought me to [this page](https://www.finngen.fi/en/access_results). 
After scrolling down a bit I found this: 

![form for database access](/assets/img/AccessDataFinngen.png)

From there, I filled out the form to gain access to the databases, once using my personal email address (and my alias of course), once using my alias and my alias's email adress (as depicted below) and once with my name and my horace mann email address. 

![filling out form](/assets/img/SammyBrown.png)

All three times, after I followed the instructions sent to my email, I was denied access to google cloud. I googled what google cloud was and I’m pretty sure you need a google workspace subscription to be able to use google cloud - which I don't have unfortunately.  Also, this may be because of some Horace Mann wifi regulation, but everytime I opened a page with google cloud in the url I got this page: 

![page not found google cloud](/assets/img/pagenotfoundgooglecloud.png)

At this point I gave up on accessing the Finngen datasets as well...

There was a bit more data then taken from "independant multicenter studies", but at this point I've spent so much time searching for data and I'm pretty sure this will end up being like Lee's study, were the data still can't be accessed from. 


The study then also included GWAS data on AD and PD from the European Population with identifier “finn-b-G6_ALZHEIMER” and identifier “finn-b-G6_PARKINSON” (respectively). I googled "European Population datasets" and nothing really came up  other than the European commissions database, which is not it. So this is yet another 2 datasets that I could not find or access. 

There were a few other datasets the study used to supplement their data or add more information on certain SNPs, more information on certain types of dementias, etc., but as the list of datasets goes on, they contribute less and less to the main point of this study. Even if I would be able to access those datasets, at this point there have already been so many that I haven't been able to access that I don't think it would impact the overall transparency of this paper. 

(Since I couldn't actually access the data used, I don't know who actually collected the data in any of the datasets)

In conclusion, while this paper, at a glance, seemed to be extremely transparent and forward about which datasets they used and how to access them, in reality, it wasn't actually that straightforward. I could not access a single dataset that I tried to find. Some of them I couldn't access because I didn't have an ID, or I didn't have a subscription to a service, so maybe it would have been possible to access those if I was extremely invested in finding them and had the means to invest money or apply for an ID. For others though, the data just simply wasn't available online (at least to the extent that I looked for it, which I think is a lot more than the general public would do). This shows how difficult it would be to replicate this study with the same data they used, which definetly harms its reliability rating. 

## Finding their funding:
This paper was funded by the Science and Technology Commission Of Shanghai Municipality. In the conflict of interest statement, the authors stated that they had no conflicts of interests due to funding. After I searched up “Science and Technology Commission Of Shanghai Municipality”, I found [their about page](https://stcsm.sh.gov.cn/yww/). It seems as though it is only affiliated with the govenrment and no coorporations that would have insentive to spin the narrative one way or another, so it seems as though there are indeed no conflict of interests from their funding. 

## Was this paper effected by publish or perish?
A lot of this study was replicating certain aspects of different studies, meaning that they don’t have any obvious unwarranted flashiness to “click-bait” journals into letting them publish the paper. While their findings are important, they didn’t come completely out of nowhere so it wasn’t like they tried to study a topic just for the sake of it getting crazy results. Additionally, this paper doesn’t actually prove causality for increased risks to all types of dementia after being analyzed using all the statistical tools they tried, it just provides more evidence to suggest a moderate or strong causality for some types of dementia. This less rigorous claim suggests that they didn’t exaggerate their results for the sake of the conclusion sounding stronger. 

## My overall rating of the study: 
 drumroll please....





















.....

























 6/10



 ....
 I think the fact that this study was transparent about their work and tried to disclose all the information that they could (whether or not that information actually gave the public anyway to replicate their research or not), was quite admirable. For example, me personally, if Chat GPT ever assists my writing, I probably would hide the fact that Chat GPT assisted me, instead of disclosing it right at the begginig of the works cited section like the authors of this paper did. I also think that the topic of the paper was interesting for me, which helped me stay engaged and made me enjoy reading the parts of the paper I could almost understand. However, it, very often, became very difficult to follow their expiramental design. I was not priorly familiar with MR study designs, but they wrote their paper as if the person reading it was pretty comfortable with it. Even now, I'm honestly still not fully sure what all their data was used for and whether I interpreted it right. If I were gading their paper, I would definetly tell them to work a bit on their communication. Also, there were a few grammar typos, so I'm not really sure how those got through the peer reviewing that needed to be completed in order for them to have published their paper. Then of course, the fact that I could not access a single one of their databases that I tried to access definetly lowers their score a bit. 
 
 Anyways, this is the end of my Meta Analysis Lab Post. Hope you've been having a nice weekend and hope this wasn't too much of a hassle to read (sorry I made it this long). See you Monday 😊!!


