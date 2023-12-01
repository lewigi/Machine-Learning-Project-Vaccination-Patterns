# Predicting Vaccination Patterns: Analyzing Backgrounds, Opinions, and Behaviors in H1N1 and Seasonal Flu Vaccination Uptake

<img src="./images/flu-vaccine.jpg" alt="Flu Vaccine" width="1200" height="500">

## Navigating the Repository

- The repository consists of the notebook `H1N1.ipynb`, and the data sources `test_set_features.csv` `training_set_features.csv` and `training_set_labels.csv`. These files are in the root directory.

- The repository also contains a folder `images` that contains `flu-vaccine.jpg`

- The project presentation can be found in the repository at [link](./example.txt)


## Steps Taken

### 1. Data Collection

The data has been sourced from U.S. Department of Health and Human Services (DHHS). National Center for Health Statistics. The National 2009 H1N1 Flu Survey courtesy of the United States [National Center for Health Statistics.](https://www.cdc.gov/nchs/index.htm)

The data has been divided into three excel files:

* `test_set_features.csv`: These are the features for observations that we will use to generate the predictions after training our model.

* `training_set_features.csv`: These are the input variables that our model will use to predict the probability that people received H1N1 flu and seasonal flu vaccines. There are 35 feature columns in total, each a response to a survey question. These questions cover several different topics, such as whether people observed safe behavioral practices, their opinions about the diseases and the vaccines, and their demographics.    

* `training_set_labels.csv`: These are the labels corresponding to the observations in the training features. There are two target variables: h1n1_vaccine and seasonal_vaccine. Both are binary variables, with 1 indicating that a person received the respective flu vaccine and 0 indicating that a person did not receive the respective flu vaccine.

### 2. Exploratory Data Analysis (EDA)

The data was explored by making the use of vizualizations to see how the features interacts with the target variables and then we explored the distribution of target variables to check for class imbalance.

### 3. Data Preprocessing

Steps were taken to preprocess the data, such as handling categorical variables, feature scaling, encoding, and splitting the dataset into train and test sets with the use of Pipelines.

### 4. Model Selection and Training

A baseline model was developed using Logistic Regression. More complex models were also developed using Random Forest and *K*-Nearest Neighbours. Ensemble methods were applied using XGBoost. Further tuning was done using GridSearchCV.

### 5. Model Evaluation

The evaluation of various machine learning models revealed insights into their performance:

- Logistic Regression demonstrated moderate accuracy (66.87%) and a decent ROC AUC score (0.8458).
- Random Forest, after tuning, improved accuracy (67.03%) and showed a higher ROC AUC score (0.8583).
- K-Nearest Neighbours, despite tuning, had lower accuracy (60.39%) and a moderate ROC AUC score (0.7663).
- The XGBoost Classifier performed competitively with a test accuracy of 68.59% and a ROC AUC score of 0.8577.
- Notably, the XGBoost model fine-tuned with GridSearchCV exhibited the highest accuracy (69.05%) and an excellent ROC AUC score (0.8664), demonstrating superior predictive ability.

The XGBoost model with GridSearchCV stood out as the best-performing model, showcasing the highest accuracy and superior predictive capability among the models evaluated.


### 6. Model Deployment

If any model was deployed or made accessible, provide instructions or details on how to access/use the model.

### 7. Conclusion and Next Steps

The XGBoost model with GridSearchCV outperformed others, showing the highest test accuracy and ROC AUC score. It demonstrated superior predictive ability and generalization to new data, making it the best-performing model among those evaluated.

Moving forward, several steps can be taken to further enhance model performance and explore new avenues:

1. **Feature Engineering:** Investigate additional features or transformations to augment the model's predictive power.
2. **Ensemble Techniques:** Explore ensemble methods or stacking approaches to leverage the strengths of multiple models for improved performance.
3. **Further Hyperparameter Tuning:** Continuously fine-tune hyperparameters to optimize model performance, potentially exploring different parameter ranges.
4. **Cross-Validation:** Implement robust cross-validation techniques to ensure the model's stability and generalization.
5. **Feature Importance Analysis:** Conduct analysis to identify key predictors influencing the model's predictions.
6. **Deployment and Monitoring:** Prepare the top-performing model for deployment and establish monitoring mechanisms to track its performance in real-world scenarios.

These steps aim to refine and enhance the predictive capabilities of the models, ensuring robustness and applicability in practical settings.

1. Clone the repository:
   ```bash
   git clone https://github.com/lewigi/Machine-Learning-Project-Vaccination-Patterns.git
