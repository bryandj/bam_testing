# From Plan A to The NBA

## Description

This project is an exploritory data analysis using NBA Combine assessment data from High School & Division 1 athletes who are trying to get to the next level. The purpose of this project is to identify:

1) Which NBA Combine assessment is the biggest delineator for athletes that make it to the next level?
2) How do athletes identify their strengths and weaknesses + how do they improve upon them?


Today, the probability of competing in athletics beyond high school is extremely slim. In fact, only 3.5% of high school basketball athletes end up competing at the college level. With such a slim chance of high school athletes making it to the next level, student athletes are beginning to plan, prepare and train younger and younger.

With this in mind, student athletes need to begin understanding how they compare to the competition. In order to get to that next level, student athletes need to be elite/above the rest and players/coaches need insight into their areas of improvement to help athletes reach the next level.

So how are players/coaches going to figure out areas of improvement, track progress, and understand their athletic strengths and weaknesses? Well I have the answer for you! 

Let me introduce you to BAM TESTING!

BAM Testing created a standardized athletic performance assessment to provide quantitative evidence to quantitatively measure how athletes compare to the rest of the competition. With this quantitative data, BAM draws insight into athletes strengths and weaknesses through the BAM Score - A standardized assessment for critical insight into athletic strengths and weaknesses.

What makes a good BAMScore?

Example of BAMScore
<img src="images/Bamscore.png"/>


## Definition of NBA Combine Protocols and Anthros

bamid
- Number randomly assigned to each athlete without knowing full name

bamscore
- Single Numerical Value that measures and benchmarks athletic performence
- "Athletic SAT Score"
- Standardized athletic assessment that gives coaches insight into where players need improvement

## Protocols (Athletic Tests)
approach_vertical
- running start, jump as high as you can

vertical_jump
- stationary start, jump as high as you can

three_quarter_court_sprint
- 75 ft straight sprint

four_way_agility
- run arouund 4 points in box, run back through

reaction_shuttle
- agility test - start in middle of box, run left, right, run back and finish through left line          

## Anthros (Body Measurements)
wingspan
- horizontal distance from arms extended side to side

reach
- standing vertical reach

height
- how tall you are in inches

weight
- how much you weigh in pounds

body_comp
- body fat (varies in measurement methods)

hand_length
- vertical length of hand

hand_width
- horizontal length of hand

### # 1 Import Libraries
- Pandas, NumPy, Matplotlib, SciPy, Seaborn, Plotly, Scikit-learn
<img src="images/Libraries.png"/>

### # 2 Import & Clean Data
- Dropped Hand Length and blank columns messing up data
- Identified NAN's and blank columns then filled and replaced with means

<img src="images/clean_data.png"/>

### # 3 Visualize
- Plotted ranks of all protocols and anthros to see distribution
- Plotted to find more outliers/data that did not make sense

<img src="images/av_rank.png"/>

### # More Visualization - Violin Plots
- Created 2 similar violin plots for each parameter with respect to BAMScore

<img src="images/violin_plot.png"/>
<img src="images/rs_violin.png"/>

### # 4 More cleaning + scaling training data
- Removed outliers
- Scaled training data

<img src="images/clean_4_way.png"/>
<img src="images/clean_4_way_1.png"/>

### # 5 Created OLS Regression Model
- Goal: figure out most important features in model

### #6 Iterated Model and added random forrest model

### # 7 Feature Importance Analysis
- Reaction Shuttle is the most important feature and highest delineator for rank

<img src="images/feature.png"/>

- Plotted reaction shuttle with respect to BAMScore

<img src="images/lmplot_reaction_shuttle.png"/>

#### Feature Importance Results
- .53 r2 test and .63 train

### # 8 Scatter Matrix
- Created scatter matrix across all ranked columns to try and visualize more trends by looking for 45 degree patterns

<img src="images/scatter.png"/>


### # 13 Conclusion and Insight
- Vertical jump is not important for delineating BAMScores
- Reaction shuttle and 4-Way agility are the most important protocols that delineate BAMScores
- Overall On average, shorter athletes have better scores (except vertical jump and approach vertical)
- Shorter athletes are much better at agility/fast twitch based protocols


## Future Work
- add more iterations to models
- spend time with more important features
- test it via classifier instead