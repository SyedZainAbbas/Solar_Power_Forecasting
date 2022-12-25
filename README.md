The aim of this project is to predict the amount of energy generated by a solar power plant using the weather parameters. But what is solar power,
how do we produce it and why do we need forecasting?

## Introduction to Solar Energy

Solar energy is simply the conversion of radiation from the sun to useful energy. When the sun shines onto a solar panel, energy from the sunlight is
absorbed by the Photovoltaic (PV) cells in the panel. This energy creates electrical charges that move in response to an internal electrical field in the
cell, causing electricity to flow.

## Need for Forecast

Upto this point, this sounds like a free energy. We just have to do some initial investments and start generating electricity with it. However, life is not that
simple, is it? Especially, if you are producing solar energy commercially. One of the many challenges in producing solar energy on a commercial level is to 
balance the grid. But first, what is grid balancing?

### Grid Balancing
Electricity has to be used in real time as storing it is an expensive option. Usually, electricity is bought on a day ahead market because it is cheaper than a real
time market. Every power plant has to inform the grid operators that it will feed this amount of energy into the grid at a certain point in time. If that amount of 
energy is not supplied to the grid at that time, the grid operators will charge that power plant with heavy fines as they have to take emergency measures to keep
the supply balanced with the demand.
 
However, solar energy is highly dependent on weather, on a bright sunny day you will produce a lot more than required whereas on a cloudy day you might produce
nothing but the grid has to be fed with the amount of energy promised earlier in time. This calls for a forecasting job.

## Project Overview 
In this project, I have used ambient temperature, module temperature, and irradiation for predicting the amount of enregy a solar power plant will generate. The
machine learning algorithms used for this purpose are the following.

1. Linear Regression
2. Decision Tree Regressor
3. Random Forest Regressor
4. Lasso Regression
5. Ridge Regression
6. XGBoost Regression

A pipeline was created for each model which takes the data normalize it and feed it into the model. The best model based on **RMSE** and **R2** values was
**XGBoost** so I further optimised the parameter of this model according to the dataset. This model predicts the power generated by solar panels with 10-15%
error but this error can be reduced if we include more weather parameters such as humidity, DHI, GHI, etc.

The dataset used for this project was taken from: https://www.kaggle.com/datasets/anikannal/solar-power-generation-data
