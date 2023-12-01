# Predicting Vaccination Patterns: Analyzing Backgrounds, Opinions, and Behaviors in H1N1 and Seasonal Flu Vaccination Uptake

<img src="./images/flu-vaccine.jpg" alt="Flu Vaccine" width="1200" height="500">

## Navigating the Repository

- The repository consists of the notebook `H1N1.ipynb`, and the data sources `submission_format.csv` `test_set_features.csv` `training_set_features.csv` and `training_set_labels.csv`. These files are in the root directory.

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

A baseline model was developed using Logistic Regression. More complex models were also developed using Random Forest and *K*-Nearest Neighbours

### 5. Model Evaluation

Explain how the models were evaluated, including performance metrics, confusion matrices, ROC curves, etc. Discuss the results obtained and their implications.

### 6. Model Deployment (if applicable)

If any model was deployed or made accessible, provide instructions or details on how to access/use the model.

### 7. Conclusion and Next Steps

Summarize the findings, limitations, and potential future improvements or directions for the project.


1. Clone the repository:
   ```bash
   git clone https://github.com/lewigi/Machine-Learning-Project-Vaccination-Patterns.git
