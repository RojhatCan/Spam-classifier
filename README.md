### Spam Classifier

In this project, a **Logistic Regression** classifier is used to build a spam classifier based on the feature vectors created in the data preparation pipeline.

#### Steps:
1. **Logistic Regression Model**:
   - **Solver**: The "lbfgs" solver is used for optimization, which is efficient for small datasets and works well for multinomial logistic regression.
   - **Maximum Iterations**: The `max_iter` parameter is set to 1000 to ensure the model converges, especially with larger datasets.
   - **Random State**: A fixed `random_state=42` is set for reproducibility of results.

2. **Cross-Validation**:
   - **Cross-validation**: The model is evaluated using **3-fold cross-validation** (`cv=3`), which splits the dataset into 3 parts, training and validating on each fold.
   - **Verbose Output**: The `verbose=3` parameter is set to print the progress during the cross-validation process.
   
3. **Model Evaluation**:
   - The mean score from the cross-validation is calculated with `score.mean()`, giving an average performance measure across all folds.

This approach helps in assessing the model's ability to generalize and gives a better estimate of its performance on unseen data.
