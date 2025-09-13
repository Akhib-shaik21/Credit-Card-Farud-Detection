# Credit-Card-Farud-Detection

This project focuses on building a machine learning model to detect fraudulent credit card transactions. The dataset used contains transactional data, and due to the highly imbalanced nature of the data (significantly more legitimate transactions than fraudulent ones), an undersampling technique was applied to create a balanced dataset for training the model.

## Dataset

The dataset used for this project is `creditcardcsv.csv`. It contains various features (anonymized as V1-V28, plus Time and Amount) and a 'Class' column indicating whether a transaction is legitimate (0) or fraudulent (1).

## Approach

1.  **Data Loading and Exploration**: The dataset was loaded into a pandas DataFrame, and initial exploration was performed to understand the data structure, check for missing values, and analyze the distribution of legitimate and fraudulent transactions.
2.  **Handling Imbalanced Data**: Recognizing the significant class imbalance, an undersampling technique was employed. A sample of legitimate transactions equal to the number of fraudulent transactions was randomly selected.
3.  **Creating a Balanced Dataset**: The sampled legitimate transactions were combined with the fraudulent transactions to create a new, balanced dataset.
4.  **Splitting Data**: The balanced dataset was split into features (X) and the target variable (Y - 'Class').
5.  **Training and Testing Split**: The data was further split into training and testing sets to evaluate the model's performance on unseen data. Stratified sampling was used to ensure that the proportion of legitimate and fraudulent transactions is the same in both the training and testing sets.
6.  **Model Training**: A Logistic Regression model was trained on the balanced training data.
7.  **Model Evaluation**: The trained model was evaluated using accuracy score on both the training and testing datasets.

## Results

The Logistic Regression model achieved an accuracy of approximately **[Insert Training Accuracy Here]** on the training data and **[Insert Test Accuracy Here]** on the test data.

## Files

*   `creditcardcsv.csv`: The dataset used for this project.
*   `credit_card_fraud_detection.ipynb`: The Jupyter Notebook containing the code for data processing, model training, and evaluation.

## Libraries Used

*   pandas
*   numpy
*   sklearn
