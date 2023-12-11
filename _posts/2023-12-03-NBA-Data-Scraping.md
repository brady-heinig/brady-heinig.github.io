---
layout: post
title:  "Who is the Goat?: How I found my Data"
author: Brady Heinig
description: This is an explanation of how I gound my data to do this project
image: /assets/images/blog-image.jpg
---

Craft a blog post encompassing:
- Introduction and motivation for your chosen topic and research question.
- A description of how data was collected and cleaned.
- An explanation of the ethical considerations and measures taken during web scraping.
- A concluding statement.
- Provide a link to the data and code repository in your blog post.
  
 The King vs. His Airness

This is a debate that has graced many barbershops for the last few years, and it doesn't show any sign of slowing down. Michael Jordan cemented himself as an all-time great by winning 6 championships with the Chicago Bulls, while also changing the way the game was played. People claimed we would never see a player that came close to Jordan's greatness. Enter Lebron James. Coming into the NBA as an 18 year old kid, Lebron lived up to lofty expectations by winning 4 championships with 3 different teams and breaking the NBA scoring record that had long been considered untouchable. Jordan left his legcay decades ago, while Lebron continues to play at a high level in the league at the age of 39! I am not old enough to have watched both players dominate in their eras, but I want to dive into the statistics that will tell me each player's story in an attempt to answer the burning question: Who is the greatest basketball player of all time

###How do we quantify Greatness?

Basic basketball statistics are available in excess across the internet, but I was curious in also looking at the advanced statistics that would give me a deeper understanding of how these players dominated in their own ways. Basketball-Reference (pictured below) is a great website that has a plethora of advanced analytics on every player that has graced an NBA court. Basketball-Reference does not have a public API, they just ask that any scraped data is not used in projects that will be for a user's profit. Because I fit this criteria, and the data for each player is publicly available, I saw no ethical problems concerning my project and moved forward with it. The website includes pages that have datatables with basic and advanced statistics for both Lebron and MJ in their regular season and playoff careers. I was interested in looking at both players dominance at an individual game level and also when zooming out and looking at seasons as a whole. The tricky part about the structure of this website is that the data for each season is located on a different page. This required some adjustments on my part in order to properly collect the data.

In order to obtain the needed statistics, I used a webscraper built with the BeautifulSoup package in python. This scraper looped through the years that each player was active in the NBA, and the resulting dataframe has entries for every single game that each player has played in their NBA careers with accompanying basic and advanced statistics. Along with common stats like Points, Rebounds, and Feild Goal %, this dataset includes advanced stats like Usage %, Effective Field Goal %, and Box Plus Minus, which allow us to analyze their performance from a game as a whole.

Once I had the data in hand, I began the EDA process in order to glean some visual insight that might solve this debate for me (you can read my article where I dive into that process <a href="https://github.com/brady-heinig/brady-heinig.github.io/blob/main/nba_salary_regression.ipynb" target="_blank">here </a>). All of the code I used to scrape Basketball-Reference.com can be in my repository here in case you would like to try a similar idea. Make sure to stay up to date with me as I settle the most heated debate in the basketball world by using advanced metrics.

Source code for the project if you want to follow along can be found <a href="https://github.com/brady-heinig/brady-heinig.github.io/blob/main/nba_salary_regression.ipynb" target="_blank">here </a>
### **Load in the Data**
- The data we are using comes from an NBA dataset found publicly on kaggle.
- The dataset includes every player who logged a minute in an NBA game this year, and it includes all basic stats including points per game,     rebounds per game, assists per game, etc. Advanced stats are also included for each player.
<img src="{{https://brady-heinig.github.io}}/assets/images/dataset.png"/>
