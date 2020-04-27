---
title: "A Study on Gradient Boosting Classifiers"
description: "My undergraduate thesis with an experimental analysis of LightGBM hyperparameters in classification models"
date: '2019-12-01'
link: 'https://www.linux.ime.usp.br/~robotenique/mac0499/'
screenshot: 'tcc.gif'
layout: 'portfolio'
featured: true
---
Gradient Boosting Machines (GBMs) is a supervised machine learning algorithm that has been achieving state-of-the-art results in a wide range of different problems and winning machine learning competitions. When building any machine learning model, the hyperparameter optimization can become a costly and time-consuming task depending on the number and the hyperparameter space of the tuning procedure. Machine learning users that are not experienced researchers or data science professionals can struggle to define which hyperparameters and values to choose when starting the model tuning, especially with newer GBMs implementations like the XGBoost and LightGBM library. In this work, a large-scale experiment with 70 datasets is conducted using the OpenML platform, measuring the sensitivity of binary classifiers evaluation metrics to changes in three LightGBM hyperparameters.

A solid statistical framework is applied to the study results, analyzing the behavior from three different viewpoints: results by hyperparameters, results by characteristics of the dataset and results by performance metric. The carried out experiments indicate insightful relationships of the hyperparameters in gradient boosting classifiers, uncovering which combinations of hyperparameters resulted in models with the highest change in the metrics from the baseline, what metrics are most sensitive and which characteristics of the studied datasets stood out. These results are hereby here presented to facilitate the model building of gradient boosting classifiers for machine learning users.
