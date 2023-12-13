---
layout: post
title:  "Who is the Goat?"
author: Brady Heinig
description: A detailed explanation of how I found and cleaned the data needed to answer this question
image: /assets/images/mj_vs_lebron.png
---  
The King vs. His Airness

This is a debate that has graced many barbershops for the last few years, and it doesn't show any sign of slowing down. Michael Jordan cemented himself as an all-time great by winning 6 championships with the Chicago Bulls, while also changing the way the game was played. People claimed we would never see a player that came close to Jordan's greatness. Enter Lebron James. Coming into the NBA as an 18 year old kid, Lebron lived up to lofty expectations by winning 4 championships with 3 different teams and breaking the NBA scoring record that had long been considered untouchable. Jordan left his legcay decades ago, while Lebron continues to play at a high level in the league at the age of 39! I am not old enough to have watched both players dominate in their eras, but I want to dive into the statistics that will tell me each player's story in an attempt to answer the burning question: Who is the greatest basketball player of all time

### **How do we quantify Greatness?**

Basic basketball statistics are available in excess across the internet, but I was curious in also looking at the advanced statistics that would give me a deeper understanding of how these players dominated in their own ways. Basketball-Reference (pictured below) is a great website that has a plethora of advanced analytics on every player that has graced an NBA court. Basketball-Reference does not have a public API, they just ask that any scraped data is not used in projects that will be for a user's profit. Because I fit this criteria, and the data for each player is publicly available, I saw no ethical problems concerning my project and moved forward with it. The website includes pages that have datatables with basic and advanced statistics for both Lebron and MJ in their regular season and playoff careers. I was interested in looking at both players dominance at an individual game level and also when zooming out and looking at seasons as a whole. The tricky part about the structure of this website is that the data for each season is located on a different page. This required some adjustments on my part in order to properly collect the data.

<img src="{{https://brady-heinig.github.io}}/assets/images/bball_ref.png"/>

In order to obtain the needed statistics, I used a webscraper built with the BeautifulSoup package in python. This scraper looped through the years that each player was active in the NBA, and the resulting dataframe has entries for every single game that each player has played in their NBA careers with accompanying basic and advanced statistics. Along with common stats like Points, Rebounds, and Feild Goal %, this dataset includes advanced stats like Usage %, Effective Field Goal %, and Box Plus Minus, which allow us to analyze their performance from a game as a whole.

### **Stay Up to Date With Me**
Once I had the <a href="https://github.com/brady-heinig/final_proj/blob/main/goat.csv" target="_blank">data </a> in hand, I began the EDA process in order to glean some visual insight that might solve this debate for me (you can read my article where I dive into that process <a href="https://brady-heinig.github.io/2023/12/09/NBA-EDA.html" target="_blank">here </a>). All of the code I used to scrape Basketball-Reference.com can be found in my repository <a href="https://github.com/brady-heinig/final_proj/blob/main/final_project.ipynb" target="_blank">here </a> in case you would like to try a similar idea. Make sure to stay up to date with me as I settle the most heated debate in the basketball world by using advanced metrics.

