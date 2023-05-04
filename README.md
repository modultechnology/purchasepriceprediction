# purchasepriceprediction

This repository contains code related to purchase price prediction experiments. 
Some of these experiments were part of the EPOCH project.

## Data

The data needed for these experiments can be found in the data folder.
The folder contains synthetic data.

Data files contain the following set of attributes:
- BEDAT - date
- Price_Change_rel - the relative price change
- Schädling (rolling-Schädling-MeanSentiment,-TotalFrequency,-MeanSentiment) - sentiment counts and frequency for pest
- GeneralWoodDamage (rolling-GeneralWoodDamage-MeanSentiment,-TotalFrequency,-MeanSentiment) - sentiment counts and frequency for general wood damage
- Wetter (rolling-Wetter-MeanSentiment,-TotalFrequency,-MeanSentiment) - sentiment counts and frequency for weather
- Folgeindustrie ((rolling-FolgeIndustrie-MeanSentiment,-TotalFrequency,-MeanSentiment)) - sentiment counts and frequency for the wood industry

## Setup

In order to rerun these experiments, please follow the following steps.

1. configure an MLFlow instance
2. create a config file in which to keep all the data related to your MFlow and experiment configuration (e.g., please check the notebooks for the parameters needed in this config file).
3. run a notebook using the created config file.

## Example models

Some basic preprocessing (e.g., missing values) is presented in the datasetcreatorv2.ipynb notebook.

Several example models are provided:
- XGBoost
- Random Forest
- LSTM
- GRU (2 variants)

## Experiments

Please make sure to install all dependencies. It is recommended to run the notebooks using a GPU (e.g., on Google Colab), as the LSTM and GRU model need more time to compute the SHAP values and create the corresponding visualization.

## Interface

A graphical user interface that allows you to quickly browse through the results is also available at the following [address](https://demo.modultech.eu/toolb/).


## License

Attribution-NonCommercial-ShareAlike 4.0 International ([CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)).
