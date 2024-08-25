# Happiness dataset Analysis Using Machine-Learning

### Project Overview:

This project analyzes the determinants of happiness using the happiness dataset from the wooldridge package in R. We conducted data cleaning, exploratory data analysis (EDA), and predictive modeling to understand the factors influencing happiness and to predict happiness levels

### Data Source:

The dataset used for this project is the happiness dataset from the wooldridge package. The dataset is publicly available and can be accessed through the R package. You can install the package and load the dataset using the following R commands:

install.packages("wooldridge")

library(wooldridge)

data("happiness")

### Dataset:

The dataset consists of 10,000 rows and 34 columns, including various socio-economic and demographic factors such as:

Work status
Income
Occupational prestige
Education level
TV hours

### Tools Used:

- R Programming Language: Core language for data analysis and visualization.
- ggplot2: For creating visualizations and exploratory data analysis.
- randomForest: For building and evaluating the Random Forest model.
- caret: For data partitioning and model training.
- pROC: For calculating and plotting ROC curves and AUC.
- kernlab: For building and evaluating the Support Vector Machine model.

### Data Cleaning and Preparation:

1. **Handling Missing Values:**
   
   - Numerical variables with missing values (e.g., prestige, educ, babies, etc.) were imputed using the mean of the respective column.
Categorical variables with missing values (e.g., workstat, divorce, widowed, etc.) were imputed using the mode of the respective column.

2. **Conversion to Factors:**
   
   - Several variables were converted to factors to facilitate categorical analysis. This included variables like happy, mothfath16, black, gwbush04, etc.

3. **Data Type Adjustments:**
   
   - The happy variable, which represents happiness levels, was adjusted to a factor with levels very happy and not too happy to streamline the analysis.

### Exploratory Data Analysis:

- Visualizations: Bar plots and box plots to explore relationships between happiness and factors like work status, income, education, etc.
- Insights: Identified significant relationships between happiness and socio-economic factors.

### Predictive Modeling

The Predictive Modeling phase involves building and evaluating machine learning models to predict happiness levels based on various features. The following models were implemented and evaluated:

1. **Logistic Regression:**
   - Model Building: Used logistic regression to predict the probability of being "very happy" based on features such as work status, income, and education.
   - Evaluation:
     - Accuracy: Achieved an accuracy of approximately 87.9%.
     - Precision: Calculated at 88.1%.
     - Recall: Achieved a high recall of 99.7%.
     - ROC-AUC: The area under the curve (AUC) was 0.7807, indicating good model performance.

3. **Random Forest:**
   - Model Building: Implemented a Random Forest classifier to handle non-linearity and interactions between features.
   - Evaluation:
     - Accuracy: Achieved an accuracy of approximately 87.7%.
     - Precision: Calculated at 87.9%.
     - Recall: Achieved a high recall of 99.8%.
     - ROC-AUC: The AUC was 0.5008, indicating that the model’s performance was close to random guessing.

3. **Support Vector Machine (SVM):**
   - Model Building: Used a Support Vector Machine with a linear kernel to classify happiness levels.
   - Evaluation:
     - Accuracy: Achieved an accuracy of approximately 87.8%.
     - Precision: Calculated at 87.8%.
     - Recall: Achieved a perfect recall of 100%.
     - ROC-AUC: The AUC was 0.5000, suggesting the model performed similarly to random guessing.

This modeling phase aimed to identify the best-performing model for predicting happiness based on the provided features and insights gained during the EDA phase.

### Summary of Findings:

- Best Model: Logistic Regression was the best-performing model overall, with the highest ROC-AUC score and a strong balance between precision and recall.
- Model Limitations: While the Logistic Regression model provided the best performance, the Random Forest and SVM models did not outperform Logistic Regression and had ROC--AUC scores close to random guessing, indicating potential limitations in feature representation or model complexity.
