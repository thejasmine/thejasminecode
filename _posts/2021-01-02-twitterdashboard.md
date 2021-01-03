---
layout: post
title:  A Twitter dashborad | Builing ETL pipline
date:   2021-01-02 13:05:55 +0300
image:  '/assets/img/twitter.jpg'
tags:   testing
blog:   https://thejasmine.medium.com/how-i-built-a-twitter-dashboard-4d5d0e53c36c
---

For this project,I use Python to extract data from Twitter API and stream them into the PostgreSQL database, perform sentiment analysis and further build a dashboard using Tableau to track the weekly trends.

---

### Background
As a data analyst, I am curious about what people say on Twitter, how often they tweet, people’s attitudes toward specific hashtags, etc. Twitter API provides us an easy way to retrieve tweets about specific keywords and hashtags. In other words, I can utilize the tool to analyze any topics I am interested in.
I have been involved in the MakeoverMonday project for months. MakeoverMonday is a social data project that each week rework a chart, retell a story more effectively, or even find more interesting insights. It has been my favorite project in 2020. The community would share their thoughts on Twitter and interact with other members. As a result, I am interested to learn more from hashtag #makeovermonday.

### Goal
This project aims to build an automatic ETL pipeline that allows me easily to update the dashboard every Monday. For this reason, I choose to store the data in the Postgresql database, which I can store every week’s new data and load to Tableau. Besides, I want to write a script that I can reuse for different hashtags and keywords.

### Process

#### I have share my process in <a href="https://thejasmine.medium.com/how-i-built-a-twitter-dashboard-4d5d0e53c36c" target="_blank" > Medium post.</a>

### Some insights💡
Based on data from 2020/12/22 to 2021/01/02.


Not surprisingly, people like to post on Monday since that is the day supposed to do the project. I like to finish my project on Monday as well since it can force me to be productive.
95% of the tweets are positive or natural. People are happy to share their works and give positive feedback.

