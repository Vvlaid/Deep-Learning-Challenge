# Deep-Learning-Challenge

## Overview of the Analysis
The purpose of this analysis is to create a binary classification model using deep learning techniques to predict if an organization funded by Alphabet Soup will be successful in their venture. The model utilizes a dataset of over 34,000 organizations that have received funding from Alphabet Soup, containing metadata about each organization.

## Results
### Data Preprocessing
- Target variable(s) for the model: The target variable for the model is IS_SUCCESSFUL.

- Feature variable(s) for the model: The feature variables for the model include APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT.

- Variable(s) removed from the input data: The EIN and NAME columns were removed from the input data as they are identification columns and not useful as features or targets.

- Feature variable NAME has been brought back in the last model.

### Compiling, Training, and Evaluating the Model
- Neurons, layers, and activation functions selected for the neural network model and rationale: The model consists of three hidden layers with 80, 30, and 1 neurons, respectively, and ReLU activation functions. The output layer uses a sigmoid activation function for binary classification. The structure was chosen to provide a balance between complexity and the potential for overfitting, while maintaining the ability to learn complex patterns in the data.

![image](https://github.com/user-attachments/assets/4934d5f8-3f5c-4fe8-87e5-13eb351fabba)

After trying different units and different layers the accuraccy rating I achieved was as follows:

![image](https://github.com/user-attachments/assets/09fe6e52-70df-4127-8b2c-3e4e120989ae)

Unfortunately did not achieve the 75% I was aiming for, all combinations I seeked got me roughly the same results.

### Summary and Recommendation

Overall, by optimizing the model we are able to increase the accuracy to above 73%.

This means we are able to correctly classify each of the points in the test data 73% of the time. In other words an applicant has a close to 80% chance of being successful if they have the following:

- The NAME of the applicant appears more than 5 times (they have applied more than 5 times)
- The type of APPLICATION is one of the following: T3, T4, T5, T6 and T19
- The application has the following values for CLASSIFICATION: C1000, C1200, C2000,C2100 and C3000.

### Alternative Method

Although this model worked very well and provided a great deal of accuracy, an alternative approach to recommend is the Random Forest model as it is also suited for classification problems. Using the Random Forest model we can achieve close to 78% accuracy.
