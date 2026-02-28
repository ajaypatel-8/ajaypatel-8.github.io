---
title: "Rainfall Prediction in Australia (MIDS DATASCI 207 Final Project)"
layout: post
categories: [grad, ml]
---

For my UC Berkeley MIDS DATASCI 207 final project, my team and I studied next-day rainfall prediction in Australia using the WeatherAUS dataset. We framed the task as predicting `RainTomorrow` from daily weather variables, and built the pipeline with a strict chronological split and expanding-window cross-validation to avoid temporal leakage.

We compared Logistic Regression, Random Forest, RNN, and PatchTST baselines, then tested latent-space generative approaches (VAE and latent WGAN) to better capture rainy-day structure in a highly imbalanced setting. Our manifold-aware approach improved rain-day forecasting compared to purely discriminative models and gave better ROC-AUC with a more balanced precision-recall tradeoff for the rainy class. The project repo is here: [MIDS DS207 Final Project (AARVE)](https://github.com/UC-Berkeley-I-School/mids_ds207_finalproject_aarve/tree/main).
