# Deep Learning Challenge Report

## Overview 
The purpose of this analysis is to develop a predictive model for Alphabet Soup, a nonprofit foundation, to identify funding applications with the highest likelihood of success. The project involves preprocessing a dataset of over 34,000 past applications, capturing various features like organization type and funding requested. Two neural network models—a base and an optimized version—were developed to improve prediction accuracy. This analysis aims to help Alphabet Soup optimize resource allocation, ensuring support for initiatives most likely to achieve positive outcomes and maximize societal impact.
## Results
### Data Preprocessing
#### Target Variable(s) for the Model:
The target variable is **IS_SUCCESSFUL**, indicating whether the funding was used effectively by the applicant.
#### Feature Variables for the Model:
Features include **APPLICATION_TYPE**, **NAME**, **AFFILIATION**, **CLASSIFICATION**, **USE_CASE**, **ORGANIZATION**, **INCOME_AMT**, **ASK_AMT**, and encoded versions of categorical variables after preprocessing.
#### Variables Removed from the Input Data:
Non-beneficial ID columns such as **EIN**, along with **STATUS** and **SPECIAL_CONSIDERATIONS**, were removed as they do not contribute predictive power to the model, based on the hypothesis that they had little impact on the outcome. 
### Compiling, Training, and Evaluating the Model
#### Neurons, Layers, and Activation Functions Selected:
* **Base Model**: Featured two hidden layers with 80 and 30 neurons, respectively, using the ReLU activation function for hidden layers and sigmoid for the output layer.
* **Optimized Model**: Included three hidden layers with 50, 30, and 10 neurons, and employed the same activation functions. The adjustments aimed to capture complex patterns more effectively without significantly increasing computational complexity.
#### Achievement of Target Model Performance:

The optimized model achieved an accuracy of approximately 77.7%, indicating a successful increase in predictive performance compared to the base model's 72.8% accuracy. This improvement surpassed the initial performance target, demonstrating the effectiveness of the optimizations made.
#### Steps Taken to Increase Model Performance:
* Preprocessing Adjustments: Modified the binning strategy for APPLICATION_TYPE and CLASSIFICATION, and introduced binning for NAME to reduce overfitting and manage dimensionality.
* Model Architecture Refinement: Increased the depth of the neural network by adding an additional hidden layer and adjusted the number of neurons in each layer to better capture the complexity of the dataset.
* Feature Engineering: Removed less informative features and those hypothesized to have minimal impact on the model's predictive ability.
* Data Scaling: Applied StandardScaler to normalize the feature variables, ensuring that the neural network could more effectively learn from the data.
