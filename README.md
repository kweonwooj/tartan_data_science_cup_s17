# Tartan Data Science Cup III

<div align="center">
  <img src="./input/front.png"><br><br>
</div>

## Abstract
[Tartan Data Science Cup III](http://www.stat.cmu.edu/tartandatasciencecup/episodeIII/index.html)

- Host : [**Capital One**](https://www.capitalone.com/)
- Prize : AppleTV + USD 50 Amazon Card
- Problem : Binary Classification
- Evaluation : [Brier Score](https://en.wikipedia.org/wiki/Brier_score)
- Period : Feb 4 2017 9AM ~ 6PM (9 hours)

Capital One hosted a 1-day data science hackathon with CMU Department of Statistics to challenge undergraduates and potential employees with real-world machine learning problem. Loan data from Lending Club was provided which contained information about the loaner and loans itself in numeric and categorical variables. Using the train dataset, we were challenged to predict if the 'loan_status' is in one of the following groups:

- Group 0: "**Good**" -- The loan is fully paid off ("Fully Paid"), in its grace period ("In Grace Period"), or currently being paid back ("Current"). 

- Group 1: "**Bad**" -- The loan is in default ("Default"), payment on the loan is late ("Late (16-30 days)" or "Late (31-120 days)"), or the loan has been charged off ("Charged Off").

Competition was co-hosted by Capital One and CMU. Four employees from Captial One was actively communicating and providing helps to the participants, they were really nice. Staffs from CMU Department of Statistics were well-organized and encouraging throughout the competition.

My team, 'Anything Random', approached this problem by generating appropriate feature representation on top of the fine-tuned XGBoost model. 100+ participants with 40+ teams competed in this one-day data science competition. 15 Finalists were selected by their prediction accuracy to move on to 2nd stage. 2~3 pages of technical report write-up was submitted describing the problem, methods and results of our machine learning pipeline. 8 finalists were selected to make 5-min presentation on team's effort.

My team ended up with 2nd place overall. It was nice to hear that we were 1st place in prediction accuracy among all participants.

## Cross-Validation Result
| Brier Score | Numeric Only (9) | + Categorical (26) | + new features (29) | outlier clipping | 
|:----------:|:----------:|:---------:|:----:|:----------:|
| RandomForest | 0.0898 | 0.0857 | 0.0855 | 0.0854 |
| LogisticRegression | - | - | - | 0.0861 |
| ExtraTrees | - | - | - | 0.0854 |
| XGBoost | - | - | - | 0.0844 |

## How to Run

**[Data]** 

Place data in ```input``` directory. 

**[Code]**

Above results can be replicated by runinng all commands in ```anything_random.ipynb``` notebook.

Make sure you are on Python 3.5.2 with library versions same as specified in requirements.txt

## Overall Result
- **1st place** in Prediction Accuracy
- **2nd place** in Overall [Prediction Accuracy + Report Write-up + Oral Presentation]
