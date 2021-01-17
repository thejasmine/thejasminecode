---
layout: post
title:  "AB testing in game — analyzing using Python"
date:   2020-12-20 15:05:55 +0300
image:  '/assets/img/12.png'
tags:   mediumpost
blog:   https://medium.com/analytics-vidhya/ab-testing-in-game-analyze-using-pty-cb82927d8422?source=friends_link&sk=9db300b73a2596d9fd3278cddc9ffb37
skills: Python | Hypothesis Testing | Statistical Analysis
---
 AB testing is a popular way to experiment with changes in websites, games, etc. We can see the result in a short time and make decisions accordingly.
I recently took several statistics thinking using Python courses and a course about designing and analyzing AB testing. As a result, I would like to apply my knowledge to the project.

---
#### Access Full Article <a href="https://medium.com/analytics-vidhya/ab-testing-in-game-analyze-using-pty-cb82927d8422?source=friends_link&sk=9db300b73a2596d9fd3278cddc9ffb37" target="_blank" >here</a>

---
Short Version
### Background& Problem Statement
The Dataset is about the mobile game Cookie Cats pops. At first, players download the game for free. As players progress through the game, they would encounter gates that ask them to wait some amount of time to enter the next game or make purchases to avoid waiting. As a result, the timing of placing gates is an important decision to make.
### The Goal
Currently, the first gate was at level 30. The company wants to know the effect of the first gate at level 30 and level 40. Would the change affect player retention?
### Process
1. Understand the dataset
2. EDA and data visualization
3. Hypothesis testing — bootstrapping
4. Result and business recommendation

Following, I will briefly take about key findings and takeaways of the project. You can access the full project code <a href="https://github.com/thejasmine/ABtesting_game" target="_blank" >here.</a>

### Result
Based on the result of the hypothesis test, there is a significant difference between the two groups. The retention rate for gate 30 is higher than gate 40 for both day one and day seven. The result tells that we can confidently believe that day one and day seven retention rate of version gate 30 is higher than the version of gate 40. In short, the company should not change the gate level to 40.

### Takeaways and recommendations

* The company should not move to gate 40 since 7-day retention is higher when the gate is at level 30.
* The retention rate drops from 44% to 18% within six days. The company should figure a way to maintain their player based. It might be players get bored at day3 or day4 and decide to leave the game. To improve the retention rate for the first week, the company can provide some incentives such as free gifts are add interesting challenges, etc.




