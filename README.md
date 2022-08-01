# Alphabet Soup Charity Analysis

## Analysis Overview

Beks needs a binary classifier made to predict whether or not applicants will be successful if funded by Alphabet Soup.

## Results

### Data Preprocessing
- What variable(s) are considered the target(s) for your model?
    - IS_SUCCESSFUL
- What variable(s) are considered to be the features for your model?
    - APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, and ASK_AMT
- What variable(s) are neither targets nor features, and should be removed from the input data?
    - EIN, NAME, and SPECIAL_CONSIDERATIONS

### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
    - After the third optimization, there were 100 nodes in layer 1, 50 in layer 2, and 25 in layer 3. The activation functions Leaky ReLU, ReLU, and Tanh were used respectively.
- Were you able to achieve the target model performance?
    - After three optimizations, target performance was not achieved.
- What steps did you take to try and increase model performance?
    - Steps taken to improve model perforamance included adjusting the binning on the APPLICATION_TYPE and CLASSIFICATION features, removing various features to gauge their impact on the model, increasing and decreasing the number of neurons and layers, using different activation functions for each layer, and adjusting the number of epochs.

## Summary

Overall, none of the optimizations made to the model increased the overall performance. Both the loss and accuracy hovered around 0.55 and 0.72 respectively despite changes made. It was found that the SPECIAL_CONSIDERATIONS feature had little impact on the models performance, whereas the other features would cause the model's accuracy to drop well below 0.72. Recommendations for alternative models would include Random Forest and Support Vector Machine. The reasoning is that neural networks have many moving parts and can be difficult to fine tune. If tabular data is being used, using a simpler model better suited to the type of data may achieve similar, if not better results with less time and effort involved.
