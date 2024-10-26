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

The main goal of this paper is to show causality between high salt intake and dementia. Prior research had already been done that suggested a correlation between these two variables, so this paper wanted to build upon that prior research to show there is in fact a causal relationship between the two variables. The study tests various different types of dementia: Alzheimer's disease, undefined dementia, etc. It also tests the relationship between high salt intake and general cognitive performance/decline. In this paper, the null hypothesis is that salt intake is not causally related with increased risk for dementia. The alternative hypothesis is that salt intake is causally related to increased risk for dementia. 

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


To access GWAS data for general cognitive performance, they went through Lee’s study and cited one of their references. The dataset ID was ebi-a-GC5T006572. I followed their works cited to find "Lee's Study" and found this a study titled : "Gene discovery and polygenetic prediction from a genome-wide association study of educational attainment in 1.1 million individuals" by Lee.J.J., Wedow R., et. al. You can find this study [here](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6393768/). I'm not gonna lie, this study seemed pretty good (when it came to being transparent with data) and they even have a whole section dedicated to all the software they used and the links to access the software as well as their databses online. HOWEVER... when I followed the [link to their database]( www.thessgac.org/data), I got a page not found error. Lee's study does link the contacts of some of their researchers to allow readers to contact them if they have any questions on the data, so if someone was desperate enough to get the data, maybe they could contact them. Anyways, I wasn't able to find or access this data used by the paper either 😢. 

The GWAS summary data on different types of dementia was obtained from the Finngen database. For VaD, the dataset identifier is “finn-b-F5 VASCDEM, for AD the dataset identifier was “finn-b-F5-ALZHDEMENT” and for unified dementia, the dataset identifier was “finn-b-F5_Dementia_U”. To try and access this data, I searched up Finngen database which brought me to this page: https://www.finngen.fi/en/access_results. From there, I filled out the form, once using my personal database and one with my horace mann email address. Both times, after I followed the instructions sent to my email (INSERT PHOTO), I was denied access to google cloud. I googled what google cloud was and I’m pretty sure you need a google workspace subscription to be able to use google cloud. Also, this may be because of some Horace Mann wifi regulation, everytime I opened a page with google cloud in the url I got this page: (INSERT PHOTO). 


The study then also included GWAS data on AD and PD from the European Population with identifier “finn-b-G6_ALZHEIMER” and identifier “finn-b-G6_PARKINSON” (respectively). 



## Why are they interested in this data?
5. What data is being recorded? What data might be left out?
6. What evidence did they present to back up their conclusions?
7. How was this study funded?
8. Do you think publish or perish had an effect on this study?
