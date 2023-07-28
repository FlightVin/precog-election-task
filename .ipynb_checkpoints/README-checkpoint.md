# PreCog Election 2024 Screening Task

## Analysis Task

### Preprocessing

Relevent data is stored in the `analysis-task/data` folder by running the notebook `analysis-task/preprocessing-data.ipynb`.

The analysis tasks mainly revolve around a subset of columns for the years 2009, 2014 and 2019. Hence the notebook stores a subset of the complete data (`analysis-task/data/year/full-data.csv`) as well as rows about the winners (`analysis-task/data/year/winner-data.csv`) for these years using pandas.

### Analysis

We use Pandas for reading the data and matplotlib for plotting in the notebook `analysis-task/analysis.ipynb`.

Three questions have been considered:
1. Do voters turn up in larger numbers to change the incumbent MP?
2. How likely are SC/ST candidates to win in a general seat?
3. What were the effects of changing party between 2009-14 and 2014-19?

The conclusions as well as the methodology (using graphs) have been elaborated upon in the notebook.

### Classification

We use Pandas for reading data, PyTorch for the model and scikit-learn for data splits and measures in the notebook `analysis-task/classification.ipynb`.

Two questions have been considered:
1. Are competitive elections governed by voter turnout and number of candidates?
2. How many terms has the MP won based on a few parameters

Classification has been done using Logistic Regression with Stochastic Gradient Descent considering Binary Cross Entropy Loss. Analysis and measures have been included in the notebook.

(Base logistic regression code has been taken from online.)

## Paper Reading Task

Report on _A Survey of Computational Framing Analysis Approaches_ has been included in the directory `paper-reading-task`.

## About Me

- Name: Vineeth Bhat
- Roll Number: 2021101103
- Stream: CSE (Entering 5th Semester)