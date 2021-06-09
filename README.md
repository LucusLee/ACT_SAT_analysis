# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: ACT & SAT Standardized Test Analysis

### Problem Statement

The new format for the SAT was released in March 2016. There have been several important changes such as 'a new scoring system', 'removal of penalization', 'reduction in number of questions', 'essay writing to be optional', etc. This project aims to explore the revised SAT performance as compared to ACT for the years 2017-2020 and if the changes have improved the participation rate for the standardization test.

### Contents:
- [Background](#Background)
- [External Research](#External-Research)
- [Data Dictionary](#Data-Dictionary)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Executive Summary](#Executive-Summary)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)

### Background

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, SAT:(400-600) and ACT: (1-36)
* [SAT Score Range](https://en.wikipedia.org/wiki/SAT)
* [ACT Score Range](https://en.wikipedia.org/wiki/ACT_(test))

On March 5, 2014, the College Board announced its plan to redesign the SAT in order to link the exam more closely to the work high school students encounter in the classroom. The new exam was administered for the first time in March 2016. Some of the major changes were: an emphasis on the use of evidence to support answers, a shift away from obscure vocabulary to words that students are more likely to encounter in college and career, an optional essay, questions having four rather than five answer options, and the removal of penalty for wrong answers (rights-only scoring).The scope of mathematics content was narrowed to include fewer topics, including linear equations, ratios, and other precalculus topics. The essay score was separated from the final score, and institutions could choose whether or not to consider it. As a result of these changes, the highest score was returned to 1600. These modifications were the first major redesign to the structure of the test since 2005. As the test no longer deducts points for wrong answers, the numerical scores and the percentiles appeared to have increased after the new SAT was unveiled in 2016. However, this does not necessarily mean students came better prepared.

To combat the perceived advantage of costly test preparation courses, the College Board announced a new partnership with Khan Academy to offer free online practice problems and instructional videos.

* [SAT 2016 Changes](https://en.wikipedia.org/wiki/SAT#2016_changes,_including_the_return_to_a_1600-point_score)

Many students and parents begin the college prep process by comparing the ACT and SAT tests. The SAT and ACT generally cover the same topics. Both ACT and SAT scores are used for college admissions decisions and awarding merit-based scholarships. Most colleges do not prefer one test over the other. Neither the SAT or ACT is harder than the other. Different students tend to do better on one test over the other.

* [SAT vs ACT](https://www.princetonreview.com/college/sat-act)


### Datasets

These are the datasets used in this project

* [`act_2017.csv`](./data/act_2017.csv): 2017 ACT Scores and participation rate by State
* [`act_2018.csv`](./data/act_2018.csv): 2018 ACT Scores and participation rate by State
* [`act_2019.csv`](./data/act_2019.csv): 2019 ACT Scores and participation rate by State
* [`act_2020.csv`](./data/act_2020.csv): 2020 ACT Scores and participation rate by State
* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores and participation rate by State
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores and participation rate by State
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores and participation rate by State
* [`sat_2020.csv`](./data/sat_2020.csv): 2020 SAT Scores and participation rate by State
---

### External Research

There are several states that have made ACT/SAT mandatory as college admissions test are being used to meet national standards required of public school.

These are the states that have mandatory requirements for individual tests:

|ACT|SAT|
|---|---|
|Alabama|Colorado|
|Arkansas|Connecticut|
|Kentucky|Delaware|
|Louisiana|Idaho|
|Mississippi|Illinois|
|Montana|Maine|
|Nebraska|Michigan|
|Nevada|New Hampshire|
|North Carolina|Rhode Island|
|North Dakota|West Virginia|
|Utah||
|Wisconsin|
|Wyoming

The listed state will be filtered during some of the participation rate related EDA.

* [States that required the ACT or SAT](https://magoosh.com/hs/sat/states-that-require-the-act-or-sat/)
* [List of statewide administration of ACT/SAT](https://www.ecs.org/wp-content/uploads/State-Information-Request_Use-of-ACT-SAT-and-PSAT-for-High-School-Testing-as-Required-by-ESSA.pdf)


2016 SAT dataset was not chosen for this project because state reports contains information on students who took the old SAT or SAT subject tests at least once through January 2016, the last time the old SAT was administered.

* [2016 SAT state reports containing both formats](https://reports.collegeboard.org/archive/sat-suite-program-results/2016/class-of-2016-results/state-reports)

The average SAT score dipped for this year’s high school graduates, according to results released Tuesday, even as more students nationwide are taking the college admission exam through publicly funded testing during the school day.

The class of 2019 scored an average of 531 on evidence-based reading and writing and 528 on math. Their combined 1059, out of a maximum 1600, was 9 points lower than what the previous class posted. But fluctuations in results are common when the population of test-takers is also in flux.

That has been especially true for the SAT since a redesigned version of the three-hour exam was launched in 2016.

* [Negative correlation for SAT scores and participation](https://www.washingtonpost.com/local/education/sat-scores-drop-for-2019-class-but-participation-rises-through-testing-in-schools/2019/09/23/332fc4d0-de11-11e9-8dc8-498eabc129a0_story.html)

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
**state**|object|final_merged_data_2017_to_2020|The 50 States of America|
**sat_participation_17**|float64|final_merged_data_2017_to_2020|SAT's average participation rate for the year 2017|
**sat_total_average_17**|int64|final_merged_data_2017_to_2020|SAT's total average score for the year 2017|
**act_participation_17**|float64|final_merged_data_2017_to_2020|ACT's average participation rate for the year 2017|
**act_total_average_17**|float64|final_merged_data_2017_to_2020|ACT's total average score for the year 2017|
**sat_participation_18**|float64|final_merged_data_2017_to_2020|SAT's average participation rate for the year 2018|
**sat_total_average_18**|int64|final_merged_data_2017_to_2020|SAT's total average score for the year 2018|
**act_participation_18**|float64|final_merged_data_2017_to_2020|ACT's average participation rate for the year 2018|
**act_total_average_18**|float64|final_merged_data_2017_to_2020|ACT's total average score for the year 2018|
**sat_participation_19**|float64|final_merged_data_2017_to_2020|SAT's average participation rate for the year 2019|
**sat_total_average_19**|int64|final_merged_data_2017_to_2020|SAT's total average score for the year 2019|
**act_participation_19**|float64|final_merged_data_2017_to_2020|ACT's average participation rate for the year 2019|
**act_total_average_19**|float64|final_merged_data_2017_to_2020|ACT's total average score for the year 2019|
**sat_participation_20**|float64|final_merged_data_2017_to_2020|SAT's average participation rate for the year 2020|
**sat_total_average_20**|float64|final_merged_data_2017_to_2020|SAT's total average score for the year 2020|
**act_participation_20**|float64|final_merged_data_2017_to_2020|ACT's average participation rate for the year 2020|
**act_total_average_20**|float64|final_merged_data_2017_to_2020|ACT's total average score for the year 2020|



### Exploratory Data Analysis


**Highest 10 participation rate:**

(Not accounting for states with mandatory requirement to either of the test and no hiarachy among states with 100% participation rate)

|Year|Test|State 1|State 2|State 3|State 4|State 5|State 6|State 7|State 8|State 9|State 10|National|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|2017|ACT|Minnesota: 100%|Oklahoma: 100%|Colorado: 100%|Tennessee: 100%|Missouri: 100%|South Carolina: 100%|Illinois: 93%|Hawaii: 90%|South Dakota: 80%|Ohio: 75%|60%|
|2017|SAT|District of Columbia: 100%|Florida: 83%|Massachusetts: 76%|New Jersey: 70%|Maryland: 69%|New York: 67%|Virginia: 65%|Pennsylvania: 65%|Washington: 64%|Indiana: 63%|38%|
|2018|ACT|Missouri: 100%|Ohio: 100%|Oklahoma: 100%|South Carolina: 100%|Tennessee: 100%|Minnesota: 99%|Hawaii: 89%|South Dakota: 77%|Kansas: 71%|Iowa: 68%|66%|
|2018|SAT|District of Columbia: 92%|New Jersey: 82%|Massachusetts: 80%|New York: 79%|Maryland: 76%|Georgia: 70%|Pennsylvania: 70%|Washington: 69%|Virginia: 68%|Texas: 68%|52%|
|2019|ACT|Ohio: 100%|Oklahoma: 100%|Tennessee: 100%|Minnesota: 95%|Missouri: 82%|Hawaii: 80%|South Carolina: 78%|South Dakota: 75%|Arizona: 73%|Kansas: 72%|52%|
|2019|SAT|Florida: 100%|District of Columbia: 94%|Maryland: 82%|New Jersey: 82%|Massachusetts: 81%|New York: 79%|Georgia: 71%|Pennsylvania: 70%|Washington: 70%|South Carolina: 68%|54%|
|2020|ACT|Ohio: 100%|Oklahoma: 100%|Tennessee: 100%|Minnesota: 92%|Hawaii: 82%|Kansas: 82%|Missouri: 78%|South Carolina: 76%|Arizona: 71%|South Dakota: 70%|49%|
|2020|SAT|District of Columbia: 100%|Florida: 100%|Maryland: 88%|New Jersey: 82%|Massachusetts:	80%|New York: 79%|Texas: 73%|Washington: 69%|Georgia: 68%|South Carolina: 68%|51%|


**Lowest 10 participation rate:**

(Not accounting for states with mandatory requirement to either of the test)

|Year|Test|State 1|State 2|State 3|State 4|State 5|State 6|State 7|State 8|State 9|State 10|National|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|2017|ACT|Maine: 8%|Delaware: 18%|New Hampshire: 18%|Rhode Island: 21%|Pennsylvania: 23%|Maryland: 28%|Michigan: 29%|Vermont: 29%|Virginia: 29%|Washington: 29%|60%|
|2017|SAT|Iowa: 2%|Mississippi: 2%|North Dakota: 2%|Wyoming: 3%|Utah: 3%|Arkansas: 3%|Minnesota: 3%|Missouri: 3%|Wisconsin: 3%|Nebraska: 3%|38%|
|2018|ACT|Maine: 7%|Rhode Island: 15%|New Hampshire: 16%|Delaware: 17%|Pennsylvania: 20%|Michigan: 22%|Virginia: 24%|Vermont: 24%|Washington: 24%|Massachusetts: 25%|66%|
|2018|SAT|North Dakota: 2%|Wyoming: 3%|Iowa: 3%|Mississippi: 3%|Wisconsin: 3%|Nebraska: 3%|South Dakota: 3%|Utah: 4%|Kansas: 4%|Kentucky: 4%|52%|
|2019|ACT|Maine: 6%|Rhode Island: 12%|Delaware: 13%|New Hampshire: 14%|Pennsylvania: 17%|Michigan: 19%|Vermont: 20%|Massachusetts: 21%|Virginia: 21%|Connecticut: 22%|52%|
|2019|SAT|North Dakota: 2%|Nebraska: 3%|South Dakota: 3%|Wisconsin: 3%|Mississippi: 3%|Wyoming: 3%|Iowa: 3%|Kentucky: 4%|Minnesota: 4%|Missouri: 4%|54%|
|2020|ACT|Maine: 5%|Delaware: 11%|Rhode Island: 11%|New Hampshire: 12%|Pennsylvania: 15%|Michigan: 17%|Massachusetts: 18%|Virginia: 19|Connecticut: 19%|Maryland: 19%|49%|
|2020|SAT|Wyoming: 2%|North Dakota: 2%|Utah: 3%|South Dakota: 3%|Wisconsin: 3%|Mississippi: 3%|Nebraska: 3%|Iowa: 3%|Minnesota: 4%|Kansas: 4%|51%|

**Highest 10 average total scores:**

|Year|Test|State 1|State 2|State 3|State 4|State 5|State 6|State 7|State 8|State 9|State 10|National|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|2017|ACT|New Hampshire: 25.5|Massachusetts: 25.4|Connecticut: 25.2|Maine: 24.3|District of Columbia: 24.2|New York: 24.2|Michigan: 24.1|Delaware: 24.1|Rhode Island: 24.0|New Jersey: 23.9|21.0
|2017|SAT|Minnesota: 1295|Wisconsin: 1291|Iowa: 1275|Missouri: 1271|Kansas: 1260|North Dakota: 1256|Nebraska: 1253|Kentucky: 1247|Mississippi: 1242|Utah: 1238|1107|
|2018|ACT|Connecticut: 25.6|Massachusetts: 25.5|New Hampshire: 25.1|New York: 24.5|Rhode Island: 24.2|Michigan: 24.2|Vermont: 24.1|Maine: 24.0|Virginia: 23.9|Illinois: 23.9|21.3|
|2018|SAT|Minnesota: 1298|Wisconsin: 1294|North Dakota: 1283|Kansas: 1265|Iowa: 1265|Missouri: 1262|Wyoming: 1257|Nebraska: 1252|Kentucky: 1248|South Dakota: 1240|1098|
|2019|ACT|Connecticut: 25.5|Massachusetts: 25.5|New Hampshire: 25.0|Rhode Island: 24.7|New York: 24.5|Michigan: 24.4|Illinois: 24.3|Maine: 24.3|New Jersey: 24.2|Delaware: 24.1|20.7|
|2019|SAT|Minnesota: 1284|Wisconsin: 1283|South Dakota: 1268|North Dakota: 1263|Nebraska: 1260|Iowa: 1244|Kansas: 1241|Wyoming: 1238|Mississippi: 1237|Missouri: 1236|1097|
|2020|ACT|Massachusetts: 26.0|Connecticut: 25.9|New Hampshire: 25.7|New York: 24.9|Maine: 24.9|Rhode Island: 24.8|Illinois: 24.7|Michigan: 24.6|Virginia: 24.4|New Jersey: 24.4|20.6|
|2020|SAT|Minnesota: 1257|Wisconsin: 1243|Kansas: 1237|North Dakota: 1231|Nebraska: 1229|Wyoming: 1220|Iowa: 1220|South Dakota: 1218|Missouri: 1212|Kentucky: 1207|1095|

**Lowest 10 average total scores:**

|Year|Test|State 1|State 2|State 3|State 4|State 5|State 6|State 7|State 8|State 9|State 10|National|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|2017|ACT|Nevada: 17.8|Mississippi: 18.6|South Carolina: 18.7|Hawaii: 19.0|North Carolina: 19.1|Alabama: 19.2|Arkansas: 19.4|Oklahoma: 19.4|Louisiana: 19.5|Arizona: 19.7|21.0|
|2017|SAT|District of Columbia: 950|Delaware: 996|Michigan: 1005|Idaho: 1005|Maine: 1012|Florida: 1017|Texas: 1020|Connecticut: 1041|Oklahoma: 1047|Georgia: 1050|1107|
|2018|ACT|Nevada: 17.7|South Carolina: 18.3|Mississippi: 18.6|Hawaii: 18.9|North Carolina: 19.1|Alabama: 19.1|Louisiana: 19.2|Arizona: 19.2|Oklahoma: 19.3|Arkansas: 19.4|21.3|
|2018|SAT|District of Columbia: 977|Delaware: 998|West Virginia: 999|Idaho: 1001|Utah: 1010|Hawaii: 1010|Michigan: 1011|Maine: 1013|Rhode Island: 1018|Illinois:1019|1098|
|2019|ACT|Nevada: 17.9|Mississippi: 18.4|South Carolina: 18.8|Louisiana: 18.8|Oklahoma: 18.9|Alabama: 18.9|Arizona: 19.0|Hawaii: 19.0|North Carolina: 19.0|Arkansas: 19.3|20.7|
|2019|SAT|West Virginia: 943|Oklahoma: 963|District of Columbia: 975|Delaware: 985|Idaho: 993|Rhode Island: 995|Florida: 999|Michigan: 1003|Illinois: 1013|Maine: 1013|1097|
|2020|ACT|Nevada: 17.9|Mississippi: 18.2|South Carolina: 18.4|Hawaii: 18.5|Oklahoma: 18.7|Louisiana: 18.7|North Carolina: 18.8|Alabama: 18.8|Arkansas: 19.0|Arizona	19.1|20.6|
|2020|SAT|West Virginia: 936|Oklahoma: 971|Delaware: 978|District of Columbia: 979|Idaho: 984|Rhode Island: 990|Florida: 992|Maine: 995|Michigan: 998|Illinois: 1007|1095|


**States with 100% participation rate for SAT in either years(2017-2020)**

|State|2017 Participation Rate|2018 Participation Rate|2019 Participation Rate|2020 Participation Rate|
|---|---|---|---|---|
|Colorado|11%|100%|100%|100%|
|Connecticut|100%|100%|100%|100%|
|Delaware|100%|100%|100%|100%|
|District of Columbia|100%|92%|94%|100%|
|Florida|83%|56%|100%|100%|
|Idaho|93%|100%|100%|100%|
|Illinois|9%|99%|100%|98%|
|Michigan|100%|100%|100%|100%|
|Rhode Island|71%|97%|100%|100%|


**States with 100% participation rate for ACT in either years(2017-2020)**

|State|2017 Participation Rate|2018 Participation Rate|2019 Participation Rate|2020 Participation Rate|
|---|---|---|---|---|
|Alabama|100%|100%|100%|100%|
|Arkansas|100%|100%|100%|100%|
|Colorado|100%|30%|27%|25%|
|Kentucky|100%|100%|100%|100%|
|Louisiana|100%|100%|100%|100%|
|Minnesota|100%|99%|95%|92%|
|Mississippi|100%|100%|100%|100%|
|Missouri|100%|100%|82%|78%|
|Montana|100%|100%|100%|100%|
|Nebraska|84%|100%|100%|100%|
|Nevada|100%|100%|100%|100%|
|North Carolina|100%|100%|100%|100%|
|Ohio|75%|100%|100%|100%|
|Oklahoma|100%|100%|100%|100%|
|South Carolina|100%|100%|78%|76%|
|Tennessee|100%|100%|100%|100%|
|Utah|100%|100%|100%|100%|
|Wisconsin|100%|100%|100%|100%|
|Wyoming|100%|100%|100%|100%|

**States that have above 50% Participation on both test for 2017**

|State|ACT Participation Rate|SAT Participation Rate|
|---|---|---|
|Florida|73%|83%|
|Georgia|55%|61%|
|Hawaii|90%|55%|

**States that have above 50% Participation on both test for 2018**

|State|ACT Participation Rate|SAT Participation Rate|
|---|---|---|
|Florida|66%|56%|
|Georgia|53%|70%|
|Hawaii|89%|56%|
|North Carolina|100%|52%|
|South Carolina|100%|55%|

**States that have above 50% Participation on both test for 2019**

|State|ACT Participation Rate|SAT Participation Rate|
|---|---|---|
|Florida|54%|100%|
|Hawaii|80%|54%|
|North Carolina|100%|51%|
|South Carolina|78%|68%|

**States that have above 50% Participation on both test for 2020**

|State|ACT Participation Rate|SAT Participation Rate|
|---|---|---|
|Hawaii|82%|51%|
|South Carolina|76%|68%|


### Executive Summary

First the problem statement was derived to analyse if the performance of the revised SAT test may improved the participation rate throughout the years. Data for both SAT and ACT between 2017 and 2020 were imported via Pandas (a software library for Python), followed by data cleaning. During data cleaning, the dataset were formatted to the right data types and also removed any duplicated or missing data. When data cleaning has been done for all the datasets, it was merged into a single file. The merged file will be used to conduct an EDA (Exploratory Data Analysis) to do statistics summary and investigate trends. Statistics summary and trends findings will be
visualize using diagrams.

The diagrams used in this analysis are:

    1. Box and whisker diagram for the comparison between the total average scores of both tests
    2. Bar chart to display any upward or downward trends on participation rates
    3. Histograms to show dive deeper into each bar chart (how are they distributed)
    4. Heatmap to identify correlation of the dataset
    5. Scatterplot to magnify the correlation between two variables

Once visualization was completed, some of the key findings found:

    1. States with participation rate of 80% and above has also increased over the years.
    2. Median scores were moving into a downward trend for both SAT & ACT over the years.
    3. Strong negative correlation was found between both tests results.



### Conclusions and Recommendations

Starting with SAT’s average scores, most of states are scoring above the median score throughout the years. However, both maximum and minimum score for the SAT seems to be moving in a downward trend ending with 1257 and 936 respectively for year 2020. On the other hand, ACT seems to be moving in an upward trend for their maximum and minimum score over the years ending with 26.0 and 17.9.  This may create a wrong impression to students and parents that SAT are getting tougher over the years which may influence their choice on which test to select.

SAT Participation rate has been increasing since 2017 with currently 19 states that have participation rate at 20% and below and 15 states with participation rate at 80% and above. Compared to 2017 which was 23 and 8 states respectively, this shows that there are more states taking the SAT over the years.

There is a negative correlation of approximate -0.8 between population rate and total average score, what this means is that the lower the population rate, it’s more likely that states will return a high average score. A reason for this would be that states with high participation rate would have their average scores being diluted with the large amount of students and states that have low participation rate will have majority of the applicants that are ready and confident to take the test and hence scoring better in the test.

In conclusion, SAT average scores does not have a direct impact to the participation rate. To achieve a higher participation rate, my recommendation would be to have more resources to be allocated to schools to strengthen preparation. This can improve the median scores for highly participated state and also garner confidence of students to take up the SAT in lower participated states.
