# Overview of the analysis

The purpose of the analysis is to determine whether or not an applications for investment from the foundation will be successful based on a variety of features of the application

# Results

## Data Preprocessing

The target variable used in the model is the "IS_SUCCESSFUL" feature. This indicates whether or not the application for investment was successful.

The variables used as features are "APPLICATION_TYPE", "CLASSIFICATION", "AFFILIATION", "ORGANIZATION", "INCOME_AMT", and "ASK_AMT". "STATUS" and "SPECIAL_CONSIDERATIONS" were both used for the initial analysis but were later dropped during the optimization phase.

Variables that were neither targets nor features are the "EIN" and "NAME" variables will don't provide any distinguishing signal regarding the chance of an investment.

## Compiling, Training, and Evaluating the Model

In the final attempt, the number of params in the model was 54,849 with 5 layers (4 hidden, 1 output) and activation functions GELU and RELU in the hidden layers and Sigmoid for the output layer. The number of layers were increased in hopes of acheiving a better fit. Note that lower amounts of layers and neurons were used in a previous attempt to check for overfitting. A sigmoid output layer was used since the result is a classification.

The target model performance was not reached using the models in the analysis.

Attempts to reach the desired performance involved dropping binary features that were heavily one sided such as "STATUS" and "SPECIAL_CONSIDERATIONS". Additionally, the neurons,hidden layers and activation functions were varied to check for over and underfitting.

# Summary

Overall, the results show that regardless of the size of the model (layers and neurons) and activation functions, the performance remained the same. This could mean we are extracting the most signal from our features and data and without different features or more data, the performance of the model won't improve. Another method of improving performance would be to use an ensemble model due to the the difference in performance on the training data vs test data.
