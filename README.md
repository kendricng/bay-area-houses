# Housing Prices in the Bay Area: An Introduction to Data Science

# Table of Contents

1. [Installation](https://github.com/kendricng/bay-area-houses#1-installation)
2. [Repo Motivation](https://github.com/kendricng/bay-area-houses#2-repo-motivation)
3. [File Descriptions](https://github.com/kendricng/bay-area-houses#3-file-descriptions)
4. [Summary of Results](https://github.com/kendricng/bay-area-houses#4-summary-of-results)
5. [Others](https://github.com/kendricng/bay-area-houses#5-others)

# 1. Installation

The scripts in the Jupyter notebooks are written in Python 3.7+ using the below libraries:

## Data Manipulation

- [numpy](https://numpy.org/): for some mathematical computations and array manipulation; and
- [pandas](https://pandas.pydata.org/): for most of the data manipulation and analysis.

## Data Visualization

- [matplotlib](https://matplotlib.org/): for plotting basic graphs; and
- [seaborn](https://seaborn.pydata.org/): for generating more sophisticated graphs.

## Model Prediction

- [scikit-learn](https://scikit-learn.org/): for machine learning tasks; and
- [scipy](https://www.scipy.org/): for basic 2 dimensional linear regression and imputation of normal distributions.

Since production code was not written in mind, note that there may be issues with running the notebooks when running future versions of these packages.

# 2. Repo Motivation

This repository explores the relationship between housing prices and other house-related information in the San Francisco Bay Area. 

The main reason I wanted to create this repo is because I am currently in the process of searching for my first house purchase, and I want to learn as much as I can about what makes houses affordable or expensive.

# 3. File Descriptions

Guide others through the files in your repository. You may not talk about every file here, but you should let them know where they can find the work they might find most interesting.

This repository consists of the following files:

## Data

1. [Housing Data - Raw](raw.csv); and
2. [Housing Data - Clean](clean.csv).

I extracted residential housing price data from publicly available real estate information during February 2020 using a third party Chrome extension web scraper.

## Jupyter Notebooks

1. [Preprocessing](Preprocessing.ipynb): contains the scripts to clean the raw data extracted by the web scraper;
2. [Exploration](Exploration.ipynb): analyzes the data to get a better understanding of the Bay Area real estate; and
3. [Prediction](Prediction.ipynb): build a basic linear regression model to predict real estate prices.

# 4. Summary of Results

## Technical Summary

Using a Linear Regression model, I have built a basic machine learning model to predict housing prices in the Bay Area mainly by using the following predictive features:

1. area (e.g. San Francisco, South Bay, East Bay); and
2. square footage.

This model resulted in an R squared value of 0.60 on the test set.

## Feature Engineering

I improved the score of this model mainly by using the following strategies:

1. Removal and Imputation of Missing Values;
2. Log Transformation;
3. Dimensionality Reduction;
4. Outlier Removal; and
5. Removal of Non-Performative Features.

## Edge Cases

The purpose of this repository is to understand the real estate market in the Bay Area for my first home purchase. Hence, a lot of the edge cases related to large houses (e.g. mansions, large acreage lots) have been removed.

## Data Integrity Issues

During the data scraping phase of the project i.e. `Preprocessing`, the data was not of the highest quality, with missing values for many of the features. 

Many of the values have been imputed by using the mean or median, and other values have been dropped. Much of the rationale for imputing missing values are largely driven by rules of thumb about houses (e.g. high correlation between `bed` and `bath`). 

Data integrity is a well known issue within the real estate industry, and a central database of cleaned real esate data is a highly sought after proprietary asset.

## Room for Improvement

Since most of the model's accuracy was provided by `area` and `sqft`, I would dig deeper into how to create more area or district specific features (e.g. transit time, crime rates, industry growth).

## Non-Technical Summary

I have also included a [Medium article](https://medium.com/@kendricng/should-i-buy-a-house-in-san-francisco-54df7a42763e) that is written for audiences without a data science background. 

# 5. Others

## License

[MIT License](LICENSE)

## Acknowledgements

I would like to acknowledge the following parties who have inspired and motivated me to create this repository:

- [Udacity Data Science Nanodegree Program](https://www.udacity.com/course/data-scientist-nanodegree--nd025): for providing the program structure to push me to create my first official data science repository; and
- Other contributors and peers (anonymous) who provided feedback on the technical and non-technical pieces of the project.

## Discussion and Feedback

For any questions, comments, and feedback on this repository, both technical and non-technical, feel free to reach out to me at Twitter [@KendricNg](https://twitter.com/KendricNg).
