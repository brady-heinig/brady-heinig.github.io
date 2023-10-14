---
layout: post
title: "Using MLR to Predict 2023 Heisman Winner"
author: Brady Heinig
description: "I'm Going to Predict the Heisman"
---
## Steps for creating a new post.  

* Create a new file in the `_posts` folder called `YYYY-MM-DD-post-name.md`, where YYYY is the year (2023), MM numeric month (01-12), and DD is the numeric day of the month (01-31).  The `post-name` is a short name for the new post with `-` between words.  **You must use this name convention for all new posts.**  

*  Make the YML heading.

'''
import pandas as pd
import numpy as np
import seaborn as sns

# Load data on player stats and salaries
df = pd.read_csv('../Downloads/nba_2022-23_all_stats_with_salary.csv', index_col=0)

# Replace with null values with zeros
na_cols = ['FT%', '3P%', '2P%', 'eFG%', 'FG%',  '3PAr', 'FTr', 'TOV%', 'TS%']
df[na_cols] = df[na_cols].fillna(0)

df.head()
'''
