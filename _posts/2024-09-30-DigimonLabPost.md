---
layout: post
title: "Lab 1: Digimon"
subtitle: Sepember 18th, 2024
tags: [Lab]
comments: true
mathjax: true
author: "Alisa Buitenhuis"
---

For the first question (What is the average HP of all Digimon?), I began by processing the data. Then I iterated through the dictionaries to access the HP value of each Digimon and then adding the HP to a variable that kept track of the total HP of the Digimon. To finish it off, I printed the total HP divided by the total number of Digimon, which is the same as the average HP of all the digamous. 

For the second part (Write a a function that can count the number of Digimon with a specific attribute), I began by defining the function to pass in two parameters: one for the attribute and one for the type of the attribute that we are searching for. Then, similarly to the first part, I iterated through the data. If the given attribute of a Digimon matched the specific type that we were looking for, I incremented a count variable by 1. In the end, I printed this counter variable, which represents the total number of Digimon with their specified attribute matching the specified type. 

For the third part (Name a team of up to 3 Digimon that has at least 300 attack (Atk) in total that is restricted by a total amount of memory), I began by appending each row of the Digimon data into a list of dictionaries, to make it easier to iterate through the data in a way were I can access specifically numbered rows. Then, I sorted the list from highest to lowest memory of the Digimon in each row. Next, I iterated through the data. Within the loop,  I check if the Digimon has the ability to be on a team on its own, the Digimon before or the two Digimon before. If it works with the attack and memory constraints, then I add it to my list of viable teams. In the end, I output all the viable teams that my algorithm came up with, though this usually isn’t all the possible viable teams. 

One potential issue with my algorithm is that it never pairs a “high” memory Digimon with “low” memory Digimon since it only pairs Digimon together that are adjacent in my list that is sorted by memory. However, I didn’t run into issues with this since it can still find many teams that fit the memory and attack criteria. If the assignment was the find the optimal team, my algorithm may not work as well because it doesn’t actually go through all the possible teams so it may miss a team that has lower  overall memory but higher overall attack. 

Initially, I tried brute forcing the solution to this problem, but this involved a tripple nested loop which isn't very efficient. Although this method misses some viable teams, it is signifcantly more efficient and seems to answer the problem well. Pre sorting the data by memory allows the program to not look through digimon that on their own already exceed the memory limit and don't need to be considered with other digimon. 
