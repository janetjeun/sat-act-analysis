# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

## Problem Statement

For decades, colleges and universities have used standardized tests such as the Scholastic Aptitude Test (SAT) and now the American College Testing (ACT) as a factor in student’s college admissions. However, when colleges and universities — both small and prestigious — announced the opportunity for students to not submit their standardized test scores on the Common Application, universities such as Harvard University saw a 42% increase in college applications, according to an article in the Washington Post ([*source*](https://www.washingtonpost.com/education/2021/04/07/admit-rates-ivy-league-pandemic-test-optional/)).

As colleges and universities switch from test compulsory to test optional - allowing students to decide whether or not they should submit their scores - we are hired by college admission board to **assess the relevancy of SAT and ACT tests.** College admission board are interested in finding out the **whether there are shifts in trends in SAT and ACT participation and scores.** They would also like to know **whether SAT/ACT scores serve as accurate indicators of student success**, such as: how well students will do with college-level course work and how successful they will be after graduation.

## Background

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry. Lately, more and more schools are opting to drop the SAT/ACT requirement for their Fall 2021 applications ([*read more about this here*](https://www.cnn.com/2020/04/14/us/coronavirus-colleges-sat-act-test-trnd/index.html)).

## Datasets

There are 7 datasets used in this project:

* [`act_2017.csv`](./data/act_2017.csv): 2017 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`act_2018.csv`](./data/act_2018.csv): 2018 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`act_2019.csv`](./data/act_2019.csv): 2019 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State ([source](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent))
* [`MERGED2018_19_PP.csv`](./data/MERGED2018_19_PP.csv): 2018-19 College-level data file containing aggregate data information on college enrollment. ([source](https://collegescorecard.ed.gov/data/))

## Dictionaries

1. sat_act datasets

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**State**|*object*|sat_act|U.S. State Name| 
|**SAT_2017_Participation**|*float64*|sat_act|Participation rate of those who took SAT in their state in 2017.| 
|**SAT_2017_Score**|*int64*|sat_act|The total score of those who took SAT in their state in 2017.|
|**SAT_2018_Participation**|*float64*|sat_act|Participation rate of those who took SAT in their state in 2018.| 
|**SAT_2018_Score**|*int64*|sat_act|The total score of those who took SAT in their state in 2018.| 
|**SAT_2019_Participation**|*float64*|sat_act|Participation rate of those who took SAT in their state in 2019.| 
|**SAT_2019_Score**|*int64*|sat_act|The total score of those who took SAT in their state in 2019.| 
|**ACT_2017_Participation**|*float64*|sat_act|Participation rate of those who took ACT in their state in 2017.| 
|**ACT_2017_Score**|*int64*|sat_act|The total score of those who took ACT in their state in 2017.|
|**ACT_2018_Participation**|*float64*|sat_act|Participation rate of those who took ACT in their state in 2018.| 
|**ACT_2018_Score**|*int64*|sat_act|The total score of those who took ACT in their state in 2018..| 
|**ACT_2019_Participation**|*float64*|sat_act|Participation rate of those who took ACT in their state in 2019.| 
|**ACT_2019_Score**|*int64*|sat_act|The total score of those who took ACT in their state in 2019.| 

2. data1819 datasets

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**School**|*object*|data1819|U.S. School Name|
|**State**|*object*|data1819|U.S. State Name|
|**ACT_Score**|*float64*|data1819|Average SAT total score students in college| 
|**SAT_Score**|*float64*|data1819|Average ACT total score students in college| 
|**Retention_Rate**|*float64*|data1819|Average rate of freshman year students who continued on to their sophomore year|
|**Ave_Earning**|*float64*|data1819|Average earning of students 6 years after college| 
|**Graduation_Rate**|*float64*|data1819|Average rate of students who complelted a degree or certification in the college| 

## Summary Findings

**Trends in SAT and ACT participation and scores for the years 2017-2019.**
From 2017-2019 SAT and ACT datasets, it can be inferred that:
1. Generally, there is no significant changes in ACT and SAT minimum scores, maximum scores, and average scores, with the exception of a slight drop in minimum & maximum SAT score from 2018 to 2019.
2. ACT and SAT scores are negatively correlated to each other. Meaning that states with lower SAT scores tend to have higher ACT scores, and vice versa.
3. ACT and SAT results every year has a very strong correlation. The states that did well last year are likely to do well next year. This correlation is much stronger for ACT tests as compared to SAT tests.
4. There are increase in participation rate of SAT test and decrease in participation rate of ACT test over the years.
5. SAT & ACT participation rates has a strong negative correlation with scores. This means that the states with higher SAT/ACT participation tend to have lower SAT scores, and vice versa. It is plausible that in states where SAT/ACT are compulsory, all the participants are required to take the test whether or not they are going to college / university. If students are not planning to go to college / university, they will tend to spend less time in preparation, hence the lower score. Whereas in states that does not make SAT/ACT compulsory, only those that planned to enter college / university will take the tests. Hence, those taking the tests are motivated to do well, and will put in efforts to study and score higher in their exams.

**SAT/ACT scores as accurate indicators of student success**
As there are changes of trends in SAT and ACT participations, are SAT / ACT are still relevant in current day & age?

From 2018-2019 College Enrollment datasets, it can be inferred that students with higher SAT/ACT scores:
1. Have a higher chance of completing their freshman year and progress to their sophomore year
1. Are more likely to complete their courses and graduate
3. Tends to be more successful, measuring from the income level 6 years post graduation

## Recommendations
Although there are a huge demand in making standardized tests as optional, it is undeniable that there are strong correlations between SAT & ACT scores and student success. Hence, college admission board shall continue to make standardized test compulsory during their admission process.

## Further Studies
The recommended further studies to be done are as follows:
1. Current analysis are done using 2017 to 2019 datasets. To analyze 2020 and 2021 datasets to get a more accurate representation of current SAT & ACT Tests
2. Current analysis measures income level 6 years post graduations. A lot of factors might affect income in 6 years, hence, it is recommended to get the income level 1 year post graduation to get a better measurement of student success.
2. To consider more factors in measuring student success, such as: College / University GPA, Academic Achievements (Awards), etc.