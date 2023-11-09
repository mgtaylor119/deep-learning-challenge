# Alphabet Soup Charity Deep Learning Model Report

## Overview of the Analysis

The purpose of this analysis was to develop a deep learning model for Alphabet Soup, a charity organization. The goal was to create a model that could effectively predict whether applicants for funding will be successful or not. This prediction will help Alphabet Soup make informed decisions about which organizations to fund, potentially maximizing their impact.

## Results

### Data Preprocessing

- **Target Variable**:
  - The target variable for our model is `IS_SUCCESSFUL`.

- **Features**:
  - The features used for the model include:
    - 'NAME', 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', and 'ASK_AMT'

- **Excluded Variables**:
  - The following variables were removed from the input data as they were neither targets nor features:
    - 'EIN' Column

### Compiling, Training, and Evaluating the Model

- **Model Architecture**:
  - We selected a neural network model with the following specifications:
    - Number of Layers: 2
    - Number of Neurons per Layer: 7 and 10
    - Activation Functions: relu and sigmoid on the Output Layer

- **Model Performance**:
  - Loss: 0.5642023086547852, Accuracy: 0.7946355938911438
  - I was able to achieve the target model performance of >75%.

- **Steps Taken to Improve Performance**:
  - Original instructions had us remove 'EIN' and 'NAME' columns, in the Optimized code I only removed 'EIN'
  - I added a batch_number into the model to aid in the speed of running the 100 epochs, since adding Name back in gratly increased the number of records/features
  - I dropped the layer neurons to 7 and 10

## Summary

In summary, the deep learning model performed successfully once adding in more features. I attempted several different versions without adding 'NAME' back in, but could not get to above 75%.
