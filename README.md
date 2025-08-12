# Heart Disease Prediction

This project demonstrates a machine learning approach to predict heart disease using a dataset from Kaggle.

## Project Steps

1. **Importing the Dataset:** The dataset was downloaded from Kaggle using the Kaggle API.  
2. **Loading the Dataset:** The `heart.csv` file was loaded into a pandas DataFrame for analysis and preprocessing.  
3. **Data Preprocessing:**  
   - Checked for missing values (none found in this dataset).  
   - Separated features (`X`) and target (`y`) variables.  
   - Identified categorical and numerical features.  
   - Applied One-Hot Encoding to categorical features using `ColumnTransformer` and `Pipeline`.  
   - Split the data into training and testing sets using `train_test_split`.  
4. **Training a Decision Tree Classifier:** Initialized and trained a Decision Tree model on the preprocessed training data.  
5. **Visualizing the Decision Tree:** Visualized the trained Decision Tree to understand its structure and decision rules.  
6. **Analyzing Overfitting and Controlling Tree Depth:**  
   - Evaluated the initial Decision Tree’s performance on training and testing data to check for overfitting.  
   - Explored the impact of `max_depth` on accuracy by training and evaluating Decision Trees with different depth limits.  
7. **Training a Random Forest Classifier:** Initialized and trained a Random Forest model as an ensemble method to improve performance and reduce overfitting.  
8. **Comparing Accuracy:** Compared the accuracy of Decision Tree and Random Forest classifiers on the test set.  
9. **Interpreting Feature Importances:** Extracted feature importances from the Random Forest model to identify the most influential features in predicting heart disease.  
10. **Evaluating using Cross-Validation:** Performed cross-validation on both models to obtain a more robust estimate of performance.  

## Results and Conclusion

- Both the Decision Tree and Random Forest models achieved high accuracy in predicting heart disease.  
- The Random Forest model showed slightly better performance in mean cross-validation accuracy.  
- Important features identified from the Random Forest model include:
  - Chest pain type (`cp_0`)
  - `oldpeak`
  - `thalach`
  - Number of major vessels (`ca_0`)
  - Thalassemia types (`thal_2`, `thal_3`)  
- Experimenting with `max_depth` in the Decision Tree showed the importance of controlling complexity to reduce overfitting.

This project provides a solid foundation for heart disease prediction using machine learning. Future improvements could include:
- Hyperparameter tuning
- Testing other algorithms
- Deeper analysis of important features  

## How to Reproduce

1. Ensure you have a Kaggle account and set up your Kaggle API credentials.  
2. Run the provided Jupyter Notebook cells in order.  
3. The notebook will:
   - Download the dataset
   - Preprocess the data
   - Train the models
   - Evaluate their performance  

## Dependencies

- pandas  
- scikit-learn  
- matplotlib
