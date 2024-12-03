---
layout: distill
permalink: /portfolio/
title: portfolio
description: A set of industry oriented examples with all the tools that I have dominated.
date: March 2022
category: work
importance: 2
img: assets/img/portfolio.png
bibliography: portfolio.bib
toc:
  - name: The case study
    # if a section has subsections, you can add them as follows:
    # subsections:
    #   - name: Example Child Subsection 1
    #   - name: Example Child Subsection 2
  - name: Data Analytics
  - name: Data Science
  - name: References
---

__My full resume can be found [here](/resume).__

The topic of my portfolio is part of the final capstone project of my [Google Data Analytics Professional Certificate](https://www.credly.com/badges/881f262f-7e69-416e-b82d-122b74471ec6/public_url). While the project had specific goals, I went beyond them, and I used them to demonstrate my analytical skills and the tools that I dominate.

## The case study

[Bellabeat](https://bellabeat.com/) is a high-tech manufacturer of health-focused products for women, and they can become a more prominent player in the global smart device market. The Chief Creative Officer of Bellabeat believes that analyzing smart device fitness data could help unlock new growth opportunities for the company. The goal is to focus on one of Bellabeat's products and analyze smart device data to understand how consumers use their smart devices. These insights will then help guide the marketing strategy for the company.

## Data Analytics

The data analytics process that I followed, as suggested by Google, is described step-by-step in this set of log files: [Ask](https://github.com/alefisico/GoogleCapstoneBellabeat/blob/main/docs/ask.md), [Prepare](https://github.com/alefisico/GoogleCapstoneBellabeat/blob/main/docs/prepare.md), [Process](https://github.com/alefisico/GoogleCapstoneBellabeat/blob/main/docs/process.md), [Analyze](https://github.com/alefisico/GoogleCapstoneBellabeat/blob/main/docs/analyze.md), [Share](https://github.com/alefisico/GoogleCapstoneBellabeat/blob/main/docs/share.md), [Act](https://github.com/alefisico/GoogleCapstoneBellabeat/blob/main/docs/act.md).

In short, I am using three different datasets that I called: `Fitabase` (Fitbit information from 30 individuals)[1], `AppleWatchFitbit` (information from two smart devices from 23 men and 26 women)[2], and `FitbitGrades` (Fitbit information from 400 college students, including grades)[3]. The following table can guide you through the different topics, the notebooks, and the collection of tools used.

| Tools used                                 | Goals                                           | Code/Notebooks/Links          |
|---------------------------------|-------------------------------------------------|------------------------------------------|
| `Bigquery`, `SQL`, `Python`, `Pandas`, `Matplotlib`, `Seaborn` | Study the overall behavior of Fitbit consumers using the Fitabase dataset. |{::nomarkdown}<ul><li> Cleaning data: <a href="https://www.kaggle.com/aleespinosa/fitabase-dataset-cleaning-capstone-bellabeat">Link to Kaggle</a> </li><li> Analyze data: <a href="https://www.kaggle.com/aleespinosa/fitabase-dataset-analyzing-capstone-bellabeat">Link to Kaggle</a> </li></ul>{:/}|
| `R`, `Tidyverse`, `ggplot2` | Study the behavior of Apple watch consumers using the AppleWatchFitbit dataset. Study differences between women and men consumers. | {::nomarkdown}<ul><li>Cleaning and Analyzing data: <a href="https://www.kaggle.com/aleespinosa/google-capstone-project-in-r-bellabeat">Link to Kaggle</a></li></ul>{:/} |
| `Spreadsheets`, `Pivot tables` | Study behavior of women/men Fitbit costumers related with their intellectual skills. | {::nomarkdown}<ul><li>Cleaning and Analyzing data: <a href="https://docs.google.com/spreadsheets/d/1zigDuu3XxDAbuZac-vhzvmmE9q8ApM4BV5-ac1WcpEo/edit?usp=sharing">Link to Google Sheets</a></li></ul>{:/} |
| `Tableau`, `dashboards` | Summarize and emphasize the previous findings using BI tools. | {::nomarkdown}<ul><li>Fitabase viz: <a href="https://public.tableau.com/app/profile/alejandro.espinosa3643/viz/GoogleCapstoneProject-Bellabeat/Story1">Link to Tableau</a></li> <li>ApplewatchFibit viz: <a href="https://public.tableau.com/app/profile/alejandro.espinosa3643/viz/GoogleCapstoneProject-BellavistaApplewatchdata/Dashboard1">Link to Tableau</a></li> <li>FitbitGrades viz: <a href="https://public.tableau.com/app/profile/alejandro.espinosa3643/viz/GoogleDataAnalyticsCapstoneProjectBellabeat-Fitbitandgrades/Dashboard1">Link to Tableau</a></li> </ul> {:/} |

Finally, the entire project is stored in this [GitHub repository](https://github.com/alefisico/GoogleCapstoneBellabeat).

### Results and recommendations

The outcomes of this study are:
 * Highly active people can use Bellabeat's Time and Leaf to track their activities, heart rate, and sleep patterns. This study suggested that highly active people have different active patterns than more sedentary people; if advertising is targeted to these groups, it should be used on different days.
 * In terms of sleeping patterns, the marketing department can be focused on showing users that tracking sleeping states with Bellabeat's Time and Leaf can let users know when they are sleeping less.
 * This study shows that women and men have different health metrics, and even some indications being active can improve women's intellectual activities. This can be used explicitly for Bellabeat to show their customers the value of a women-focused company.
 * The data used in this analysis can be further utilized to predict activity levels. This step is covered in the Data Science part of the portfolio.

A set of slides highlighting the results and recommendations can be found [here](https://docs.google.com/presentation/d/e/2PACX-1vSKc4eu_yg6UgVXtkCkp-ac1YA5E5xynui-IClT2iQgJy0rznOoJZ5TYUkthFRJyu7PE_GNBLgKui3L/pub?start=false&loop=false&delayms=10000).

## Data Science

After completing the capstone project and having a deeper look at the datasets, I got some ideas that I want to explore, showing other tools that I dominate. In this part of my portfolio, I am showing machine learning techniques applied to answer some questions that I got from the datasets:

| Tools used                      | Goals                                           | Code/Notebooks/Links          |
|---------------------------------|-------------------------------------------------|------------------------------------------|
| `statsmodels` regressions, `scikit-learn`, `XGBoost`, `Feature importance`, `ML Optimizations`  | Can I infer the number of calories burned from other variables collected by the apple watch?. By answering this goal, I can show different regression techniques. | [Link to the notebook](https://www.kaggle.com/code/aleespinosa/calories-regression-in-data-from-apple-watch-user/notebook) |
| `sklearn`, `classification`, `LogisticRegression`, `RandomForest`, `XGBoost`, `Exploratory Data Analysis`, `matplotlib`, `seaborn` |  The famous _Titanic competition_. Here I test many different ML algorithms. | [Link to the notebook](https://www.kaggle.com/code/aleespinosa/titanic-competition-attempt) |
| `pyspark`, `binary classification`, `SQL`, `Feature engineering` | I use `pyspark` in one the Kaggle Monthly Challenges. | [Link to the notebook](https://www.kaggle.com/code/aleespinosa/learning-pyspark-with-may22-tps) |
| `TensorFlow`, `Keras`, `sklearn`, `multilabel classification`, `deep neural network` | Classification problem using one the CERN LHC datasets. | [Link to the notebook](https://www.kaggle.com/code/aleespinosa/classification-lhc-jet-physics-with-simple-nn) |


__More soon__

## References

[1] Furberg, R., Brinton, J., Keating, M., & Ortiz, A. (2016). Crowd-sourced Fitbit datasets 03.12.2016-05.12.2016 [Data set]. Zenodo. [https://doi.org/10.5281/zenodo.53894](https://doi.org/10.5281/zenodo.53894)

[2] Fuller, Daniel, 2020, "Replication Data for: Using machine learning methods to predict physical activity types with Apple Watch and Fitbit data using indirect calorimetry as the criterion.", [https://doi.org/10.7910/DVN/ZS2Z2J](https://doi.org/10.7910/DVN/ZS2Z2J), Harvard Dataverse, V1

[3] Broaddus, Allie; Jaquis, Brandon; Jones, Colt; Jost, Scarlet; Lang, Andrew; Li, Ailin; et al. (2018): Dataset: Fitbits, field-tests, and grades. The effects of a healthy and physically active lifestyle on the academic performance of first year college students.. figshare. Dataset. [https://doi.org/10.6084/m9.figshare.7218497.v1](https://doi.org/10.6084/m9.figshare.7218497.v1)
