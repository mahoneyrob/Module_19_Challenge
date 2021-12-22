# Overview
This project was to use a deep neural net to analyze the success of a charitable donation campaign. Nine different parameters were read in to analyze and compare to a success metric.  The model encoded objects in different columns, and scaled the numeric data for analysis with less bias.

# Results

## Data Preprocessing
- What variable(s) are considered the target(s) for your model?
	- There was one variable to be targeted, and it was called "is_successful."
- What variable(s) are considered to be the features for your model?
	- There are nine features to this models.  We had application_type, affiliation, classification, use_case, organization, status, income_amt, special_considerations, and ask_amt.
- What variable(s) are neither targets nor features, and should be removed from the input data? 
	- There were 2 variables that we dropped as they had no influence on if a grant was given.  Those were the organization's EIN and their Name.

## Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation functions did you select for your neural network model, and why?
	- I did 2 layers in the original model, and based on the started code, I made the first with 80 neurons, and the second with 30.  The hidden layers both used ReLU as the activation, and the output layer used the sigmoid function as we wanted a 1 or a 0.  
- Were you able to achieve the target model performance?
	- No.  The goal was to get to 75% or higher, but the original model came in at about 72.5%.
- What steps did you take to try and increase model performance? 
	- The optimization steps did not improve the results by much.  I did 3 try's with the neural network, and then one with the random forest.  The first neural network got to 72.4%, the second to 72.4%, and the third to 72.2%.  These variations were created by doing a combination of using more layers, adding more neurons per layer, and reducing the number of object categories.  The last part with the random forest yielded an even lower expected success rate at 70.5%.

# Summary
It appears that a good model cannot be achieved with this data set.  Every tweak tried either yielded the same accuracy, or even dropped the accuracy.  In addition, other modeling methods, such as random forest, were not any better.  To do an additional analysis, I conducted a fourth try with fewer dataset, dropping application_type, affiliation, and classification, and dropped to 2 layers.  This gave even a lower accuracy at about 60%.  In conclusion, it appears that this dataset cannot be optimized above 75%.